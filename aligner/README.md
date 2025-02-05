## Overview
We priovide all code and processed data to replicate the sentence alignment experiment in our paper.

## Usage



## Data
You can find all processed data and checkpoints from this [Dropbox folder](https://www.dropbox.com/sh/ohqaw41v48c7e5p/AADb6_qWCwgHvsCqg121cK9Ma?dl=0).

For both Newsela-Manual and Wiki-Manual, we have prepared the processed gold paragraph alignment for train/dev/test sets and paragraph alignment generated by our algorithm for dev/test sets. 

The code is designed to work out-of-box with Newsela data. Due to permission restriction, please contact us for the processed data used in Newsela-Manual experiment.

Once you got the data, you can use the followiong command to run the code:

```
python aligner.py  --train_gold newsela-processed-file/train_perfect_paragraph_alignment.pkl   --dev_gold newsela-processed-file/dev_perfect_paragraph_alignment.pkl    --test_gold newsela-processed-file/test_perfect_paragraph_alignment.pkl    --dev_real newsela-processed-file/dev_inperfect_paragraph_alignment.pkl   --test_real newsela-processed-file/test_inperfect_paragraph_alignment.pkl --BERT_folder wiki-auto-dropbox/aligner-checkpoint-newsela
```

The processed data for Wiki-Manual is in the above folder. 



## Checkpoints

We have provide the BERT-base checkpoints finetuned on Newsela-Manual and Wiki-Manual datasets in the above folder.
