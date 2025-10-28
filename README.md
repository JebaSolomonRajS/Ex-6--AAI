<H3>NAME: Jeba Solomon Raj S</H3>
<H3>REGISTER NO: 212223230089</H3>
<H3>EX. NO.6</H3>
<H1 ALIGN =CENTER>Implementation of Semantic ANalysis</H1>
<h3>Aim:</h3>
To perform Parts of speech identification and Synonym using Natural Language Processing (NLP) techniques.
 
 
## <h3>Algorithm:</h3>

Step 1: Import the nltk library.<br>
Step 2: Download the 'punkt', 'wordnet', and 'averaged_perceptron_tagger' resources.<br>
Step 3:Accept user input for the text.<br>
Step 4:Tokenize the input text into words using the word_tokenize function.<br>
Step 5:Iterate through each word in the tokenized text.<br>
•	Perform part-of-speech tagging on the tokenized words using nltk.pos_tag.<br>
•	Print each word along with its corresponding part-of-speech tag.<br>
•	For each verb , iterate through its synsets (sets of synonyms) using wordnet.synsets(word).<br>
•	Extract synonyms and antonyms using lemma.name() and lemma.antonyms()[0].name() respectively.<br>
•	Print the unique sets of synonyms and antonyms.

## <H3>Program:</H3>

```python
import nltk
#import wordnet
nltk.download( 'punkt' )
nltk.download('wordnet')
from nltk.tokenize import word_tokenize
nltk.download( 'averaged_perceptron_tagger' )
sentence=input ()
# Tokenize the sentence into words
words = word_tokenize(sentence)
# Identify the parts of speech for each word
pos_tags= nltk.pos_tag(words)
from nltk.corpus import wordnet

# Identify synonyms and antonyms for each word
synonyms =[]
antonyms =[]
for word in words:
	for syn in wordnet.synsets(word) :
		for lemma in syn.lemmas():
			synonyms . append (lemma . name( ) )
			if lemma . antonyms():
				antonyms . append ( lemma. antonyms ( ) [0] . name ( ) )
# Print the synonyms and antonyms
print ( "Synonyms : " ,set (synonyms) )
print ( "Antonyms : " ,set(antonyms) )
```

## <H3>Output</H3>
<img width="379" height="50" alt="image" src="https://github.com/user-attachments/assets/9fcd65b7-9e97-487d-b527-583c93639cb6" />

<img width="187" height="172" alt="image" src="https://github.com/user-attachments/assets/610ed1fe-4f87-41c8-8c4a-719167986efc" />

<img width="962" height="49" alt="image" src="https://github.com/user-attachments/assets/a0648a3d-3795-48ab-88a1-de81fcec8ba2" />


## <H3>Result:</H3>
Thus ,the program to perform the Parts of Speech identification and Synonymis executed sucessfully.
