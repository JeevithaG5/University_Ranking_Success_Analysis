# University_Ranking_Success_Analysis
University Success Analytics
Overview:
The University Success Analytics project is an in-depth exploration of higher education trends, leveraging data analytics tools such as Power BI, SQL, and Excel. By integrating a structured dataset with MECE analysis and interactive Power BI visualizations, this study offers a holistic perspective on the key factors driving university success. The project aims to provide data-driven insights into rankings, demographics, and institutional performance, supporting informed decision-making in the academic sector. Interactive visualizations and dashboards help users explore university rankings, understand demographic trends, and assess institutional performance over time.
Summary:
This project delves into the complex landscape of higher education, using advanced data analytics to uncover meaningful patterns and trends. Through Power BI dashboards, SQL queries, and Excel-based analyses, the study examines university rankings, student demographics, and performance metrics across different countries and over time. By identifying key factors influencing academic excellence, the project enhances the understanding of institutional success and supports strategic decision-making in higher education.
Significance
This project is essential for stakeholders in higher education because it enables them to:
•	Monitor Key Performance Indicators (KPIs): Track metrics such as ranking scores, student-to-staff ratios, international and female student enrollment, and research outputs.
•	Analyze Global and Regional Trends: Gain insights into how universities perform across different regions and how ranking criteria evolve over time.
•	Benchmark Institutional Performance: Compare universities across various ranking systems (e.g., Times Higher Education, Shanghai Ranking, CWUR) to identify strengths and areas for improvement.
•	Drive Data-Driven Decisions: Leverage detailed visualizations and analytical insights to inform strategic planning, policy-making, and investment in higher education.
Getting Started
Prerequisites
•	Microsoft Excel (2016 or later)
•	Power BI Desktop ( for advanced interactive dashboards)
•	SQL Server or an equivalent relational database (optional, for data extraction and analysis)
•	Basic knowledge of Excel formulas, SQL queries, and Power BI visualizations.
Data Sheets Overview
The dataset is structured into six interrelated tables, each providing distinct insights:
1. Country Table
•	Purpose: Provides essential geographic context for the analysis.
•	Key Attributes:
o	ID: Unique identifier for each country.
o	Country Name: The official name of each country.
2. University Table
•	Purpose: Catalogs universities featured in global ranking systems.
•	Key Attributes:
o	ID: Unique identifier for each university.
o	Country ID: Identifier linking the university to its country.
o	University Name: Official name of the university.
3. Ranking System Table
•	Purpose: Details the distinct ranking systems used to evaluate university performance.
•	Key Attributes:
o	ID: Unique identifier for each ranking system.
o	System Name: Name of the ranking system (e.g., Times Higher Education, Shanghai Ranking, CWUR).
4. Ranking Criteria Table
•	Purpose: Lists the evaluation criteria for each ranking system.
•	Key Attributes:
o	ID: Unique identifier for each ranking criterion.
o	Ranking System ID: Links the criterion to a specific ranking system.
o	Criteria Name: Name of the ranking criterion (e.g., Research, Teaching, Citations).
5. University Year Table
•	Purpose: Provides yearly institutional metrics and student demographic data.
•	Key Attributes:
o	University ID: Unique identifier for each university.
o	Year: The year of the recorded data.
o	Number of Students: Total student enrollment.
o	Student-Staff Ratio: Indicator of faculty availability.
o	Percentage of International Students: Reflects global student mobility.
o	Percentage of Female Students: Highlights gender representation in higher education.
6. University Ranking Year Table
•	Purpose: Serves as the primary repository for ranking scores over time.
•	Key Attributes:
o	University ID: Unique identifier for each university.
o	Ranking Criteria ID: Identifier for the ranking criterion used.
o	Year: The year in which the ranking was recorded.
o	Score: The score achieved by the university based on the specified criterion.
Steps to Create the Dashboard
1. Data Preparation
•	Country & University Data: Import and clean data from the Country and University tables to ensure proper linking.
•	Ranking Data: Import ranking scores and criteria data, ensuring consistency across different ranking systems.
•	Yearly Metrics: Consolidate the University Year data to capture trends in enrollment and student-faculty ratios.
2. Loading CSV Data for SQL
•	CSV Import:
o	Open your SQL management tool (e.g., SQL Server Management Studio).
o	Use the built-in import wizard to load CSV files into corresponding SQL tables.
o	Ensure that columns match the schema described in the Data Sheets Overview.
o	For example, load the Country.csv, University.csv, etc., into your database to facilitate further SQL queries.
3. SQL Queries for KPI Extraction
•	Use SQL queries to extract key metrics such as average ranking scores, student-to-staff ratios, and demographic trends.
•	Create views or stored procedures as needed to summarize data for further analysis.
4. Importing SQL Data into Power BI
•	Connecting Power BI to SQL:
o	Open Power BI Desktop and select “Get Data” → “SQL Server.”
o	Enter your server name and database details to establish a connection.
o	Import the relevant tables or SQL views created earlier.
o	Use Power BI’s query editor to refine and model the data before building dashboards.
5. Define Key Performance Indicators (KPIs)
•	Calculate KPIs such as average ranking score, student-to-staff ratio, percentage of international and female students, and overall student enrollment.
•	Use pivot tables, formulas, and SQL queries (if applicable) to summarize these metrics.
6. Build Visualizations
•	Ranking Analysis: Create charts to compare ranking scores across systems and over time.
•	Demographic Trends: Develop visualizations to examine changes in student demographics (international, female, total enrollment).
•	Regional & Global Insights: Use map visualizations to display the distribution of universities and assess regional performance.
•	Correlation Analysis: Illustrate relationships between KPIs (e.g., ranking scores vs. student-to-staff ratios) using scatter plots and trend lines.
7. Enhance Interactivity
•	Implement slicers and filters to enable dynamic exploration of the data.
•	Create dashboards with interactive elements that allow users to drill down into specific data points (e.g., by year, country, or ranking system).
8. Finalize and Publish
•	Review the dashboards and reports for accuracy and clarity.
•	Save and publish the final Excel and Power BI files to share with stakeholders or deploy them for ongoing analysis.

