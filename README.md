Forecasting ICU Admissions for COVID-19 Patients in Brazil: A Data-Driven Approach 

![image](https://github.com/user-attachments/assets/274f92b9-d026-40cc-a9e9-8a6ecada3ac7)

Abstract 
The COVID-19 pandemic has strained healthcare systems worldwide, particularly in countries like Brazil with diverse healthcare infrastructure. Efficient ICU bed allocation has become critical. This project aims to use machine learning techniques to predict ICU admissions for COVID-19 patients in Brazil, helping optimize resource management. By analyzing patterns and risk factors associated with ICU admissions, the model can support decision-making and improve healthcare delivery. Data for this study is sourced from a Kaggle dataset provided by SírioLibanês Hospital (https://www.kaggle.com/datasets/S%C3%ADrio-Libanes/covid19). 

Data Description, Exploration and Processing  

The dataset, after being cleaned and scaled, contained missing values that were handled using forward-fill and backward-fill techniques to maintain data consistency. Forward-fill replaced missing values with the last known value, while backward-fill used the next available value. These methods helped preserve data quality, especially in key patient-level features like clinical and demographic details. The dataset included important features such as patient identifiers, age percentiles, and ICU admission status, the latter being the primary outcome of interest

Visualizations, including heatmaps and count plots, were employed to explore how ICU admissions varied across different age groups and periods. Heatmaps were used to display relationships between variables, while count plots showed the frequency of ICU admissions in various categories, aiding in identifying trends and patterns.

![image](https://github.com/user-attachments/assets/2cd16922-a46c-4b04-ac58-2aa8a72e50c3)

Machine Learning Models 

Three machine learning models were employed to predict ICU admissions: Logistic Regression, Random Forest Classifier, and Decision Tree Classifier. The following sections detail the model training, evaluation, and optimization processes. the window column was dropped before working on the models. This is because there would be a lot of assumptions if it had to be included in the features.  

Logistic Regression Accuracy before optimization: 80% Accuracy after optimization: 81%Class 0 (non-ICU patients)precision: 82%Recall: 93%class 1 (ICU patients)precision: 71%recall: 47%

Random ForestAccuracy: 81% Class 0 (non-ICU patients)precision: 89%Recall: 85%class 1 (ICU patients)precision: 65%recall: 72%

Decision TreeAccuracy before optimization: 75% Accuracy after optimization: 80%Class 0 (non-ICU patients)precision: 82%Recall: 85%class 1 (ICU patients)precision: 56%recall: 50%

Conclusion 

This study demonstrates the potential of machine learning models to predict ICU admissions for COVID-19 patients in Brazil. Healthcare providers can better allocate ICU resources and improve patient outcomes by leveraging data and advanced modeling techniques. Future research should incorporate additional features, such as treatment history, to enhance prediction accuracy and model robustness. It should also include time stamps for the vitals, that way the window column can be better utilized. All the models did well, but they had trouble accurately predicting the minority class, this indicates an imbalance in the data that needs to be addressed. This could be addressed using techniques like SMOTE, feature engineering, and the exploration of ensemble methods to enhance predictive performance, particularly for ICU patients. On the overall performance of all the models, Random Forest outperformed the rest, and it will be the ideal model to use in future predictions. 
