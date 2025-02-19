# Tata Steel Machine Failure Prediction - Exploratory Data Analysis (EDA)

![Tata Steel](https://github.com/akashmailar/Tata-Steel-Machine-Failure-Prediction/blob/main/tata_steel.jpeg)

## Project Overview

This project focuses on predicting machine failures in **Tata Steel**'s manufacturing operations using **Exploratory Data Analysis (EDA)**. The dataset contains **136,429 rows** and **14 columns**, providing valuable insights into the operational conditions of machines. The goal is to identify key factors contributing to machine failures, enabling early detection and minimizing downtime, improving safety, and reducing maintenance costs.


### Dataset Overview

The dataset includes the following columns:

- **Product ID** (String) – Unique identifier for each machine instance.
- **Type** (String) – Categorical variable indicating the product type (e.g., L, M, H).
- **Air Temperature [K]** (Float) – Temperature of the surrounding environment.
- **Process Temperature [K]** (Float) – Internal process temperature of the machine.
- **Rotational Speed [rpm]** (Integer) – Speed at which the machine operates.
- **Torque [Nm]** (Float) – Rotational force applied to the machine.
- **Tool Wear [min]** (Integer) – Cumulative wear on the machine’s tool.
- **Machine Failure** (Boolean) – Target variable (0 = No Failure, 1 = Failure).
- **TWF (Tool Wear Failure)** – Failure due to tool degradation.
- **HDF (Heat Dissipation Failure)** – Failure caused by overheating.
- **PWF (Power Failure)** – Failure due to power system issues.
- **OSF (Overstrain Failure)** – Failure caused by excessive operational strain.
- **RNF (Random Failure)** – Unclassified random failures.
- **id (Integer)** - Row numbering.


### Key Insights from EDA

1. **Distribution of Machine Failures**: The dataset shows a significant imbalance between failure and non-failure instances, with the majority of machines not failing. This imbalance requires specialized techniques like resampling or class weighting during modeling.

2. **Correlation Analysis**: Strong correlations were observed between some features, such as process temperature and air temperature. However, certain indices like TWF and RNF showed weak correlations with machine failure status.

3. **Feature Importance**: Features like rotational speed, torque, and tool wear were found to be highly predictive of machine failure. These features are indicative of the operational stress placed on the machine.

4. **Class Imbalance**: The dataset exhibits a clear class imbalance, with significantly more instances of machines not failing compared to those that failed. Techniques like SMOTE (Synthetic Minority Over-sampling Technique) may be necessary to balance the dataset.

5. **Categorical Feature Analysis**: Different types of machines showed varying failure rates, with some types being more prone to failure under specific conditions.

6. **Time-Based Analysis**: Although there is no direct time feature, tool wear data suggests temporal trends, with higher tool wear correlating with higher failure rates.


### Business Objectives

The primary business objectives of this project are:

1. **Reduce Unplanned Downtime**: Predict machine failures before they occur to enable proactive maintenance scheduling.

2. **Optimize Maintenance Costs**: Identify potential failures early to reduce emergency repairs and overall maintenance expenses.

3. **Increase Operational Efficiency**: Prevent machine failures to ensure smooth production lines and better resource utilization.

4. **Improve Safety and Quality**: Prevent accidents caused by malfunctioning equipment and maintain product quality.

5. **Enhance Decision-Making in Maintenance**: Provide actionable insights to prioritize and allocate resources effectively.

6. **Long-Term Cost Savings**: Extend the lifespan of machinery, prevent major breakdowns, and reduce downtime-related losses.


### Data Preprocessing and Cleaning

Before analysis, the dataset underwent several preprocessing steps:

- **Handling Missing Values**: The dataset was inspected for missing values, and imputation methods were used where necessary.

- **Data Type Conversion**: Columns were checked for correct data types, ensuring numerical columns were in appropriate formats.

- **Outliers Detection**: Statistical methods like IQR (Interquartile Range) and Z-scores were used to detect and handle outliers.


### Exploratory Data Analysis (EDA)

The EDA process involved:

1. **Distribution Analysis**: Examining the distribution of the target variable, "Machine failure."

2. **Correlation Analysis**: Creating a correlation matrix to examine relationships between numerical features.

3. **Feature Importance**: Identifying key features that contribute most to predicting machine failure.

4. **Class Imbalance Analysis**: Addressing the imbalance between failure and non-failure instances.

5. **Categorical Feature Analysis**: Exploring how different machine types and product IDs affect failure rates.

6. **Time-Based Analysis**: Analyzing tool wear data to identify temporal trends.


### Insights and Conclusions

The EDA highlighted the importance of continuous monitoring and predictive analytics in industrial machinery. Key findings include:

- **Predictive Features**: Tool wear, rotational speed, torque, and process temperature were found to be highly predictive of machine failure.

- **Class Imbalance**: The dataset's class imbalance requires special attention during model training.

- **Operational Failure Indices**: Features like TWF, PWF, HDF, and RNF provide additional insights into the type of failure, aiding in more precise maintenance strategies.


### GitHub Repository
You can find the complete code and analysis in the GitHub repository:

[GitHub Repository](https://github.com/akashmailar/Tata-Steel-Machine-Failure-Prediction/)


How to Use This Repository

1. **Clone the Repository**:
      ```
      git clone https://github.com/akashmailar/Tata-Steel-Machine-Failure-Prediction.git
      ```

2. **Install Dependencies**:
   
   Ensure you have the necessary Python libraries installed:
      ```
      pip install pandas numpy matplotlib seaborn
      ```

      ```
      pip install -r requirements.txt
      ```

4. **Run the Jupyter Notebook**:
   
   Open the Jupyter Notebook (`Sample_EDA_Submission_Template.ipynb`) to explore the EDA process and analysis.


### Contributing

This is an individual project, but feedback and suggestions are welcome. Feel free to open an issue or submit a pull request.


### License

This project is licensed under the MIT License.


----

**Note**: This project is part of an exploratory data analysis effort to predict machine failures in Tata Steel's manufacturing operations. The insights gained will serve as the foundation for further model development and help guide Tata Steel in enhancing its machine maintenance strategies.

----

Thank You!
