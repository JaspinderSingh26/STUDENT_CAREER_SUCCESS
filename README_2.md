# Student Career Success Analytics

An exploratory data analysis (EDA) project built in Python and Pandas on a dataset of 50,000 students, examining how academics, skills, and activities relate to job placement outcomes and starting salary.

## 📊 Dataset

`student_career_success_dataset.csv` — 50,000 rows, 29 columns covering:
- **Academics**: CGPA, attendance, study hours, academic performance
- **Skills**: programming, communication, teamwork, problem-solving, interview score
- **Activities**: internships, projects, certifications, hackathons, GitHub/LinkedIn presence
- **Outcomes**: placement status, placement mode, company tier, career field, starting salary

## 🔧 What this notebook does

**1. Data Cleaning**
- Checked dataset shape, structure, and summary statistics (`.shape`, `.info()`, `.describe()`)
- Checked and handled missing values with `.fillna()` — mean imputation for numeric columns (Age, CGPA, Interview Score), mode imputation for categorical columns (Gender, Placement Mode)
- Checked for duplicate records
- Standardized text values (`.str.lower()`) and inspected unique categories

**2. Outlier Detection**
- Used the IQR (Interquartile Range) method to flag CGPA and Starting Salary outliers
- Identified and reviewed unusually high/low values against student records

**3. Exploratory Analysis (Q&A style)**
A series of analytical questions answered with Pandas `groupby`/`agg`, including:
- Total students and placement rate
- Highest-enrollment and highest-paying majors
- Placement rate and average salary by major, gender, university year, and placement mode
- Internship count vs. placement rate
- Multi-level aggregations (Major × Gender, Major × Placement Mode, University Year × Major × Gender)

**4. Visualizations**
Built with Matplotlib:
- Bar chart — total starting salary by major
- Pie chart — student distribution by placement mode
- Bar chart — average employability score by major
- Line chart — starting salary trend by university year
- Pie chart — placement status distribution

## 🛠️ Tools & Libraries
- Python 3
- pandas
- matplotlib

## 🚀 How to run
1. Clone this repository
2. Install dependencies: `pip install pandas matplotlib`
3. Open `Python_Project_1.ipynb` in Jupyter Notebook (or Anaconda Navigator)
4. Update the CSV file path in the first cell to match your local path
5. Run all cells

## 📁 Files
- `Python_Project_1.ipynb` — main analysis notebook
- `student_career_success_dataset.csv` — source dataset

## 📌 Note
Some markdown insight cells in this notebook were adapted from an e-commerce dataset template — a couple of leftover captions (e.g. referencing "Electronics", "T-shirts", or "Net Banking") don't yet match the student dataset and should be rewritten before publishing (see below for corrected versions):
- Salary by major → mention the actual top major (Computer Science), not "Electronics"
- Placement mode chart → mention "Campus Placement" is most common, not "Net Banking"
- Employability score chart → mention "Artificial Intelligence" has the highest score, not "T-shirts"
- Monthly trend chart → this dataset has no date column, so "September/October" references don't apply; caption should describe the University Year trend instead
- Placement status chart → mention "Placed" vs "Not Placed" (78.08% / 21.92%), not "delivered/returned/cancelled"
