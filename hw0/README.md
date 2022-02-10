In the ZIP document there are two folders: wordcount and bigram.
In each folder there are my py code, originral txt document, and the output folder.

Because it is running in a folder which contains both xxx.py and wiki.txt, the command below can be used to run:

spark-submit ./wordcount.py ./wiki.txt ./output ##

Please make sure there are no output folder created before running the command above(remove the output folder before you run).

Interpretation of the output (document named 'part-00000'):

1)For the wordcount: 
e.g.
('ancient', 2777)
('isaac', 359)
('led', 3618)

It's simply the word and its count.

2)For the bigram: 
e.g.
('european', 4567, ('european', 'circus'), 1, 0.00022)

The single word 'european' has a total count of 4567 in the original txt file, and the bigram 'european circus' has a count of 1. Thus the conditional bigram distribution frequency is 1/4567 = 0.00022. The calculation outcome has been rounded to 5 digits in my code.

-*--*-this-is-the-end-of-the-readme-file-*--*-