Relationships Between Tables: University Ranking Dataset
The dataset is structured as a relational database, where key relationships exist between tables:
•	Country Table → University Table (One-to-Many): Each country has multiple universities.
•	University Table → University Year Table (One-to-Many): Each university has yearly demographic and student-related data.
•	Ranking System Table → Ranking Criteria Table (One-to-Many): Each ranking system has multiple criteria.
•	Ranking Criteria Table → University Ranking Table (One-to-Many): Each ranking criterion is used to assess universities.
•	University Table → University Ranking Table (One-to-Many): Each university is ranked based on different criteria.
This structured data model ensures efficient data exploration, making it easier to analyze global university performance, ranking trends, and institutional demographics.
Entity Relationship (ER) Diagram:
 
Exploratory Data Analysis: 
Problem Statement 1: How has the number of universities changed over the years in each country?
 
•	The total number of ranked universities increased steadily from 185 in 2011 to 199 in 2015 but dropped to 110 in 2016, suggesting a possible change in ranking methodology.
•	The United States dominated rankings, peaking at 77 universities in 2015 before dropping to 36 in 2016.
•	The UK maintained a steady presence (~27-30 universities per year).
•	China and South Korea have fewer ranked universities than expected given their educational investments.
•	Countries like Turkey showed growth, while others like the U.S. exhibited fluctuations.
Problem Statement 3: Is there a relationship between a country's population and the number of universities?
 
•	A weak positive correlation exists between population size and the number of ranked universities.
•	The U.S. has a disproportionately high number of universities relative to its population, while China and India have fewer despite their large populations.
Problem Statement 4: Are there any common criteria used by different ranking systems?
 
