# Instacart Market Basket Analysis
: 

---

"Whether you shop from meticulously planned grocery lists or let whimsy guide your grazing, our unique food rituals define who we are. Instacart, a grocery ordering and delivery app, aims to make it easy to fill your refrigerator and pantry with your personal favorites and staples when you need them. After selecting products through the Instacart app, personal shoppers review your order and do the in-store shopping and delivery for you ... In this competition, Instacart is challenging the Kaggle community to use this anonymized data on customer orders over time to predict which previously purchased products will be in a user’s next order."

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
1. **instacart_labelling_script.ipynb** -> ./data/previous_products.pkl'<br />
2. **instacart_statistics_script.ipynb** -> ./data/user_department_products.pkl   |   ./data/user_aisle_products.pkl<br />
3. **instacart_splitting_script.ipynb** -> ./data/chunk_0.pkl<br />
4. **instacart_product_script.ipynb** -> ./data/product_periods_stat.pkl<br />
5. **instacart_processing_script.ipynb** -> ./data/order_train.csv   |   ./data/order_test.csv<br />
</pre>

After running **instacart_processing_script.ipynb**, you'll have generated **order_train.csv** and **"order_test.csv**. Ensure that they're in their proper directory and run **instacart_lightgbm.ipynb**. The file will be generated and placed in the ./data/ folder for further exploration.

---
