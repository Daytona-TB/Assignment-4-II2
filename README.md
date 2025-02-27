NBA Player Statistical Analysis

**Overview**
This project analyzes NBA regular season player statistics using a dataset extracted from a ZIP file. It dynamically processes the dataset, identifies the player with the most seasons played, evaluates three-point accuracy trends, and conducts statistical analyses on field goals made and attempted.

**Class Design & Implementation**
The project is structured around procedural data processing rather than class-based object-oriented programming. However, if class design were implemented, the following classes would be useful:

**NBADataProcessor**

**Purpose:**
Handles file extraction, loading, and filtering of NBA regular season data.

**Attributes:**
zip_path: Path to the ZIP file containing the dataset.
extract_path: Path where the files will be extracted.
csv_file: Path to the detected CSV file.

**Methods:**
extract_and_find_csv(): Extracts the ZIP file and detects the CSV file automatically.
load_data(): Reads the CSV into a Pandas DataFrame.
filter_nba_regular_season(): Filters the dataset to include only NBA regular season data.

**NBAStatsAnalyzer**
Purpose: Analyzes player statistics, identifying key trends and performing computations.

**Attributes:**
player_df: Filtered DataFrame for the player with the most seasons played.

**Methods:**
identify_most_seasons_player(): Finds the player with the highest number of regular seasons played.
calculate_three_point_accuracy(): Computes three-point accuracy for each season played.
perform_regression_analysis(): Fits a linear regression model to three-point accuracy over seasons.
integrate_accuracy_trend(): Uses numerical integration to determine the average three-point accuracy over time.
interpolate_missing_seasons(): Estimates missing values for seasons without recorded data.
compute_field_goal_statistics(): Computes mean, variance, skewness, and kurtosis for field goals made and attempted.
perform_t_tests(): Conducts statistical t-tests on field goals made and attempted.

**Limitations**
Data Availability: Missing seasons for some players require interpolation.
Model Assumptions: Linear regression assumes a consistent trend in three-point accuracy, which may not hold true in all cases.
Dataset Dependency: The script relies on a specific dataset structure and may need adjustments for variations in formatting.
Performance Considerations: Large datasets may cause memory issues when processing all NBA players.

**How to Use**
Upload archive.zip to the same directory as the Jupyter Notebook.
Run the notebook to extract data, process statistics, and generate analysis results.
View the outputs for regression models, interpolated values, and statistical comparisons.
This structured approach ensures a clean, modular design, making it easy to extend or integrate additional statistical analyses.
