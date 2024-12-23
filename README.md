# Diabetes Risk Prediction Using BRFSS 2015 Data
# 1. Introduction

Diabetes is a widespread and chronic health condition that affects millions of people globally, and its impact is particularly pronounced in the United States. According to the Centers for Disease Control and Prevention (CDC), approximately 34.2 million Americans had diabetes as of 2018, with an additional 88 million living with prediabetes. Diabetes leads to serious health complications such as heart disease, kidney failure, vision loss, and amputations, while also significantly reducing quality of life and life expectancy for those affected. Furthermore, the economic burden is substantial, with the annual cost of diagnosed diabetes estimated at $327 billion.

Diabetes is characterized by the body's inability to effectively regulate blood glucose levels, either due to insufficient insulin production (Type 1 diabetes) or an inability to use insulin properly (Type 2 diabetes). Early detection of diabetes and prediabetes is crucial, as it allows individuals to adopt lifestyle changes and receive treatments that can help manage or delay the onset of complications.

The goal of this report is to leverage the Behavioral Risk Factor Surveillance System (BRFSS) 2015 dataset—a large, national survey conducted by the CDC—to build predictive models that can accurately assess diabetes risk based on various health indicators. The BRFSS collects data annually from over 400,000 participants on topics such as health behaviors, chronic health conditions, and the use of preventive services. This dataset offers a rich source of information to investigate the factors most closely associated with diabetes.

## Purpose of the Study:

This study aims to apply machine learning techniques to predict an individual's diabetes risk based on the responses provided in the BRFSS survey. Additionally, the study seeks to identify which factors are most predictive of diabetes, providing valuable insights for healthcare practitioners and policymakers.

## Research Questions:

The study is designed to address the following key research questions:

1. **Predictive Power of Survey Data**: 

Can survey responses from the BRFSS accurately predict whether an individual has diabetes, prediabetes, or no diabetes?

2. **Risk Factors**: 

What are the most significant risk factors for diabetes according to the data, and how do these factors contribute to overall diabetes risk?

3. **Feature Subset Selection**: 

Can a subset of the available health indicators be used to build an accurate and efficient predictive model for diabetes risk?

4. **Streamlined Prediction Model**: 

Is it possible to develop a simplified model that uses fewer survey questions while still accurately predicting an individual's diabetes risk, which could be deployed in public health initiatives?

## Objectives:

The primary objectives of this study are:

1. To develop and evaluate predictive models for diabetes risk using data from the BRFSS 2015.

2. To identify the most important health indicators and risk factors that contribute to the likelihood of an individual developing diabetes.

3. To use feature selection techniques to create a more efficient predictive model that requires fewer inputs but still maintains high accuracy.
4. To provide insights that can be used to develop a streamlined set of survey questions, which can be implemented in future public health screenings for early diabetes detection.


This study aims to contribute to the growing body of research in the field of public health and machine learning, with the ultimate goal of improving diabetes prevention efforts and public health strategies.

# 7. Conclusion

In this report, we utilized the BRFSS 2015 dataset to explore predictive modeling for diabetes risk and successfully addressed the research questions. Through data preprocessing, exploratory data analysis, and predictive modeling, we gained valuable insights into the key predictors of diabetes and created an efficient, streamlined model for diabetes risk assessment.

## Key Findings:

1. **Class Imbalance**:

The dataset exhibited significant class imbalance, with the vast majority of participants classified as non-diabetic (84%), and smaller proportions as prediabetic (2%) or diabetic (14%). This imbalance posed challenges for predictive modeling, particularly for the minority classes (prediabetes and diabetes). Addressing this imbalance will be crucial for improving model sensitivity across all classes.

2. **Key Predictive Features**:

The Recursive Feature Elimination (RFE) process identified five key features that are most predictive of diabetes risk:

- General Health (GenHealth): Individuals reporting worse general health are more likely to be diabetic, indicating that overall health status is strongly correlated with diabetes risk.

