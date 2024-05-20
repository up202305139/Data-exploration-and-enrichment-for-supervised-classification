# Data-exploration-and-enrichment-for-supervised-classification
The Hepatocellular Carcinoma Dataset
In this project, the goal is to address a real data science use case from data cleaning and feature assessment to visual inspection and communication of results, using the Hepatocellular Carcinoma (HCC) dataset. The HCC dataset was collected at the Coimbra Hospital and University Center (CHUC) in Portugal and contains real clinical data of patients diagnosed with HCC. The main goal of this project is to develop a machine learning pipeline capable of determining the survivability of patients at 1 year after diagnosis (e.g., “lives” or “dies”). To address this project, students should focus on each step of a standard data science pipeline and explore suitable solutions to develop an efficient machine learning solution:

● Data Exploration: An initial exploratory data analysis should be carried out including examining feature types, number of features/records, class distribution, values per attribute, etc., and highlighting feature inconsistencies such as missing values, outliers, underrepresented concepts, irrelevant features, etc. The analysis can and should be supported with visualization techniques.

● Data Preprocessing: This refers to feature pre-processing (e.g., imputation of missing values, data transformation, data scaling, etc.) and feature engineering (e.g., building new features or removing redundant features) and other tasks considered relevant.

● Data Modeling (Supervised Learning): Supervised learning includes the identification of the target concept, definition of the training and test sets, selection and parameterization of the learning algorithms to employ, and evaluation of the learning process (in particular on the test set). Decision Trees and KNN (e.g., using Scikit-learn) should be used to build classification models. Other classifiers are optional and considered as “extra elements”.

● Data Evaluation: Classification results should be compared across different evaluation metrics (performance during learning, confusion matrix, ROC/AUC, precision, recall, accuracy) using a standard train/test split. Results should be compared using tables and plots (e.g., using Seaborn or Matplotlib libraries). Other partitioning methods are considered “extra elements”.

● Interpretation of Results: This involves extracting meaningful insights from the obtained results: explain the behavior of the models, drawing conclusions about the effectiveness of the chosen algorithms and preprocessing techniques, providing recommendations for future analysis, investigating discrepancies of unexpected findings, etc.


------

**DATA EXPLORATION:** 
A exploração dos dados permitiu identificar relações entre variáveis, destacar padrões e possíveis áreas de melhoria.
 

**DATA PREPROCESSING:**
Para melhorar a qualidade dos dados e o desempenho dos métodos de machine learning:

**01** Imputação de valores em falta
Substituição dos valores em falta pela moda/média da coluna correspondente

**02** Remoção de colunas com base na correlação
Identificação de pares de colunas com alta correlação e eliminação das que possuem menor correlação com a variável alvo (‘Class’).

**03** Remoção de colunas com base na frequência de 'Nan' e na variância
Identificação de colunas com mais valores em falta ('Nan') e mais baixa variância

Colunas removidas: Grams_day, Spleno, PHT, Dir_Bil, AST, Sat, Ferritin, Iron, Packs_year, Varices, Smoking, HBeAg, Endemic, HBcAb e Hemochro.


**DATA MODELING:**
Usamos como métodos de pesquisa supervisionada o k-nearest neighbors algorithm, o decision tree classifier e random forest, para estudar o nosso dataset e identificar o conceito alvo.


**DATA EVALUATION:**
Comparamos os métodos de pesquisa através de gráficos com a performance de cada um durante a aprendizagem, matrizes de confusão, curvas ROC/AUC, precisão, recall, exatidão e f1-score.


**DATA INTERPRETATION:**
Em termos de precisão, recall, exatidão e F1-score, os algoritmos KNN e Random Forest superam a Decision Tree. No entanto, o Random Forest tem maior pontuação AUC, pelo que parece ser o algoritmo mais eficaz para o nosso conjunto de dados.


------

**Instruções:**

**01** Usar Python 3.12.3

**02** Ter o ficheiro 'hcc_dataset.csv'

**03** Ter os imports todos necessários 

