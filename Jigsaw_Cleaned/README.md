# Jigsaw Unintended Bias in Toxicity Classification: 

---

"The Conversation AI team, a research initiative founded by Jigsaw and Google (both part of Alphabet), builds technology to protect voices in conversation. A main area of focus is machine learning models that can identify toxicity in online conversations, where toxicity is defined as anything rude, disrespectful or otherwise likely to make someone leave a discussion. When the Conversation AI team first built toxicity models, they found that the models incorrectly learned to associate the names of frequently attacked identities with toxicity ... In this competition, you're challenged to build a model that recognizes toxicity and minimizes this type of unintended bias with respect to mentions of identities. You'll be using a dataset labeled for identity mentions and optimizing a metric designed to measure unintended bias. Develop strategies to reduce unintended bias in machine learning models, and you'll help the Conversation AI team, and the entire industry, build models that work well for a wide range of conversations."

---

### Requirements

In order to run **jigsaw_bert_training.ipynb**, you'll also need to install nvidia-apex. In order to do so, follow the following instructions:

<pre>
$ git clone https://github.com/NVIDIA/apex
$ cd apex
$ pip install -v --no-cache-dir --global-option="--cpp_ext" --global-option="--cuda_ext" ./
</pre>

---

### Competition Data

Link (1) - https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification/data <br />
Link (2) - https://storage.googleapis.com/bert_models/2018_10_18/uncased_L-12_H-768_A-12.zip

<pre>
jigsaw_cleaned -----|----- data ----------------------------|----- train.csv                    |----- bert_config.json
                    |----- .gitignore                       |----- test.csv                     |----- bert_model.ckpt.data-00000-of-00001
                    |----- README.md                        |----- uncased_L-12_H-768_A-12 -----|----- bert_model.ckpt.index
                    |----- jigsaw_bert_inference.ipynb                                          |----- bert_model.ckpt.meta
                    |----- jigsaw_bert_processing.ipynb                                         |----- vocab.txt
                    |----- jigsaw_bert_training.ipynb
</pre>

---

### Generating Solution

In order to generate the solution file for this competiton, simply download the train/test files from the given links and place them in their proper directory before running **jigsaw_bert_processing.ipynb**. This will generate the **train_seq.pickle** file. Following this, run **jigsaw_bert_training.ipynb**, which will fine-tune BERT on the dataset. Finally, run **jigsaw_bert_inference.ipynb**. The file will be generated and placed in the ./data/ folder for further exploration.

---