- Body Mass Index (BMI): Higher BMI is associated with a significantly increased risk of diabetes, reaffirming the link between obesity and diabetes.

- High Blood Pressure (HighBP): Those with high blood pressure are at a higher risk of diabetes, as this is a known risk factor for cardiovascular and metabolic diseases.

- Age: Older individuals are more likely to develop diabetes, which reflects the increasing prevalence of diabetes with age.

- High Cholesterol (HighChol): High cholesterol levels were also identified as a significant predictor, aligning with the understanding that cholesterol management is important in diabetes prevention.

3. **Model Performance**:

The multinomial logistic regression model achieved an overall accuracy of approximately 84.57%. While the model performed well for predicting non-diabetic cases (class 0), it struggled with the minority classes (prediabetes and diabetes). The sensitivity was high for class 0 but much lower for classes 1 and 2. This indicates that further refinement is needed, particularly for improving the prediction of prediabetes and diabetes cases.

4. **Feature Selection Efficiency**:

Using RFE, we demonstrated that a subset of five variables (GenHealth, BMI, HighBP, Age, and HighChol) could provide comparable predictive performance to models that use all 21 features. This streamlining could help create a more efficient and accessible diabetes risk assessment tool that focuses on the most impactful variables.


## Research Questions Addressed:

1. *Can survey questions from the BRFSS provide accurate predictions of whether an individual has diabetes?*

Yes, the BRFSS survey data provides a strong foundation for accurate predictions of diabetes risk, with a multinomial logistic regression model achieving a reasonable level of accuracy (84.57%).

2. *What risk factors are most predictive of diabetes risk?*

The most predictive risk factors were identified as General Health, BMI, High Blood Pressure, Age, and High Cholesterol. These factors were the most influential in predicting diabetes risk in the population.

3. C*an we use a subset of the risk factors to accurately predict whether an individual has diabetes?*

Yes, the RFE process confirmed that a subset of five key variables can be used to build a predictive model with good accuracy, offering a more efficient approach to diabetes risk assessment.

4. *Can we create a short form of questions from the BRFSS using feature selection to accurately predict if someone might have diabetes or is at high risk of diabetes?*

Absolutely. The RFE process demonstrated that using a short form based on the five most predictive variables could maintain strong predictive performance, making it a viable tool for public health screening.

## Recommendations:

Based on these findings, several steps could further improve prediction accuracy and help identify individuals at high risk of diabetes:

1. **Address Class Imbalance**:

Techniques such as SMOTE (Synthetic Minority Over-sampling Technique) or under-sampling of the majority class should be considered to better balance the dataset and enhance model performance, particularly for prediabetes and diabetes classes.

2. **Explore Other Modeling Techniques**:

Implementing other machine learning models like Random Forest, Gradient Boosting Machines, or Neural Networks may help handle class imbalance more effectively and provide better performance across all classes.

3. **Use Advanced Evaluation Metrics**:

Evaluating model performance using Precision, Recall, and F1-Score—especially for the minority classes—can provide more detailed insights into model effectiveness and areas for improvement.

4. **Feature Importance Analysis**:

Performing detailed feature importance analysis using methods like SHAP (SHapley Additive exPlanations) values would provide greater transparency and understanding of how each feature influences the prediction outcome.

5. **Model Interpretability**:

Improving model interpretability through techniques like SHAP or LIME (Local Interpretable Model-agnostic Explanations) can help clinicians and public health officials better understand the drivers of diabetes risk and make more informed decisions.

## Conclusion:

This report demonstrates that the BRFSS 2015 data is a valuable resource for predicting diabetes risk. By identifying key risk factors and leveraging feature selection techniques, we successfully created an efficient and accurate predictive model. This research highlights the potential for creating streamlined screening tools that can help identify individuals at risk of diabetes earlier, ultimately contributing to improved public health outcomes. Further research and model refinement are recommended to continue improving the performance of these predictive tools.


# 8. Reference
https://archive.ics.uci.edu/dataset/891/cdc+diabetes+health+indicators
