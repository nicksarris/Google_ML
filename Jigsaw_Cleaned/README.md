# Jigsaw Unintended Bias in Toxicity Classification: 

---

"The Conversation AI team, a research initiative founded by Jigsaw and Google (both part of Alphabet), builds technology to protect voices in conversation. A main area of focus is machine learning models that can identify toxicity in online conversations, where toxicity is defined as anything rude, disrespectful or otherwise likely to make someone leave a discussion. When the Conversation AI team first built toxicity models, they found that the models incorrectly learned to associate the names of frequently attacked identities with toxicity ... In this competition, you're challenged to build a model that recognizes toxicity and minimizes this type of unintended bias with respect to mentions of identities. You'll be using a dataset labeled for identity mentions and optimizing a metric designed to measure unintended bias. Develop strategies to reduce unintended bias in machine learning models, and you'll help the Conversation AI team, and the entire industry, build models that work well for a wide range of conversations."

---

### Competition Data

Link - https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification/data

<pre>
Jigsaw_Cleaned -----|----- data ----------------------------|----- train.csv
                    |----- .gitignore                       |----- test.csv
                    |----- README.md
                    |----- jigsaw_bert_inference.ipynb
                    |----- jigsaw_bert_processing.ipynb
                    |----- jigsaw_bert_training.ipynb
</pre>

---

### Generating Solution

In order to generate the solution file for this competiton, simply download the mentioned files from the given link and place them in their proper directory as shown in the diagram above before running the individual utility scripts. To be able to train the model, you must first generate **order_train.csv** and **"order_test.csv**. In order to do so, you must first run the following scripts sequentially: 

<pre>
1. instacart_labelling_script.ipynb -> ./data/previous_products.pkl
2. instacart_statistics_script.ipynb -> ./data/user_department_products.pkl | ./data/user_aisle_products.pkl
3. instacart_splitting_script.ipynb -> ./data/chunk_0.pkl
4. instacart_product_script.ipynb -> ./data/product_periods_stat.pkl
5. instacart_processing_script.ipynb -> ./data/order_train.csv | ./data/order_test.csv
</pre>

After running **instacart_processing_script.ipynb**, you'll have generated **order_train.csv** and **order_test.csv**. Ensure that they're in their proper directory and run **instacart_lightgbm.ipynb**. The file will be generated and placed in the ./data/ folder for further exploration.

---
