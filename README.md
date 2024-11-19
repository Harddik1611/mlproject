## End to End Machine Learning Project
### Student Performance Indicator
This project aims to understand how students' performance, as measured by their test scores, is influenced by variables such as Gender, Ethnicity, Parental Level of Education, Lunch Type, and Test Preparation Course. By analyzing these factors, the project seeks to predict students' performance and provide insights for improving academic outcomes.

### Table of Contents
1.Project Overview
2.Dataset Description
3.Project WorkFlow
4.Model And Evaluation
5.Results and Insights
6.Installation and Usage
7.Future Enhancements
8.Contribution

### 1. Project Overview
Education is a cornerstone of societal progress. Understanding the factors that impact student performance can help educators and policymakers enhance learning experiences and outcomes. This project uses machine learning techniques to:
- Explore relationships between student demographics, socio-economic factors, and academic performance.
- Predict test scores based on these variables.
- Provide actionable insights for education stakeholders.

### 2.Dataset Description
The dataset includes information about students and their test scores across three subjects (Math, Reading, and Writing).

####  Features:
- Gender: Male/Female
- Ethnicity: Student's ethnicity group (categorical).
- Parental Level of Education: Highest education level attained by parents.
- Lunch: Type of lunch provided (standard or free/reduced).
- Test Preparation Course: Completion status of test preparation course (Yes/No).
- Scores: Numeric scores in Math, Reading, and Writing.

#### Target Variable:
- Student performance in test scores.

#### Source
- Dataset Source - https://www.kaggle.com/datasets/spscientist/students-performance-in-exams?datasetId=74977
- The data consists of 8 column and 1000 rows.

