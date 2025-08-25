# ***🩺 AAMC Medical School Matriculation Trends Analysis***

*A comprehensive longitudinal study examining gender disparities in medical school matriculation, MCAT scores, and GPAs over the past 20 years using official AAMC data.*

## ***Project Overview***

*This research project analyzes 20 years of AAMC (Association of American Medical Colleges) data to investigate changing trends in medical school matriculation patterns between male and female students. Through statistical analysis and predictive modeling, we examine how the number of matriculants and their academic credentials have evolved from 2005-2025.*

### ***Research Question***

***"To what extent have the number of matriculants and their MCAT scores/GPAs changed over the past 20 years? How do these changes compare between females and males?"***

### ***Key Hypotheses***

* ***Null:** No significant differences exist in yearly changes of matriculant numbers, MCAT scores, and GPAs between females and males*  
* ***Alternative:** Significant differences exist in these metrics between gender groups over time*

## ***Technologies Used***

* ***Python 3.x***  
* ***Data Analysis:** pandas, numpy*  
* ***Visualization:** matplotlib, seaborn*  
* ***Statistical Analysis:** scipy.stats, statsmodels*  
* ***Machine Learning:** scikit-learn*  
* ***Data Source:** Official AAMC FACTS Tables (2024)*  
* ***Development Environment:** Google Colab*

## ***Dataset Information***

### ***Data Sources (AAMC FACTS Tables 2024\)***

* ***Table A-21:** MCAT Scores and GPAs for Applicants by Gender (2018-2025)*  
* ***Table A-22:** MCAT Scores and GPAs for Matriculants by Gender (2018-2025)*  
* ***Table A-7.1:** Historical Matriculation Data (2005-2015)*  
* ***Table A-7.2:** Recent Matriculation Data (2015-2025)*  
* ***Table B-10:** Additional enrollment statistics*  
* ***Table 1:** Overall program statistics*

### ***Key Variables Analyzed***

* ***Matriculant Demographics:** Total numbers by gender and year*  
* ***Academic Metrics:** MCAT section scores, total MCAT scores, science/non-science GPAs*  
* ***Temporal Trends:** Year-over-year changes and long-term patterns*  
* ***Gender Categories:** Men, Women, Another Gender Identity (2023-2025)*

## ***Methodology***

### ***1\. Data Processing & Cleaning***

* ***Excel Integration:** Direct import from AAMC FACTS tables*  
* ***Data Restructuring:** Pivot operations for time-series analysis*  
* ***Missing Value Handling:** Strategic filling of categorical variables*  
* ***Data Validation:** Cross-referencing multiple tables for accuracy*

### ***2\. Exploratory Data Analysis***

* ***Trend Visualization:** 20-year longitudinal plots*  
* ***Gender Comparison:** Side-by-side analysis of male vs female trends*  
* ***Change Analysis:** Year-over-year difference calculations*  
* ***Correlation Studies:** Relationships between matriculant numbers and academic metrics*

### ***3\. Statistical Analysis***

* ***Paired T-Tests:** Comparing year-over-year changes between genders*  
* ***Correlation Analysis:** Examining relationships between variables*  
* ***Time Series Analysis:** Long-term trend identification*  
* ***Significance Testing:** P-value calculations for hypothesis testing*

### ***4\. Predictive Modeling***

* ***Linear Regression:** MCAT score predictions based on year and matriculant numbers*  
* ***Model Validation:** R² scores, MSE, and MAE calculations*  
* ***Future Projections:** 2025 predictions for academic metrics*  
* ***Gender-Specific Models:** Separate predictive models for male and female cohorts*

## ***Key Findings***

### ***Matriculation Trends (2005-2025)***

* ***Total Growth:** Medical school matriculants increased from 17,003 (2005-06) to 23,158 (2024-25)*  
* ***Gender Shift:** Women now comprise 55% of matriculants (up from 48% in 2005-06)*  
* ***Crossover Point:** Women surpassed men in matriculation around 2016-17*  
* ***Recent Stability:** Gender ratios have stabilized in recent years*

### ***Academic Performance Trends***

* ***MCAT Scores:** Both genders show consistent improvement over 20 years*  
  * *Women: 507.0 → 511.1 (+4.1 points)*  
  * *Men: 509.8 → 512.6 (+2.8 points)*  
