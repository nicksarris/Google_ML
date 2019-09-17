# Instacart Market Basket Analysis: 

---

"In this competition, Kaggle is challenging you to build a model that predicts the total ride duration of taxi trips in New York City. Your primary dataset is one released by the NYC Taxi and Limousine Commission, which includes pickup time, geo-coordinates, number of passengers, and several other variables."

---

### Competition Data

Link - https://www.kaggle.com/c/instacart-market-basket-analysis/data

<pre>
Instacart_Cleaned -----|----- data ---------------------------------|----- aisles.csv
                       |----- .gitignore                            |----- departments.csv
                       |----- README.md                             |----- order_products__prior.csv
                       |----- instacart_labelling_script.ipynb      |----- order_products__train.csv
                       |----- instacart_lightgbm.ipynb              |----- orders.csv
                       |----- instacart_processing_script.ipynb     |----- products.csv
                       |----- instacart_product_script.ipynb
                       |----- instacart_splitting_script.ipynb
                       |----- instacart_statistics_script.ipynb
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