### 3. Project Workflow
The project follows the typical machine learning workflow:
#### 1.Exploratory Data Analysis (EDA):
The graph below shows the distribution of Average_score with Gender
##### Average Score Distribution
The histogram below illustrates the following things:
- From the first plot:
- Overall performance trends (e.g., most students score around a particular range, or scores are skewed toward higher or lower ends).
- Whether the average scores follow a specific distribution (e.g., normal or skewed).
- From the second plot:
- Gender-based differences in performance.
- Whether one gender scores consistently higher or lower on average.
- The overlap in score distributions, indicating the similarity or disparity in performance.
![Average_Score_Distribution](Images.png/Average_Score_Distribution.png)
##### Total Score Distribution
- The first plot shows the overall performance trend, while the second plot highlights potential gender-based differences in total_score.
- If gender curves largely overlap, performance is similar across genders. If distinct, one gender outperforms the other consistently.
![Total_Score_Distribution](Images.png/Total_Score_Distribution.png)
##### Effects of Lunch Type  on Student
- Standard lunch positively impacts performance for both genders, but the magnitude of its effect may vary.
- Females might show a stronger correlation between lunch type and scores compared to males.
- Lunch type is a potential socio-economic indicator affecting academic outcomes.
![Type of Lunch](Images.png/Lunch_Variation.png)
##### Effects of Parental_Level_Of_Education on Student Performance
- Parental education significantly correlates with student performance, regardless of gender.
- In general parent's education don't help student perform well in exam.
- 2nd plot shows that parent's whose education is of associate's degree or master's degree their male child tend to perform well in exam
- 3rd plot we can see there is no effect of parent's education on female students.
![Effects Of Parental Level Education](Images.png//Parental_level_of_education_variation.png)
#####  Maximumum score of students in all three subjects
- From the above three plots its clearly visible that most of the students score in between 60-80 in Maths whereas in reading and writing most of them score from 50-80.
- Symmetry indicates consistent performance, while skewness or wider tails indicate variability.
- Compare the width and shape of each violin to see which subject has the most variability or outliers.
- Subjects with a narrow, centered violin suggest more uniform student performance.
![Max Score in all Subjects ](Images.png/Max_score.png)
#####  Multivariate analysis using Pieplot 
- Number of Male and Female students is almost equal.
- Number students are greatest in Group C.
- Number of students who have standard lunch are greater.
- Number of students who have not enrolled in any test preparation course is greater.
- Number of students whose parental education is "Some College" is greater followed closely by "Associate's Degree".
![Multivariate Analysis On all features ](Images.png/Multivariate_analysis.png)
##### Feature Wise Visualization
###### GENDER COLUMN
- How is distribution of Gender ?
- Is gender has any impact on student's performance ?
###### UNIVARIATE ANALYSIS ( How is distribution of Gender ? )
- Gender has balanced data with female students are 518 (48%) and male students are 482 (52%).
- The dataset shows the gender distribution in terms of both absolute counts and percentages.
- A balanced distribution ensures fair analysis across genders, while an imbalance might require careful interpretation to avoid bias in conclusions.
![Univariate Analysis On Gender ](Images.png/Gender_distribution.png)
##### Bivariate Analysis (Does gender has any impact on student's performance ?)
- This visualization highlights gender-based differences in overall academic performance and in math.
- The comparison allows us to assess if one gender performs better in math relative to overall scores or if other subjects influence performance.
- On an average females have a better overall score than men, whereas males have scored higher in Maths.
![Bivariate Analysis On Gender ](Images.png/Bivariate_analysis.png)
##### RACE/EHNICITY COLUMN
- How is Group wise distribution ?
- Is Race/Ehnicity has any impact on student's performance ?
##### UNIVARIATE ANALYSIS ( How is Group wise distribution ?)
Race/Ethnicity representation in the dataset is displayed, with certain groups dominating the dataset.
This breakdown is important to assess potential biases or over-representation of a particular group, which can impact the overall analysis and conclusions.
- Most of the student belonging from group C /group D.
- Lowest number of students belong to groupA.
![Univariate Analysis On Race_Ethinicity ](Images.png/Race_ethinicity_Distribution.png)
##### BIVARIATE ANALYSIS ( Is Race/Ehnicity has any impact on student's performance ? )
- Group E students have scored the highest marks. 
- Group A students have scored the lowest marks. 
- Students from a lower Socioeconomic status have a lower avg in all course subjects.
![Bivariate Analysis On Race_Ethinicity ](Images.png/Bivariate_Anlaysis_Ethinicity.png)
##### PARENTAL LEVEL OF EDUCATION COLUMN 
- What is educational background of student's parent ?
- Is parental education has any impact on student's performance ?
##### UNIVARIATE ANALYSIS ( What is educational background of student's parent ? )
- The dataset shows a skew towards lower parental education levels (such as High School), with fewer students coming from families with higher education levels.
- This information is useful for understanding the socioeconomic background and potential influence on student performance
- Largest number of parents are from some college.
![Univariate Analysis On Parental_Level_Of_Education ](Images.png/Parental_level_of_education.png)
##### LUNCH COLUMN 
- Which type of lunch is most common amoung students ?
- What is the effect of lunch type on test results?
##### UNIVARIATE ANALYSIS ( Which type of lunch is most common amoung students ? )
###### Lunch Type Distribution:
- The countplot shows the distribution of students based on the type of lunch they receive: Standard vs Free/Reduced.
- Each bar represents the count of students for each lunch type.
###### Key Observations:
- If the Standard lunch bar is significantly taller than the Free/Reduced lunch bar, it indicates that most students receive standard lunch.
- A smaller count of students receiving Free/Reduced lunch may suggest socio-economic factors influencing lunch eligibility.
- Students being served Standard lunch was more than free lunch
![Univariate Analysis Lunch type  ](Images.png/Lunch_type_comparison.png)
##### BIVARIATE ANALYSIS (  Is lunch type intake has any impact on student's performance ? )
- Students who get Standard Lunch tend to perform better than students who got free/reduced lunch.
- The visualizations suggest a potential link between parental education and both test preparation course completion and lunch type.
- Higher parental education is associated with higher test prep course completion and access to standard lunch, which may reflect broader socioeconomic factors that influence student resources and opportunities
![Bivariate Analysis Lunch type ](Images.png/Bivariate_analysis_Lunch.png)
##### 4.4.5 TEST PREPARATION COURSE COLUMN 
- Which type of lunch is most common among students ?
- Is Test prepration course has any impact on student's performance ?
##### BIVARIATE ANALYSIS ( Is Test prepration course has any impact on student's performance ? )4
- Lunch type and test preparation course completion significantly impact performance, with Standard lunch and course completion leading to better scores in all subjects.
- These insights highlight the importance of nutrition and structured preparation in improving academic outcomes.
![Bivariate Analysis Test Preparation Course Column ](images/test_preparation_course on student performance.png)
![Bivariate Analysis of Test_Preparation_course ](Images.png/Bivariate_Analysis_test_pre.png)
##### Multivariate Anaysis Based on Gender Using Pairplot 
###### Correlation Analysis:
- You can observe how two numerical variables (e.g., math_score vs. reading_score)  - relate to each other. If there's a linear relationship, it might indicate correlation.
Group Differentiation:
- By setting hue='gender', the scatterplots will distinguish between male and female data points using different colors, helping to identify potential differences in distributions or relationships.
###### Univariate Analysis:
- The diagonal of the pairplot contains histograms or KDE plots for each numerical variable, showing their individual distributions.
###### Multivariate Interactions:
- It visually highlights how one variable interacts with others across different genders.
#### 2.Data Preprocessing:
- Handle missing values and outliers.
##### Quick Insights from the Boxplots:
###### Overall Score Distribution:
- Each boxplot visualizes the distribution of scores for Math, Reading, Writing, and the Average.
- The boxes represent the interquartile range (IQR), while the whiskers show the range of most scores.
###### Key Observations:
- Median Scores: The median (line inside each box) for all subjects appears similar, suggesting balanced performance across subjects.
- Outliers: There may be outliers (dots outside the whiskers) in some subjects, indicating a few students with significantly lower or higher scores.
- Spread of Scores: Math scores may have a narrower spread, while other subjects like reading and writing may have a wider range.
- Encode categorical variables We have 5 categorical features :('Gender',  'Race_Ethnicity', 'Parental_Level_Of_Education', 'Lunch', 'Test_Preparation_Course')
- Normalize numerical features.
![Checking Outliers ](Images.png/Outliers.png)
#### 3.Feature Engineering:
- Analyze feature importance.
-
#### 4.Model Performance:
- Best_performing model: 
#### Linear Regression
- Model performance for Training set
- Root Mean Squared Error: 5.3293
- Mean Absolute Error: 4.2715
- R2 Score: 0.8740
----------------------------------
- Model performance for Test set
- Root Mean Squared Error: 5.4252
- Mean Absolute Error: 4.2222
- R2 Score: 0.8790

#### Lasso
- Model performance for Training set
- Root Mean Squared Error: 6.5938
- Mean Absolute Error: 5.2063
- R2 Score: 0.8071
----------------------------------
- Model performance for Test set
- Root Mean Squared Error: 6.5197
- Mean Absolute Error: 5.1579
- R2 Score: 0.8253
----------------------------------
#### 5. Insights and Interpretation:
Some of the Key Findings from :
- Student's Performance is related with lunch, race, parental level education.
- Females lead in pass percentage and also are top-scorers.
- Student's Performance is not much related with test preparation course.
- Finishing preparation course is beneficial.


#### 6. Installation and Usage
##### Prerequisites
- Python 3.x
- Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn

##### Clone the repository:
- git clone https://github.com/Harddik1611/mlproject.git
- cd student-performance-indicator
- Install required dependencies:
pip install -r requirements.txt
- Run the project script or Jupyter Notebook:
jupyter notebook Student_Performance_Indicator.ipynb

#### 7. Future Enhancements
- Incorporate additional socio-economic or behavioral data to improve predictions.
- Experiment with advanced models like XGBoost or Neural Networks.
- Deploy the model using a web-based application for educators to input data and predict scores.
#### 8. Contribution
Contributions are welcome!
- Fork the repository.
- Create a feature branch.
- Submit a pull request with a clear description of the changes.