# Titanic EDA

Exploratory data analysis on the Titanic dataset, done as part of a Python and AI training task. The goal was to load the dataset, clean it up, and dig into what actually affected survival.

## Dataset

The data used here is the classic Titanic passenger dataset (`train.csv`), 891 rows with details like age, sex, passenger class, fare, and family info, along with whether each passenger survived.

Source: [Kaggle Titanic competition](https://www.kaggle.com/c/titanic/data)

## What's in this repo

- `titanic_eda.ipynb` — the notebook with all the analysis
- `train.csv` — the dataset used
- `README.md` — this file

## Steps taken

1. Loaded the dataset with pandas and checked its shape, structure, and summary stats.
2. Checked for missing values. Age and Embarked had some missing values, Cabin was missing for most rows.
3. Filled missing Age with the median, filled missing Embarked with the most common value, and dropped the Cabin column since it wasn't usable.
4. Looked at overall survival rate, then broke it down by gender, passenger class, age, fare, family size, and port of embarkation.
5. Added a new FamilySize feature (SibSp + Parch + 1) to see if traveling with family affected survival.
6. Plotted everything using matplotlib and seaborn, including a correlation heatmap for the numeric columns.

## Key findings

1. Overall survival rate was around **38%**.
2. **Gender** was the strongest factor, women survived at a much higher rate than men.
3. **Passenger class** mattered a lot, 1st class had the best survival rate, 3rd class the worst.
4. **Younger passengers**, especially children, had somewhat better survival odds.
5. Passengers who paid **higher fares** (usually 1st class) tended to survive more.
6. **Family size** small families survived more than solo travelers or very large families.

## Tools used

Python, pandas, numpy, matplotlib, seaborn, Jupyter Notebook

## Notes

This was done as a hands on practice task to build familiarity with EDA workflows and Jupyter notebooks, part of a broader Python and AI training module.
