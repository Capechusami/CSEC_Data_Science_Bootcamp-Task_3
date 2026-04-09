📊 Data Science Bootcamp – Task 3

A clean, educational Python project that demonstrates data manipulation, exploration, cleaning, and analysis using Pandas, and provides detailed insights on the Titanic dataset.

🚀 Project Overview

This repository includes two main parts:

Part 1 – Custom Dataset (Foundation)
Build a dataset from scratch using dictionaries and Pandas, with custom indexing and structured columns.
Part 2 – Titanic Dataset Analysis (Applied)
Explore, clean, and analyze the Titanic dataset (train.csv) to extract meaningful insights, including survival patterns based on gender, class, and age.

The notebooks are designed to run seamlessly on Google Colab or Jupyter Notebook, with well-commented, readable, and professional code.

🗂️ Repository Structure
Task3_DataScienceBootcamp/
├── Part1_CustomDataset.ipynb      # Notebook for creating and exploring custom dataset
├── Part2_TitanicAnalysis.ipynb    # Notebook for Titanic dataset analysis
├── train.csv                      # Titanic training dataset from Kaggle
└── README.md                      # Project overview and instructions
File Guide
Part1_CustomDataset.ipynb:
Create a 5-column, 15-row dataset with a custom index
Demonstrates pd.Series and pd.DataFrame usage
Explains logic step-by-step with markdown
Part2_TitanicAnalysis.ipynb:
Explore Titanic dataset: .head(), .info(), .describe()
Clean data: fill missing values, drop unnecessary columns, remove duplicates
Analyze using groupby and filtering
Extract insights based on gender, class, and age
Step 5: Detailed survival insights with professional markdown explanations
train.csv: Titanic dataset (download from Kaggle Titanic Competition
)
🔹 Part 1: Custom Dataset

Objective: Build a small dataset from scratch and explore it.

Implementation Steps:

Define custom index labels (S1, S2, … S15)
Create a dictionary of columns: Name, Age, Department, Score, Graduated

Convert to Pandas DataFrame:

df = pd.DataFrame(data_dict, index=index_labels)

Display the dataset using:

df.head()

Outcome: A clean, structured dataset ready for further operations.

🔹 Part 2: Titanic Dataset Analysis

Objective: Explore, clean, analyze, and interpret the Titanic dataset.

Step 1: Exploration
Preview data: .head()
Check structure: .info()
Describe numeric features: .describe()
Step 2: Data Cleaning
Age: Fill missing with median
Embarked: Fill missing with mode
Cabin: Drop column
Remove duplicates
Step 3: Analysis (using groupby)
Survival by gender
Survival by class
Average age per class
Survival by age group (Child, Teen, Adult, Senior)
Step 4: Filtering
Female passengers who survived
Children who survived
1st class passengers with high survival probability
Step 5: Insights (Detailed)
┌─────────────────────────────┐
│ 1️⃣ Gender                   │
│ Females survived more than   │
│ males (Female 74% vs Male 19%)│
│ → "Women and children first" │
├─────────────────────────────┤
│ 2️⃣ Class                     │
│ 1st Class: 63%, 2nd: 47%,   │
│ 3rd: 24% → Higher class =   │
│ easier access to lifeboats   │
├─────────────────────────────┤
│ 3️⃣ Age Group                 │
│ Children <12: 60% survival,  │
│ Adult: 38%, Senior: 20%     │
│ → Children prioritized       │
├─────────────────────────────┤
│ 4️⃣ Highest Survival Combo    │
│ Female + 1st Class + Child  │
│ → Close to 100% survival    │
└─────────────────────────────┘

Key Learnings:

Gender, class, and age strongly influenced survival
Female + 1st class + child had highest survival probability
Demonstrates practical use of Pandas for data analysis and insights
⚙️ Setup Instructions
Clone the repository:
git clone https://github.com/your-username/Task3_DataScienceBootcamp.git
cd Task3_DataScienceBootcamp
Open notebooks in Google Colab or Jupyter Notebook
For Part 2 (Titanic Analysis), upload train.csv in Colab:
from google.colab import files
uploaded = files.upload()
Run notebooks in order:
Part1_CustomDataset.ipynb
Part2_TitanicAnalysis.ipynb
✅ Acceptance Criteria
 Part 1: Create DataFrame with 5 columns and 15 rows
 Part 1: Use custom index labels
 Part 2: Clean dataset (fill missing values, drop unnecessary columns)
 Part 2: Analyze survival by gender, class, and age
 Part 2: Filter specific passenger groups correctly
 Part 2: Extract insights and highest survival combination
📜 License

MIT License
