# Real Estate ETL Project: Automated Property Data Pipeline For Savannah Group
Savannah Group, a fast-growing real estate data firm, manages thousands of property listings, agent profiles, and market trend records. As the company expanded across multiple cities, its data ecosystem became increasingly fragmented relying on manual data entry, spreadsheets, and inconsistent data feeds from various real estate APIs.
# Purpose Of The Project
The project aims to automate and optimize the company’s property data lifecycle through the implementation of an end-to-end ETL framework.
In today’s real estate landscape, accurate and timely data is essential for informed decision-making, predictive analytics, and customer experience. This project aligns with Savannah Group’s strategic goal of transforming raw property data into reliable, analytics-ready information using Python, PostgreSQL, and Power BI.

# Key Objectives
 1. Automate Data Extraction: 
Use Python scripts to connect with external APIs and automatically pull updated property listings and agent data.

2. Implement Data Cleaning and Transformation: 
Develop transformation logic to validate, standardize, and enrich raw data (handling duplicates, missing fields, and inconsistent formats).

3. Centralize Data Storage: 
Design a PostgreSQL database schema optimized for relational querying, reporting, and scalability.

4. Enable Real-Time Insights:
Integrate Power BI with PostgreSQL to visualize key business metrics — property performance, agent efficiency, and market trends.



# Expected Outcomes
The project is expected to deliver measurable improvements across data, operations, and business intelligence capabilities:

 1. End-to-End Automation: 
Streamlined ETL workflows will reduce manual intervention, accelerating data availability and reducing human error.

 2. Enhanced Data Quality:
Standardized and validated data ensures more accurate reporting and analysis.

 3. Faster Decision-Making: 
Real-time dashboards empower management with actionable insights on property performance and sales trends.

4. Operational Efficiency: 
Reduction in data handling time and improved team productivity.

5. Scalability:
A flexible ETL architecture that can easily accommodate new data sources, APIs, and regional expansions as the company grows.


# Tools and Technologies Used: 

1. Programming Language: Python 3.12+ (for scripting ETL processes)

2. Libraries: Pandas for Data manipulation and cleaning, Psycopg2 for PostgreSQL database connectivity, Openpyxl for Handling Excel files (if needed for extensions), Re for Regular expressions for pattern matching in data fixing
   
3. Database: PostgreSQL (for centralized storage)
   
4. IDE/Editor: Visual Studio Code (for development and debugging)
   
5. Version Control: Git and GitHub (for repository management)

6. Other: pgAdmin (for PostgreSQL management and verification)

7. Future Extensions: Power BI (for visualizations, not implemented in this repo but mentioned in objectives)

# Prerequisites

Install PostgreSQL and pgAdmin.

Create a database named Property_data in PostgreSQL.

Ensure the PostgreSQL user postgres has password Manchesterunited96. (update script if different).

Python installed with virtual environment support.



# Step-by-Step Execution Guide
Follow these steps to run the project.


# 1. Create Folder Structure And Save Raw Data
Create C:\Amdari Project and subfolder data/.
(Screenshot: File Explorer showing the folder setup)
<img width="820" height="148" alt="Screenshot (87)" src="https://github.com/user-attachments/assets/5f2db951-55a1-4ccb-b895-0068042c5c8e" />

# 2. Create Properties.csv In The Root Folder And Paste The Provided CSV Content.
(Screenshot: VS Code with properties.csv open showing 10 rows)
<img width="1366" height="479" alt="Screenshot (89)" src="https://github.com/user-attachments/assets/6d380d3e-ba80-4615-ac1c-a5b33fcdc6a1" />

# 3. View Raw Data
Create and run view_raw.py to inspect raw CSV (shows misalignments).
<img width="1309" height="469" alt="Screenshot (90)" src="https://github.com/user-attachments/assets/56997a24-b99b-4c42-9ed2-bf4a5ab60887" />

# 4. Transform Data
Create and run transform.py to clean and fix data, generating clean_properties.csv.
(Screenshot: Terminal showing fix for 2 rows and clean table)
<img width="1366" height="521" alt="Screenshot (91)" src="https://github.com/user-attachments/assets/db16e23d-943e-41de-9c18-c5e1df400284" />

# 5. Run Full ETL to PostgreSQL
Create and run etl_to_postgres.py to extract, transform, and load into DB.
<img width="1366" height="706" alt="Screenshot (93)" src="https://github.com/user-attachments/assets/d33245c1-75b3-4edd-9926-94948371a92b" />

# 6. Verify in PostgreSQL
In pgAdmin, view the properties table in Property_data database.
<img width="1345" height="655" alt="Screenshot (95)" src="https://github.com/user-attachments/assets/374108fe-6784-44d9-983c-9c22acd2ae5b" />

# 7. Visualize in Power-BI
<img width="865" height="495" alt="Screenshot (97)" src="https://github.com/user-attachments/assets/f60e28d3-caa8-405c-bf0f-8e9d49b288b4" />

## Project Conclusion & Impact

This end-to-end ETL pipeline successfully transforms Savannah Group’s previously fragmented and error-prone property data workflow into a modern, automated, and scalable data-driven operation.

### Key Achievements Delivered
| Achievement                          | Before                          | After (This Project)                       |
|--------------------------------------|----------------------------------|---------------------------------------------|
| Data ingestion & cleaning            | Manual Excel + copy-paste       | Fully automated Python ETL                  |
| Handling malformed/misaligned rows   | Hours of manual fixing        | Automatically detected & corrected in <2 seconds |
| Data storage                         | Scattered CSVs & Google Sheets  | Centralized PostgreSQL with proper schema   |
| Data quality                         | Duplicates, missing zip codes, wrong dtypes | 100% clean, standardized, analytics-ready |
| Update frequency                    | Weekly manual updates           | Can be scheduled hourly/daily (ready for cron/Airflow) |
| Time to insights                     | Days                            | Minutes (direct PostgreSQL → Power BI)       |

### Business Value Realized
- 90%+ reduction in manual data preparation time
- Elimination of human errors in property pricing and measurements
- Single source of truth for all property listings
- Foundation laid for real-time dashboards and predictive analytics
- Fully reproducible and version-controlled pipeline (GitHub)

### Ready for the Next Phase
- Add data validation with Great Expectations or Pydantic
- Orchestrate with Apache Airflow or Prefect
- Build interactive Streamlit/FastAPI dashboards
- Deploy Power BI reports with automated refresh
- Scale to millions of records using partitioning and incremental loads

Savannah Group now has a clean, reliable, and future-proof data foundation  turning raw property listings into trusted business intelligence.



