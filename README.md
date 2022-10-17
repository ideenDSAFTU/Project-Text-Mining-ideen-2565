# codeless data mining
# Measuring similarity English translations of Surah Al-Fatihah using computational calculation methods.
 
## Overview
   The Qur'an has been translated in many different versions by using different translation sentence. For example, the word Allah has more than one translation. Some translate to “God” some translate to “Lord”.

   In this project, I would like to know whether the translations are similar or not. By measuring the similarity of Surah Al-Fatihah ( The opening) using four models; text processing , Term Frequency-inverse Document Frequency or TF, IDF and cosine Similarity.

## Methodology
### Tools of use
- a computer
- Knime Analytics Platform
- Ecxel
- GitHub, GitHub Desktop
### package in need
- Textproccessing (in knime)

### Steps to do

<p float="left">
 <img src="1.PNG" alt="data" width="700"/> 
</p>

- Data Access 
- Tranform Data
- Text preprocessing
- Create model 
- View the result

####  Data Access 

Use the excel file in the datasets folder of this repository

<p float="left">
 <img src="2.PNG" alt="data" width="200"/> 
</p>

####  Tranform Data

<p float="left">
 <img src="3.PNG" alt="data" width="500"/> 
</p>

- Use Column filter node to remove unused column(surah,text,ayat)
- Use Tranpose node to tranpose data 
- Use Column combiner to combine 7 columns into a single column.
<p float="left">
 <img src="2.1.PNG" alt="data" width="500"/> 
</p>

- Use Column filter node to remove unused column(all column except new column)
- Use Column Appender node to create new id
- Use String Manipulation node to remove -




####  Text preprocessing

<p float="left">
 <img src="4.PNG" alt="data" width="500"/> 
</p>

- Use String to Document node to change string to document
- Use Column filter node to remove unused column
- Use Punctuation Erasure to remove punctuation (? ! , . () , : ; "")
- Use case convertor node to change all character to be lowercase letter
- Use Stop Word Filter node to remove stop word
- Use POS Tagger node ,Stanford node to separate word Part of speech(nouns,verbs, adverb etc.)
- Use Standford Lammatizer node to make the verb to be base form

<p float="left">
 <img src="4.1.PNG" alt="data" width="500"/> 
</p>

- Use Bag of Word Creator node to create bag of word

####  Model 

<p float="left">
 <img src="5.PNG" alt="data" width="500"/> 
</p>

- Use TF-IDF node to be Model
- Use Math Formula node for calculate(TF*log(IDF))
- Use TF-IDF model to calculate weight of words



  
###  Cosine similarity

<p float="left">
 <img src="6.PNG" alt="data" width="500"/> 
</p>

## Result

#### Result of Data access
<p float="left">
 <img src="Data access.PNG" alt="data" width="500"/> 
</p>

#### Result of Tranform Data 
<p float="left">
 <img src="Tranform Data.PNG" alt="data" width="500"/> 
</p>

#### Result of Text Processing 
<p float="left">
 <img src="Text Processing.PNG" alt="data" width="500"/> 
</p>

#### Result of TF
<p float="left">
 <img src="TF.PNG" alt="data" width="500"/> 
</p>

#### Result of IDF
<p float="left">
 <img src="12.png" alt="data" width="500"/> 
</p>

#### Result of cosine similarity

<p float="left">
 <img src="14.png" alt="data" width="500"/> 
</p>

#### Result of cosine similarity to see similarity  between documents

<p float="left">
 <img src="19.png" alt="data" width="500"/> 
</p>

<p float="left">
 <img src="20.PNG" alt="data" width="500"/> 
</p>

# Conclusion

# Suggestion
