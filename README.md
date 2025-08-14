# Electronic Sales

**Electronic Sales** is a comprehensive data analysis tool designed to streamline data exploration, analysis, and visualisation. The tool supports multiple data formats and provides an intuitive interface for both novice and expert data scientists.

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content

The name of the dataset is [**"Electronic_sales_Sep2023-Sep2024"**](https://www.kaggle.com/datasets/cameronseamons/electronic-sales-sep2023-sep2024) and contains  16 columns x 20000 records. The size of the file is 2.43MB. This dataset looks at the purchase behaviour of a customer who buys electronic products and certain factors that may influence that purchase.


## Business Requirements

The goal is to optimize electronic retail performance through data-driven insights.

Understanding how customer demographics, product categories, and sales trends impact revenue.
Also evaluating loyalty program effectiveness and upsell. Providing clear visualizations to support strategic business decisions.


## Hypothesis and how to validate?

### 1. **Using Matplotlib** 

- **Hypothesis:** Loyalty Members spend more per transaction than non-loyalty members.
    - **Validation:** Bar chart of average spending by loyalty status.
- **Hypothesis:** Certain product categories have higher revenues than others.
   - **Validation:** Bar chart of average spending per product category.
- **Hypothesis:** Sales peak in specific months.
   - **Validation:** Histogram showing monthly total revenue.

### 2. **Using Seaborn**

- **Hypothesis:** Male and Female customers differ in spending distribution.
    - **Validation:** Boxplot of spending by gender.
- **Hypothesis:** Add-on purchases are more common for higher-priced products.
   - **Validation:** Violin plot of product price by add-on purchase (Yes or No).
- **Hypothesis:** Younger customers tend to spend less than older customers. 
   - **Validation:** Swarm plot of spend by age group

### 3. **Using Plotly**

- **Hypothesis:** Loyalty members buy more add-ons than non-loyalty members.
    - **Validation:** Stacked bar chart of add-on purchases by loyalty status.
- **Hypothesis:** Certain payment methods are associated with higher average transaction value.
   - **Validation:** Bar chart of average spend per payment method.
- **Hypothesis:** High-rated products are associated with higher sales.
   - **Validation:** Scatter plot of product rating vs. total spend, with trendline. 
 

## Project Plan

* Outline the high-level steps taken for the analysis.
   - Loaded and explored a custom dataset.
   - Cleaned the data by handling missing values and standardizing categories.
   - Removed rows that should not be part of the dataset (cancelled orders).
   - Sorted and grouped data to reveal trends.
   - Visualised key metrics using bar charts, boxplots, violin plots, swarm plots etc.
   - Tested hypotheses and answered them using visualisation to validate my answer.
   - Summarised insights and suggested business actions based on findings.

* How was the data managed throughout the collection?
   - The dataset was sourced from Kaggle and downloaded as a CSV file.
   - Data integrity was maintained

* How was the data managed throughout the processing?
   - Raw data was loaded into Pandas dataframes for efficient manipulation.
   - Missing values were identified and filled with appropriate replacements.
   - Unnecessary rows were removed to ensure data quality.
   - New column was added to support deeper analysis.
   - Cleaned and processed data was saved to a new CSV file for further analysis with visualisations.

* How was the data managed throughout analysis?
   - The cleaned dataset was explored using descriptive statistics and visualisations to discover patterns and trends.
   - Data was grouped and sorted to compared key metrics across different categories.
   - Hypotheses were tested using the dataset was analysed.
   - Insights were documented and visualisations were used to support business recommendations
   - All steps were reproducible, with code in Jupyter Notebooks

* How was the data managed throughout interpretation?
   - Key findings from the analysis were summarised and interpreted in the context of business objectives
   - Insights were communicated clearly, highlighting trends, correlations and areas for improvement
   - All interpretations were documented
 
* Why did you choose the research methodologies you used?
   - Methodologies such as explortory data analysis, feature engineering, and hypothesis testing are considered standard practices for uncovering insights in data analysis.
   - Visualisation libraries such as Matplotlib, Seaborn, and Plotly were chosen because of their ability to clearly communicate trends and patterns to stakeholders in a simple way.


## The rationale to map the business requirements to the Data Visualisations

* List your business requirements and a rationale to map them to the Data Visualisations:

   - **Business requirement 1:** Optimise electronic retail performance through data-driven insights

      - **Rationale & Visualisation:** Used summary bar charts and histograms to identify overall sales trend, peak periods, and top performing products.


   - **Business requirement 2:** Understand how customer demographics, product categories, and sales trend impact revenue:

      - **Rationale & Visualisation:** Used grouped bar charts, boxplots and swarm plots to compare spending across age groups, genders and product categories.

   
   - **Business requirement 3:** Evaluate loyalty program effectiveness:
      
      - **Rationale & Visualisation:** Used stacked bar charts and violin plots to compare add-on purchases and average spending between loyalty members and non-members.


   - **Business requirement 4:** Provide clear visualisation to support strategic business decisions:

      - **Rationale & Visualisation:** Used interactive plotly charts and well-labeled Seaborn/Matplotlib plots to communicate findings making it easy to interpret for non technical audiences.


## Analysis techniques used

* List the data analysis methods used and explain limitations or alternative approaches.
   - Used descriptive statistics, grouping, an sorting to summarise and compare data
   - Used bar charts, boxplots, violin plots, swarm plots and stacked bar charts for visual analysis
   - Limitations: Data was synthetic so results don't always seem realistic

* How did you structure the data analysis techniques. Justify your response.
   - Logical sequence: Exploratory analysis, data cleaning, feature engineering, hypothesis testing and visualisation.

* Did the data limit you, and did you use an alternative approach to meet these challenges?
   - The synthetic nature of the data limited the realism of some findings
   - To manage this, i focused on cleaning, feature engineering an visual analysis to extract some meaning patterns where it was possible and made sense.

* How did you use generative AI tools to help with ideation, design thinking and code optimisation?
   - Help decide what hypotheses could be made with this dataset
   - Helped me understand what certain code meant (pipelining)

## Development Roadmap

* What challenges did you face, and what strategies were used to overcome these challenges?
   - Faced challenges with missing values, inconsistent categories and synthetic data realism
   - Applied data cleaning methods and feature engineering to improve data quality
   - Used clear interpretable visualisations to draw some meaningful correlations.

* What new skills or tools do you plan to learn next based on your project experience?
   - I definitely want to continue to learn how to use feature engineering as my use in this project was more limited than i preferred. I want to gain more knowledge about visualisation libraries as they are extremely useful when understanding data.


## Main Data Analysis Libraries
* Here you should list the libraries you used in the project and provide an example(s) of how you used these libraries.

   - **pandas:** Used for loading data, cleaning and manipulation.
      - Example: df = pd.read_csv('dataset/cleaned/Electronic_sales_cleaned.csv')

   - **numpy:** Used for numerical operations
      - Example: np.isclose(df['Total Price'], df['Quantity'] * df['Unit Price'])

   - **matplotlib:** Used for creating bar charts and histograms
      - Example: plt.bar(product_counts.index, product_counts.values)

   - **seaborn:** Used for advanced visualisations like boxplots, violin plots and swarm plots
      - Example: sns.boxplot(data=df, y='Gender', x='Grand Total')

   - **plotly:** Used for interactive charts such as stacked bar charts and scatter plots
      - Example: fig = px.bar(add_on_count, x='Loyalty Member', y='count', color='Add-ons Count')

   - feature_engine: Used for categorical imputation in data cleaning
      - Example: pipeline = Pipeline([('categorical_imputer', CategoricalImputer(...))])


## Credits 

- LMS
- Copilot

## Acknowledgements (optional)
* Thank the people who provided support through this project.
- Thank you Vasi for steering me in the right direction of how to complete this project
- Thank Roman, Mark and Neil for the valuable masterclasses.