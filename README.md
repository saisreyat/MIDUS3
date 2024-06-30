# MIDUS3
**Project Name**: Summary of Data Analysis Tasks
**Overview**
This repository documents the data analysis tasks performed on multiple datasets related to cognitive and health variables. The project involves data loading, cleaning, merging, and analysis to derive insights into the relationship between physical activity, cognition, and various health outcomes.

**Tasks Completed**

**Data Loading and Conversion**

TSV files ('36346-0001-Data.tsv', '36346-0002-Data.tsv', '36346-0003-Data.tsv', '38837-0001-Data.tsv', '38837-0002-Data.tsv') were read into DataFrames using pandas.
Converted DataFrames to CSV format for easier handling and saved as separate files ('midus1_df.csv', 'midus2_df.csv', 'midus3_df.csv', 'biomarker1_df.csv', 'biomarker2_df.csv').

**Data Selection**

Selected relevant variables from each dataset ('midus1_selected', 'midus2_selected', 'midus3_selected', 'biomarker1_selected', 'biomarker2_selected').

**Data Merging**

Merged selected datasets based on the 'M2ID' column using pandas merge() function into 'merged_data'.

**Data Cleaning**

Handled missing values by forward-filling with 'ffill' option and dropped rows with remaining missing values using dropna().
Removed duplicate rows using drop_duplicates().
Saved cleaned dataset as 'cleaned_dataset.csv'.
Duplicate Column Removal
Identified and removed duplicate columns from cleaned dataset using duplicated() method.
Saved dataset without duplicate columns as 'cleaned_dataset_no_duplicates.csv'.

**Column Renaming**

Created 'column_mapping' dictionary to rename columns to more descriptive names.
Renamed columns using rename() method and 'column_mapping' dictionary.
Saved dataset with renamed columns as 'cleaned_dataset_renamed.csv'.

**Identifying Unmapped Columns**

Identified columns in cleaned dataset not mapped in 'column_mapping' for further investigation.
Extracting Specific Columns
Extracted subset of columns based on specific requirements ('C4WR3ASB', 'M2FAMNUM', 'SAMPLMAJ').
Saved extracted dataset as 'extracted_dataset.csv'.

**Final Dataset Creation**

Created final dataset 'final_dataset' with variables: phy_act_vars, cognition_vars, cvd_vars, loneliness_vars.

**Statistical Analysis**

Identified timepoints of physical activity and cognition variables to analyze their impact on population outcomes.
Calculated composite scores (CESD, PSS, MASQ) for cognition variables.
Conducted correlation analysis using Spearman correlation due to non-normal data distribution.
Tested normality using Shapiro-Wilk test, calculated p-values, correlation coefficients, and sample sizes.
Combined leisure time physical activity variables and analyzed correlations with cognitive and outcome variables.

**Next Steps**

Continue refining analysis with additional statistical tests and visualization techniques.
Expand dataset exploration to uncover further insights into relationships between variables.
Document and publish findings in a comprehensive report or presentation.
