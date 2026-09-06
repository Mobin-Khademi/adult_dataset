```markdown
# Adult Dataset Analysis

Analysis and preprocessing of the **Adult (Census Income)** dataset from the UCI Machine Learning Repository.

This project includes:
- Exploratory Data Analysis (EDA)
- Data cleaning and preprocessing
- Encoding of categorical and numerical features
- Association Rule Mining

---

## Project Structure


adult_dataset/
├── data/
│   └── adult.csv                 # Original dataset
├── dist/
│   ├── adult_preprocessed.csv    # Preprocessed dataset
│   ├── frequent_itemsets.txt     # Frequent itemsets
│   └── rules.txt                 # Association rules
├── src/
│   ├── explore.ipynb             # Exploratory Data Analysis
│   ├── Preprocessing.ipynb       # Data preprocessing & encoding
│   └── association_analysis.ipynb # Association rule mining
└── requirements.txt


```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Mobin-Khademi/adult_dataset.git
cd adult_dataset
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the notebooks:
```bash
jupyter notebook
```

---

## Workflow

### 1. Exploratory Data Analysis (`explore.ipynb`)
- Feature distribution analysis
- Missing value detection
- Basic statistical summaries

### 2. Preprocessing (`Preprocessing.ipynb`)
- Replace missing values (`?`) with the mode of each column
- Group rare countries into an `others` category
- Binary encoding of nominal features (manual one-hot encoding)
- Binning of numerical features:
  - `age` → 12 bins (equal frequency)
  - `education-num` → 8 bins (equal width)
  - `hours-per-week` → 5 bins (equal width)
  - `capital-gain` and `capital-loss` → custom bins
- Drop the `fnlwgt` column

### 3. Association Analysis (`association_analysis.ipynb`)
- Extract frequent itemsets using `mlxtend`
- Generate association rules
- Save results in the `dist/` folder

---

## Requirements

- pandas
- numpy
- matplotlib
- scikit-learn
- mlxtend
- jupyter

---

## Dataset Source

Adult dataset from UCI Machine Learning Repository:  
[https://archive.ics.uci.edu/ml/datasets/Adult](https://archive.ics.uci.edu/ml/datasets/Adult)

---

## Author

**Mobin Khademi**  
GitHub: [Mobin-Khademi](https://github.com/Mobin-Khademi)
```