* ***GPA Trends:** Steady increases across both groups*  
  * *Women: 3.64 → 3.80 (+0.16 points)*  
  * *Men: 3.61 → 3.78 (+0.17 points)*

### ***Statistical Significance Results***

| *Metric* | *P-Value* | *Significance* | *Interpretation* |
| ----- | ----- | ----- | ----- |
| *MCAT Changes* | *0.34* | *Not Significant* | *Similar improvement patterns between genders* |
| *GPA Changes* | *0.77* | *Not Significant* | *Consistent GPA trends across groups* |
| *Matriculant Numbers* | *0.068* | *Marginally Significant* | *Notable but not statistically significant difference* |

### ***Predictive Model Performance***

| *Model* | *R² Score* | *MSE* | *MAE* | *Target Variable* |
| ----- | ----- | ----- | ----- | ----- |
| *Women MCAT (Year Only)* | *0.92* | *0.48* | *0.52* | *MCAT Scores* |
| *Men MCAT (Year Only)* | *0.89* | *0.61* | *0.58* | *MCAT Scores* |
| *Combined Model* | *0.87* | *0.71* | *0.63* | *MCAT Scores* |

## ***Project Structure***

```
aamc-medical-school-analysis/
│
├── aamc_analysis.py                 # Main analysis script
├── README.md                        # Project documentation
├── data/
│   ├── 2024_FACTS_Table_A-21.xlsx  # Applicant scores by gender
│   ├── 2024_FACTS_Table_A-22.xlsx  # Matriculant scores by gender
│   ├── 2024_FACTS_Table_A-7.1.xlsx # Historical matriculation (2005-2015)
│   ├── 2024_FACTS_Table_A-7.2.xlsx # Recent matriculation (2015-2025)
│   └── 2024_FACTS_Table_B-10.xlsx  # Additional statistics
├── visualizations/
│   ├── matriculation_trends.png    # 20-year matriculation patterns
│   ├── academic_performance.png    # MCAT and GPA trends
│   ├── year_over_year_changes.png  # Annual change analysis
│   └── gender_comparison.png       # Comparative analysis
├── models/
│   ├── mcat_prediction_model.pkl   # Trained prediction model
│   └── model_evaluation.png        # Model performance plots
└── results/
    ├── statistical_analysis.csv    # T-test and correlation results
    └── summary_statistics.csv      # Descriptive statistics
```

## ***Getting Started***

### ***Prerequisites***

```shell
pip install pandas matplotlib numpy scipy scikit-learn statsmodels openpyxl
```

### ***Data Setup***

1. ***Download AAMC FACTS Tables:***

   * *Visit the AAMC website and download the required Excel files*  
   * *Place them in the `data/` directory*  
2. ***Configure Google Drive (if using Colab):***

```py
from google.colab import drive
drive.mount('/content/drive')
```

### ***Running the Analysis***

1. ***Clone the repository:***

```shell
git clone https://github.com/yourusername/aamc-medical-school-analysis.git
cd aamc-medical-school-analysis
```

2.   
   ***Execute the analysis:***

```shell
python aamc_analysis.py
```

3.   
   ***View results:***

   * *Statistical outputs will be printed to console*  
   * *Visualizations will be displayed/saved*  
   * *Model predictions will be generated*

## ***Key Visualizations***

### ***1\. Long-Term Matriculation Trends***

* ***20-year stacked bar chart** showing the growth in total matriculants*  
* ***Gender-separated comparison** highlighting the demographic shift*  
* ***Crossover analysis** identifying when women became the majority*

### ***2\. Academic Performance Evolution***

* ***MCAT score trajectories** for both genders over time*  
* ***GPA trend analysis** showing steady improvement patterns*  
* ***Comparative performance** between applicants vs matriculants*

### ***3\. Year-Over-Year Change Analysis***

* ***Annual difference plots** showing volatility and patterns*  
* ***Statistical significance markers** for major changes*  
* ***Correlation scatter plots** between metrics*

## ***Statistical Analysis Results***

### ***Correlation Analysis***

* ***Women Matriculants vs MCAT:** r \= 0.91 (strong positive correlation)*  
* ***Men Matriculants vs MCAT:** r \= 0.87 (strong positive correlation)*  
* ***Change Correlations:** Weak correlations between annual changes in different metrics*

