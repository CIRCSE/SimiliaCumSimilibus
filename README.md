# SimiliaCumSimilibus

## What's this?

In this repo you will find the scripts and materials used to collect the data from the treebanks published in [Universal Dependencies](http://universaldependencies.org/) used in the research paper *Similia cum similibus congregantur*.

The paper is currently under review.


## Content

* `conllu_to_conllx.pl`: Perl script provided from the UD team (see [here](https://github.com/UniversalDependencies/tools/blob/master/conllu_to_conllx.pl)) to convert CoNLL-U (the format of the UD treebanks) to the CoNLL-X format. This preprocessing step is needed, because [`NLTK`](http://nltk.org/) currently doesn't have a reader for the CoNLL-U format.
* `Dependency VS Co-occurrence network.ipynb`: Jupyter Notebook detailing (well, sort of...) the steps to transform the converted CoNLL-X files to the edge list (saved as CSV files) that will be used to generate the networks.
* `syntacticNetwork.py`: despite the name, it contains the same code as the Jupyter Notebook above in a single script.
* `syntacticNetwork.log`: a log on the number of sentences and tokens processed per each language; generated by the previous script.
* `network_files`: folder that contains the CSV edge list for each treebank; generated by the previous script.
* `lemma-pos`: folder that contains a file per language, associating the lemmas found in the treebank with its assigned PoS.