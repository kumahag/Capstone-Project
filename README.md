# Capstone-Project
Movie Review Sentiment Classification Challenge

Can you classify sentiment about movie reviews?

**Challenge Description**

This dataset contains movie reviews along with their associated binary sentiment polarity labels. It is intended to serve as a benchmark for sentiment classification.

The objective of this challenge is to, given a sentence, classify whether the sentence is of positive, negative, or neutral sentiment. For messages conveying both a positive and negative sentiment, whichever is the stronger sentiment should be chosen. Predict if the text would be considered positive, negative, or neutral (for an average user). This is a binary task.

**About**

The core dataset contains 50,000 reviews split evenly into 25k train and 25k test sets. The overall distribution of labels is balanced (25k pos and 25k neg). We also include an additional 50,000 unlabeled documents for unsupervised learning.

In the entire collection, no more than 30 reviews are allowed for any given movie because reviews for the same movie tend to have correlated ratings. Further, the train and test sets contain a disjoint set of movies, so no significant performance is obtained by memorizing movie-unique terms and their associated with observed labels. In the labeled train/test sets, a negative review has a score <= 4 out of 10, and a positive review has a score >= 7 out of 10. Thus reviews with more neutral ratings are not included in the train/test sets. In the unsupervised set, reviews of any rating are included and there are an even number of reviews > 5 and <= 5.

**Data citing**

@InProceedings{maas-EtAl:2011:ACL-HLT2011,

author = {Maas, Andrew L. and Daly, Raymond E. and Pham, Peter T. and Huang, Dan and Ng, Andrew Y. and Potts, Christopher},

title = {Learning Word Vectors for Sentiment Analysis},

booktitle = {Proceedings of the 49th Annual Meeting of the Association for Computational Linguistics: Human Language Technologies},

month = {June},

year = {2011},

address = {Portland, Oregon, USA},

publisher = {Association for Computational Linguistics},

pages = {142--150},

url = {http://www.aclweb.org/anthology/P11-1015}}

**Files**

DESCRIPTION
FILES
Train contains the target. This is the dataset that you will use to train your model.

Train.csv
32.2 MB
Is an example of what your submission should look like. The order of the rows does not matter but the name of the ID must be correct.

SampleSubmission.csv
495.9 KB
Test resembles Train.csv but without the target-related columns. This is the dataset on which you will apply your model to.

Test resembles Train.csv but without the target-related columns. This is the dataset on which you will apply your model to.

**Process**

1.This challenge is solved by applying my Data science knowledge to fine-tune a pretrained Hugging face model: First import data (test and train CSV from Zindi into Colab) 
2.Code to eliminate rows containing NaN values 
3. Load datasets into pretrained model 
4. Select model from hugging face under sentiment analysis for fine-tuning

**Fine-Tuning Steps**

1.Prepare the dataset

2.Load pretrained Tokenizer, call it with dataset(encoding)

3.Build pytorch dataset with encodings

4.Load pretrained model

5.Load trainer and train into native pytorch training loop
After fine-tuning on pretrained model, a. Embed into Grado App b. Host on Hugging Face

**Steps to upload on Hugging Face**

Create a Hugging face account
Download test- trainer folder from google Colab and save model on Hugging Face
Host your fine-tuned model and app on the Hugging Face Platform
You can find my Hugging face model at:https://huggingface.co/Mawulom/Fine-Tuned-Bert-Large-Uncased

It achieves the following results on evaluation set:

'eval_loss': 0.6932001113891602, 'eval_accuracy': 0.5, 'eval_runtime': 242.9746, 'eval_samples_per_second': 20.578, 'eval_steps_per_second': 2.572}
