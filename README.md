# Arabic POS Tagging Using Transformers

<html>
<img src="https://camo.githubusercontent.com/9819a757acc12aadc0ead8a46334a7aae56bcedaa64d69d49b9e074c1ce47c8d/68747470733a2f2f64333377756272666b69306c36382e636c6f756466726f6e742e6e65742f643563626334623065313463323066383737333636623639623931373136343961666531316664612f64393661382f6173736574732f696d616765732f62696772616d2d686d6d2f706f732d7469746c652e6a7067" width="100%">
</html>

In natural language processing (NLP), **Part of Speech (POS)** refers to **the grammatical category** or syntactic function that a word serves in a sentence. It's a way of categorizing words based on their roles within the structure of a sentence. POS tagging involves assigning a specific label, such as **noun**, **verb**, **adjective**, **adverb**, etc., to each word in a sentence.

Here are some common parts of speech:

| Tag              | Arabic Tag | Description |
| :---------------- | ------: | :---- |
| Noun (N)        |   اسم   | Represents a person, place, thing, or idea. Examples: dog, city, happiness. |
| Verb (V)           |   فعل   | Describes an action or occurrence. Examples: run, eat, sleep. |
| Adjective (ADJ)    |  صفة   | Modifies or describes a noun. Examples: happy, tall, red. |
| Adverb (ADV) |  حال   | Modifies or describes a verb, adjective, or other adverb. Examples: quickly, very, well. |
| Pronoun (PRON) |  ضمير   | Replaces a noun. Examples: he, she, it. |


# Dataset
Im this notebook I will use [ UD_Arabic-PADT](https://github.com/UniversalDependencies/UD_Arabic-PADT)
The treebank consists of 7,664 sentences (282,384 tokens) and its domain is mainly newswire.
The annotation is licensed under the terms of
[CC BY-NC-SA 3.0](http://creativecommons.org/licenses/by-nc-sa/3.0/)
and its original (non-UD) version can be downloaded from
[http://hdl.handle.net/11858/00-097C-0000-0001-4872-3](http://hdl.handle.net/11858/00-097C-0000-0001-4872-3).

The morphological and syntactic annotation of the Arabic UD treebank is created through
conversion of PADT data. The conversion procedure has been designed by Dan Zeman.
The main coordinator of the original PADT project was Otakar Smrž.

### Source of annotations

This table summarizes the origins and checking of the various columns of the CoNLL-U data.

| Column | Status |
| ------ | ------ |
| ID | Sentence-level units in PADT often correspond to entire paragraphs and they were obtained automatically. Low-level tokenization (whitespace and punctuation) was done automatically and then hand-corrected. Splitting of fused tokens into syntactic words in Arabic is part of morphological analysis. [ElixirFM](http://elixir-fm.sf.net/) was used to provide context-independent options, then these results were disambiguated manually. |
| FORM | The unvocalized surface form is used. Fully vocalized counterpart can be found in the MISC column as Vform attribute. |
| LEMMA | Plausible analyses provided by ElixirFM, manual disambiguation. Lemmas are vocalized. Part of the selection of lemmas was also word sense disambiguation of the lexemes, providing English equivalents (see the Gloss attribute of the MISC column). |
| UPOSTAG | Converted automatically from XPOSTAG (via [Interset](http://ufal.mff.cuni.cz/interset)); human checking of patterns revealed by automatic consistency tests. |
| XPOSTAG | Manual selection from possibilities provided by ElixirFM. |
| FEATS | Converted automatically from XPOSTAG (via Interset); human checking of patterns revealed by automatic consistency tests. |
| HEAD | Original PADT annotation is manual. Automatic conversion to UD; human checking of patterns revealed by automatic consistency tests. |
| DEPREL | Original PDT annotation is manual. Automatic conversion to UD; human checking of patterns revealed by automatic consistency tests. |
| DEPS | &mdash; (currently unused) |
| MISC | Information about token spacing taken from PADT annotation. Additional word attributes provided by morphological analysis (i.e. ElixirFM rules + manual disambiguation): Vform (fully vocalized Arabic form), Translit (Latin transliteration of word form), LTranslit (Latin transliteration of lemma), Root (word root), Gloss (English translation of lemma). |