•	Each ranking system applies distinct evaluation criteria.
•	Some criteria appear similar (e.g., citations and publications), but no two ranking systems use the exact same evaluation approach.
Problem Statement 5: What is the trend in university rankings over the years according to each system?
 
•	CWUR expanded significantly from 2012 to 2015 but has missing data in 2016.
•	Shanghai Ranking remained relatively consistent with minor fluctuations.
•	THE Ranking increased until 2015 but dropped in 2016.
Problem Statement 6: How does the choice of ranking system affect a university's international student enrollment?
 
•	THE Ranking has the highest influence on international student enrollment.
•	CWUR saw a huge increase in enrollment from 2013 to 2014.
•	Shanghai Ranking remained stable with minor fluctuations.
Problem Statement 7: Are there any criteria that have different weights in different ranking systems?
 
•	No ranking system applies different weights to the same criteria; each has unique evaluation methodologies.
Problem Statement 8: How have the weights of ranking criteria changed over time?
 
•	Shanghai Ranking’s criteria were followed consistently by about 71 universities from 2005 to 2015, but none followed them in 2016.
•	THE World University followed by an average of 180 universities from 2011 to 2016.
•	CWUR saw a sudden spike in ranked universities from 2013 to 2015 but dropped in 2016.
Problem Statement 9: Is there a relationship between a university's score and the student-staff ratio?
 
•	A very weak positive correlation (0.063) suggests that student-staff ratio has minimal impact on ranking scores.
Problem Statement 10: How does the number of female students differ among universities?
 
•	Universities in Finland and Austria have higher female enrollment (~65-67%).
•	Universities in Japan, South Korea, and Norway have significantly lower female enrollment (<30%).
Problem Statement 11: What is the distribution of universities across different countries?
 
•	The U.S. has the highest number of ranked universities (273), accounting for 22% of the total.
•	China (96 universities) follows, reflecting its growing global academic influence.
•	The top 10 countries account for 68% of all ranked universities, showing dominance in specific regions.
Problem Statement 12: How has the ranking of universities changed over the years?
 
•	From 2005 to 2010, only the Shanghai Ranking was used.
•	THE Ranking emerged in 2011, covering 245 universities across 30 countries.
•	CWUR followed in 2012, with 1024 universities ranked across 59 countries.
Problem Statement 13: What is the trend in the percentage of female students over time?
 
•	Female student representation remained stable (~45%) between 2011 and 2016, with minor fluctuations.
Problem Statement 14: How has the ranking score of universities evolved over the years?
 
•	CWUR scores increased sharply from 2011 to 2014 before stabilizing.
•	Shanghai Ranking remained relatively stable with minor variations.
•	THE Ranking showed more volatility, peaking in 2015 before dropping in 2016.
Problem Statement 15: Is there a relationship between a university's ranking score and the number of students over time?
 
•	A weak negative correlation (-0.11718) suggests that an increase in student population slightly correlates with a lower ranking score.

UNIVERSITY SUCCESS ANALYSIS DASHBOARDS
COUNTRY ANALYSIS

 

UNIVERSITY ANALYSIS

 


RANKING ANALYSIS

 

YEAR ANALYSIS:

 
Key Highlights:
•	Developed interactive Power BI dashboards for year-wise, university, country, and ranking analysis, providing stakeholders with a comprehensive overview of higher education metrics.
•	Utilized SQL queries to extract and analyze data on university rankings, criteria weights, and demographic trends, offering valuable insights into the factors influencing academic performance.
•	Applied Excel-based charts and visualizations to illustrate relationships between ranking scores, student demographics, and institutional success, supporting data-driven decision-making in academia.
•	Conducted exploratory data analysis (EDA) to examine correlations between a country’s GDP, population, and university distribution, along with evolving trends in ranking scores and evaluation criteria over time.
•	The project ultimately seeks to equip higher education stakeholders with actionable insights to enhance institutional performance, inform strategic initiatives, and promote academic excellence.


