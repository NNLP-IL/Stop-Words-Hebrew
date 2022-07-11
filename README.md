# Stop-Words-Hebrew


There is some ambiguity in the definition of stop words. Stop words are words that are commonly used in any language. The words "the", "is" and "and" would easily qualify as stop words in English.

In the absence of a definition, we created two lists, a long one and a more minimalist one. It gives the user more flexibility to choose the appropriate list based on their use case. During the process of creating the lists, we kept in mind two different use cases. For example, we recommend using the short list for taks like retrieving information. However, we recommended using the long one for topic analysis.
The basic list was produced through Universal Dependencies of the The Israeli Association of Human Language Technologies (IAHLT) who [analyzed sentences from the Hebrew wikipedia](https://github.com/UniversalDependencies/UD_Hebrew-IAHLTwiki). 

From the UD we extracted the following POS:  
DET - determiner (including article; examples: כל/כול, אף, שום)  
ADP - adposition (preposition/postposition; examples: למרות, ליד, לפני)  
PRON - pronoun (examples: הוא, זה, כך, מי)  
CCONJ - coordinating conjunction (examples: אך, אבל, או, אלא, בין)  
SCONJ - subordinating conjunction (examples: אשר, כי, אילו)  
SYM - non-punctuatuon symbol (examples: %, $, =)  

The short list is created by intersecting the UD list with the 1000 most frequent words from Wikipedia

This long list was compiled from three sources:
1. The 50 most frequent words on Wikipedia
2. List that extract from the UD
3. A custom list that we have added manually.

The reason for this responds to the fact that the UD tokenization follows more radical rules than whitespace tokenization. Moreover, the UD tokenization is of high quality, as it is manually performed. For this reason, the original list did not include tokens like - שלו - איתך - ועם; in UD these tokens are morphologically segmented: the prepositions are separated from the pronouns and the conjunctions are separated from the prepositions, like in these examples: של+ו - אית+ך - ו+עם. In order to adapt the list to simpler whitespace tokenized corpora, we added words that we recognized as missing.

Feel free to add or remove words using Pull Request.  
The attached files are:  
prepare_stop_word.ipynb .iypnb - A notebook that can be used to recreate the lists.     
stopswords_list_extend.txt  - long list of stop words  
stopswords_list_short.txt  - short list of stop words  
top_3000_most_freq_wiki.csv - 3000 frequent words from Wikipedia.   