### ***Hypothesis Testing Results***

*The analysis reveals that while there are observable differences in trends between male and female matriculants, most are not statistically significant at the α \= 0.05 level. However, the matriculant number changes approached significance (p \= 0.068), suggesting meaningful differences in enrollment patterns.*

## ***Key Insights & Implications***

### ***Major Findings***

1. ***Gender Parity Achievement:** Women now represent the majority of medical school matriculants*  
2. ***Academic Excellence:** Both groups show consistent improvement in MCAT scores and GPAs*  
3. ***Stable Competition:** The gap between genders in academic metrics remains minimal*  
4. ***Future Projections:** Models predict continued improvement in academic standards*

### ***Healthcare Implications***

* ***Workforce Diversity:** Increasing female representation in medicine*  
* ***Academic Standards:** Rising MCAT and GPA requirements reflect increased competition*  
* ***Systemic Changes:** Data suggests successful efforts to increase diversity in medical education*

### ***Policy Considerations***

* ***Admission Strategies:** Data supports evidence-based admission policies*  
* ***Resource Planning:** Enrollment trends inform medical school capacity planning*  
* ***Diversity Initiatives:** Quantified progress in gender representation*

## ***Future Research Directions***

### ***Potential Extensions***

* *\[ \] **Specialty Choice Analysis:** Examine gender differences in medical specialty selection*  
* *\[ \] **Geographic Trends:** Analyze regional variations in matriculation patterns*  
* *\[ \] **Socioeconomic Factors:** Incorporate family income and educational background*  
* *\[ \] **International Comparisons:** Compare US trends with global medical education data*  
* *\[ \] **Long-term Outcomes:** Follow matriculants through residency and career outcomes*

### ***Advanced Analytics***

* *\[ \] **Time Series Forecasting:** ARIMA models for more sophisticated predictions*  
* *\[ \] **Machine Learning:** Random Forest/XGBoost for multi-variable predictions*  
* *\[ \] **Causal Inference:** Identify factors driving observed changes*  
* *\[ \] **Interactive Dashboards:** Plotly/Dash visualization tools*

## ***Contributing***

*Contributions are welcome\! This project would benefit from:*

### ***Data Enhancements***

* *Additional years of historical data*  
* *International medical school data*  
* *Specialty choice information*  
* *Socioeconomic variables*

### ***Analysis Improvements***

* *Advanced statistical modeling*  
* *Causal inference techniques*  
* *Interactive visualizations*  
* *Real-time data updates*

### ***Development Setup***

1. *Fork the repository*  
2. *Create a feature branch (`git checkout -b feature/AnalysisImprovement`)*  
3. *Commit your changes (`git commit -m 'Add advanced statistical modeling'`)*  
4. *Push to the branch (`git push origin feature/AnalysisImprovement`)*  
5. *Open a Pull Request*

## ***Data Ethics & Limitations***

### ***Data Source Acknowledgment***

*All data used in this analysis comes from official AAMC FACTS Tables and is publicly available. This research is conducted for educational and analytical purposes.*

### ***Limitations***

* ***Aggregated Data:** Individual-level analysis not possible*  
* ***Gender Categories:** Limited gender identity options in historical data*  
* ***Confounding Variables:** Unable to control for all factors affecting matriculation*  
* ***Temporal Changes:** MCAT scoring changes in 2015 may affect trend analysis*

## ***References & Citations***

* *Association of American Medical Colleges. (2024). FACTS: Applicants and Matriculants Data*  
* *AAMC FACTS Tables A-21, A-22, A-7.1, A-7.2, B-10, and Table 1*  
* *Medical school admission statistics and trend analysis methodologies*

## ***Author***

***Your Name***

* *GitHub: https://github.com/abhioriganti?tab=repositories*  
* *LinkedIn: https://www.linkedin.com/in/abhishek-rithik-origanti/*  
* *Email: [origanti@umd.edu](mailto:origanti@umd.edu)*

## ***Acknowledgments***

* ***AAMC** for providing comprehensive, publicly available data*  
* ***Medical education researchers** whose methodologies informed this analysis*  
* ***Open source community** for statistical and visualization tools*  
* ***Peer reviewers** who provided feedback on methodology and interpretation*

---

***Star this repository if you found this research valuable\!***

*Contributing to evidence-based understanding of medical education trends.*

