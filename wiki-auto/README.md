Wiki-Auto provides a set of aligned sentences from English Wikipedia and Simple English Wikipedia as a resource to train sentence simplification systems. 
We first trained our Neural CRF alignment model on the Wiki-Manual dataset and then extracted aligned sentence pairs from the 138,095 parallel articles.
Here, we provide the raw Wiki-Auto dataset with alignment information and three versions of preprocessed Wiki-Auto datasets that can be directly used
to train the generation systems.


```all_data``` folder contains the raw data of the ```Wiki-Auto``` dataset in ```json``` format. 
It contains aligned article pairs between English Wikipedia and Simple English Wikipedia, and their paragraph alignment and sentence alignment information. 
The article pairs are aligned by using ```Wikidata``` database (details in our ACL 2020 paper), and all articles haven been sentence splitted. 
The paragraph alignment is generated by the paragraph alignment algorithm described in our ACL 2020 paper, and the sentence alignment is generated by our neural CRF sentence alignment model.


``ACL2020``` folder contains the Wiki-Auto training data used in our ACL 2020 paper ```Neural CRF Model for Sentence Alignment in Text Simplification```.
```train.src``` contains complex sentences, and ```train.dst``` contains simple sentences. This is a filtered version where we eliminated sentence pairs with
high (>0.9) or low (<0.1) lexical overlap based on BLEU scores. We observed that sentence pairs with low BLEU are often inaccurate paraphrases with only shared named entities and
the pairs with high BLEU are dominated by sentences merely copied without simplification. Also, this version does not contain sentence splitting.


```GEM2021/full_no_split``` folder contains the unfiltered version of the dataset, where the sentences with low and high lexical overlap are not removed. 
```train.src``` contains complex sentences, and ```train.dst``` contains simple sentences. This version does not contain sentence splitting.


```GEM2021/full_with_split``` folder also contains the unfiltered version of the dataset but we join the sentences in the simple article mapped 
to the same sentence in the complex article to capture sentence splitting.

``ACL2020``` and ```GEM2021/full_no_split``` focus on paraphrasing- and deletion-based simplification. On the other hand, ```GEM2021/full_with_split``` 
focuses on all the three operations of simplification: paraphrasing, deletion and splitting. 

