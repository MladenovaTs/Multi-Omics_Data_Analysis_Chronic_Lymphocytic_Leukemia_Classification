# Multi-Omic Data Analysis for Chronic Lymphocytic Leukemia (CLL) Classification

## Objective

The goal of this analysis was to explore a multi-omic biomedical dataset comprising 200 human Chronic Lymphocytic Leukemia (CLL) samples. The primary task was to develop and evaluate supervised machine learning models that integrate the most informative features across various omics data types — methylation, gene expression, drug response, and somatic mutations — to accurately classify samples based on their biological sex annotation.

## Methodology

### 1. Data Preparation

- **Data Integration:** The omic datasets were merged based on sample IDs, ensuring correct alignment of data types without information loss. The datasets included drug response, somatic mutations, methylation, and gene expression features, along with the biological sex annotation as the target variable.
- **Missing Data Handling:** Missing data were managed using imputation techniques to minimize information leakage and preserve dataset integrity. Each dataset was normalized separately.

### 2. Feature Selection and Engineering

- **Initial Feature Analysis:** Features were initially evaluated for relevance to the biological sex annotation using statistical methods such as correlation analysis and mutual information scores.
- **Feature Engineering:** New features were generated through transformations and combinations of existing features to capture complex relationships between omics data and the target variable.

### 3. Model Building

- **Model Selection:** Various machine learning models were evaluated, including Logistic Regression, Random Forest, and XGBoost. The Random Forest model was ultimately selected for its robustness and ability to handle large numbers of features with potential noise.
- **Model Training:** The model was trained on the integrated dataset with careful tuning of hyperparameters to optimize performance.

### 4. Model Evaluation and Interpretation

- **Performance Metrics:** The model’s performance was evaluated using metrics such as accuracy, precision, recall, area under the ROC curve (AUC), and R-squared. Cross-validation was employed to ensure generalizability.
- **Feature Importance:** The contribution of each feature to the model’s decisions was assessed to interpret predictions, with the mRNA and methylation datasets showing the most significant impact.
- **Error Analysis:** Misclassifications were analyzed to identify model limitations and potential areas for improvement.

## Findings and Results

- **Model Performance:** The XGBoost model achieved high accuracy and AUC, indicating strong discriminative power in classifying samples based on biological sex. The XGBoost model also performed well, showcasing the effectiveness of feature integration from multiple omic sources.
- **Key Features:** Features from the mRNA and methylation datasets were identified as the most significant contributors to the classification task.
- **Challenges:** Key challenges included managing data imbalance, integrating diverse omic data types without losing critical biological signals, and interpreting model results to derive biological insights.

## Conclusion

The analysis successfully demonstrated the integration of multi-omic data for predictive modeling in a biological context, particularly for classifying CLL samples by biological sex. The Random Forest and XGBoost models provided robust performance, validating the approach's effectiveness. However, challenges related to data integration, class imbalance, and model interpretability suggest areas for further improvement.

## Recommendations

- **Biological Insight Exploration:** Further investigation into the biological significance of the identified important features is recommended.
- **Advanced Modeling Techniques:** Consideration of more sophisticated models, such as ensemble methods or neural networks, to potentially enhance predictive performance.
- **Generalizability Testing:** Applying the developed methodology to other multi-omic datasets to validate its broader applicability.

## Report Overview

This combined report synthesizes the findings and methodologies from both the Python and RMD reports to present a cohesive overview aligned with the task objectives outlined in the Omniscope assessment document.
