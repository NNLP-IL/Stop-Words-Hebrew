# Stop-Words-Hebrew
The list was produced through Universal Dependencies of the The Israeli Association of Human Language Technologies (IAHLT) who analyzed sentences from the Hebrew wikipedia.

From the UD we extracted the following POS:
DET - determiner (including article; examples: כל/כול, אף, שום)
ADP - adposition (preposition/postposition; examples: למרות, ליד, לפני)
PRON - pronoun (examples: הוא, זה, כך, מי)
CCONJ - coordinating conjunction (examples: אך, אבל, או, אלא, בין)
SCONJ - subordinating conjunction (examples: אשר, כי, אילו)
SYM - non-punctuatuon symbolSymbol (examples: %, $, =)

The result provides us with a reasonable list, which, however, required little cleaning.
On the other hand the UD does not include all the words because of its limited nature like לפיכן,בשבילכן
*We will soon add a paragraph about the aggressive tokenization of UD and its effect on the project with examples and how we dealt with it*
In the second step we went through the list manually and made corrections like removing unnecessary words and adding words that we recognized as missing.

Feel free to add words using Pull Request.

The attached files are:
Stopwords notebook.iypnb - Notebook that allows you to restore the list.
Stop words.txt - list of stop words

