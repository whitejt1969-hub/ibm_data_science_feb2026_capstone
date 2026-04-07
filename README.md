
In this capstone, I will predict whether the Falcon 9 first stage will land successfully. SpaceX advertises Falcon 9 rocket launches on its website at a cost of 62 million dollars, while other providers charge upwards of 165 million dollars each. Much of the savings comes from SpaceX’s ability to reuse the first stage. Therefore, if we can determine whether the first stage will land, we can estimate the cost of a launch. This information can be valuable if an alternate company wants to bid against SpaceX for a rocket launch.

Based on the data collected and prepared for modeling, the main objective is to predict whether the Falcon 9 booster will land successfully. A classification model was used to make this prediction.

Process Steps

Data Collection — Data was collected from REST APIs (SpaceX v4 endpoints). The API responded with a JSON file. Flat nested structures were transformed into a DataFrame and saved as a .csv file. Web scraping was performed with Python’s BeautifulSoup to extract HTML tables containing historical data from previous flights. From one HTML table, selected columns were identified as potential features for the classification model. Column and row data from the table were transformed into another DataFrame and saved as a .csv file.

Data Wrangling — Using Python’s pandas library, data wrangling was performed to enrich IDs via additional endpoints, filter for Falcon 9 launches, handle null values (for example, payload mass), and encode outcomes for downstream modeling.

Exploratory Data Analysis (EDA) — SQL queries and database summaries were used to explore the data. Scatter plots and bar charts were created to visualize patterns for features such as launch_site and payload_mass, as well as to identify trends over time. Correlation analysis was applied to gain further insight into the available data. One-hot encoding was also performed on key columns to create categorical fields for machine learning preparation. The work performed on the data was saved in a .csv file.

