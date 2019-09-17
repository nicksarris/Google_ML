# Google_ML

**This repository contains some of my past work on Machine Learning competitions. Each folder corresponds to a different project. Each script in a folder should run properly without errors, although because I primarily used cloud servers to train/run each individual model, some of the pathing and directories may be incorrect. Each individual project is described below:**

---

### Allstate Claims Severity: 

"When you’ve been devastated by a serious car accident, your focus is on the things that matter the most: family, friends, and other loved ones. Pushing paper with your insurance agent is the last place you want your time or mental energy spent. This is why Allstate, a personal insurer in the United States, is continually seeking fresh ideas to improve their claims service for the over 16 million households they protect. Allstate is currently developing automated methods of predicting the cost, and hence severity, of claims. In this recruitment challenge, Kagglers are invited to show off their creativity and flex their technical chops by creating an algorithm which accurately predicts claims severity."

Team Name: Misfyre (114th / 3055) <br />
Link to Competition: https://www.kaggle.com/c/allstate-claims-severity/ <br/>
Link to Repository: https://github.com/nicksarris/Google_ML/tree/master/Allstate_Cleaned

---

Results on Leaderboard:

| Models | Public Leaderboard | Private Leaderboard | Outcome
| :---         |     :---      |         :--- |          :--- |
| LightGBM (Included) | 1108.50187 (MAE) | 1121.82356 (MAE) | 664th / 3055
| Ensemble (Best) | 1101.21368 (MAE) | 1113.62895 (MAE) | 114th / 3055

---

For this competition, the repository contains the code for my best single model, which resulted in a mean absolute error of 1121.82356 when compared to the test labels, or 664th / 3055 on the private leaderboard. This model, blended with an XGBoost and NN solution, ended up scoring a mean absolute error of 1113.62895, good enough for 114th / 3055 on the private leaderboard. The winning solution to this competition (https://www.kaggle.com/c/allstate-claims-severity/discussion/26416#latest-261183), which employed more than 80 different models, only had a mean absolute error of 1109.70772.

---

### Instacart Market Basket Analysis

"Whether you shop from meticulously planned grocery lists or let whimsy guide your grazing, our unique food rituals define who we are. Instacart, a grocery ordering and delivery app, aims to make it easy to fill your refrigerator and pantry with your personal favorites and staples when you need them. After selecting products through the Instacart app, personal shoppers review your order and do the in-store shopping and delivery for you ... In this competition, Instacart is challenging the Kaggle community to use this anonymized data on customer orders over time to predict which previously purchased products will be in a user’s next order."

Team Name: Nick Sarris (378th / 2622) <br />
Link to Competition: https://www.kaggle.com/c/instacart-market-basket-analysis/ <br/>
Link to Repository: https://github.com/nicksarris/Google_ML/tree/master/Instacart_Cleaned

---

Results on Leaderboard:

| Models | Public Leaderboard | Private Leaderboard | Outcome
| :---         |     :---      |         :--- |          :--- |
| LightGBM (Included) | 0.40419 (F1) | 0.40249 (F1) | 378th / 2622

---

For this competition, the repository contains the code for my entire solution to this competition, which resulted in an F1 score of approximately 0.40249 when compared to the test labels, or 378th / 2622 on the private leaderboard. The second-place solution to this competition (https://www.kaggle.com/c/instacart-market-basket-analysis/discussion/38143#latest-432390, https://github.com/KazukiOnodera/Instacart) ended up with an F1 score of 0.40820.

---

### Jigsaw Unintended Bias in Toxicity Classification

"The Conversation AI team, a research initiative founded by Jigsaw and Google (both part of Alphabet), builds technology to protect voices in conversation. A main area of focus is machine learning models that can identify toxicity in online conversations, where toxicity is defined as anything rude, disrespectful or otherwise likely to make someone leave a discussion. When the Conversation AI team first built toxicity models, they found that the models incorrectly learned to associate the names of frequently attacked identities with toxicity ... In this competition, you're challenged to build a model that recognizes toxicity and minimizes this type of unintended bias with respect to mentions of identities. You'll be using a dataset labeled for identity mentions and optimizing a metric designed to measure unintended bias. Develop strategies to reduce unintended bias in machine learning models, and you'll help the Conversation AI team, and the entire industry, build models that work well for a wide range of conversations."

Team Name: Nick & Wenrui (45th / 2646) <br />
Link to Competition: https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification <br/>
Link to Repository: https://github.com/nicksarris/Google_ML/tree/master/Jigsaw_Cleaned

---

Results on Leaderboard:

| Models | Public Leaderboard | Private Leaderboard | Outcome
| :---         |     :---      |         :--- |          :--- |
| Bert Singular (Included) | N/A | N/A | N/A
| Bert Ensemble | N/A | N/A | N/A
| LSTM/Bert Ensemble (Best) | N/A | 0.94511 (AUC) | 45th / 2646 

---

For this competition, the repository contains the code for one of the BERT (BASE) models in my final ensemble to fine-tune itself and generate predictions. Sadly, I'm unable to report an accurate AUC score for this model, as there was an error on Kaggle's end with the leaderboard at the end of the competiton and previous scores were wiped. My complete solution consisted of four different, fine-tuned BERT (BASE) models, an ensemble of two Bi-LSTM and two Bi-GRU models that each differed primarily by seed, and a single BERT (LARGE) model that I fine-tuned on cloud servers. This combined model resulted in an AUC score of approximately 0.94511, or 45th / 2646 on the private leaderboard. The first-place solution to this competition (https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification/discussion/103280#latest-619135) ended up with a final score of 0.94734.

---

### New York City Taxi Trip Duration

In this competition, Kaggle is challenging you to build a model that predicts the total ride duration of taxi trips in New York City. Your primary dataset is one released by the NYC Taxi and Limousine Commission, which includes pickup time, geo-coordinates, number of passengers, and several other variables.

Link to Competition: https://www.kaggle.com/c/nyc-taxi-trip-duration <br/>
Team Name: Nick Sarris (130th / 1257)

---

Results on Leaderboard:

| Models | Public Leaderboard | Private Leaderboard | Outcome
| :---         |     :---      |         :--- |          :--- |
| Ensemble (Included) | 0.41204 (RMSE) | 0.40932 (RMSE) | 536th / 1257
| Ensemble (Best) | 0.37745 (RMSE | 0.37498 (RMSE) | 130th / 1257

---

### The Numer.ai Hedge Fund

Numerai is an AI-run, crowd-sourced hedge fund based in San Francisco. It was created by South African technologist Richard Craib in October 2015. Its primary competitors are other open source trading platforms mainly QuantConnect, Quantopian & WorldQuant. Every week, Numerai hosts a tournament in which data scientists submit their predictions in exchange for the potential to earn some amount of USD and a cryptocurrency called Numeraire.

Link to Competition: https://numer.ai/rounds <br/>
Team Name: N/A (N/A)

---

Results on Leaderboard:

| Models | Public Leaderboard | Private Leaderboard | Outcome
| :---         |     :---      |         :--- |          :--- |
| XGBoost (Included) | N/A | N/A | N/A

---
