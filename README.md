# 🐞 BugRadar — Software Issue Classification & Resolution-Time Prediction

BugRadar is a machine learning and database-based project that analyzes software issue reports, classifies issues into categories, and predicts their resolution time. It combines Python, MongoDB, PyMongo, and Scikit-learn to demonstrate data preprocessing, database management, machine learning, and result visualization.

## 📌 Project Overview

Software development teams receive numerous bug reports and issue requests. Managing and prioritizing these issues manually can be time-consuming.

BugRadar aims to simplify this process through two machine learning tasks:

- **Issue Classification:** Automatically classifies software issues based on their titles and descriptions.
- **Resolution-Time Prediction:** Estimates how long a closed issue may take to resolve based on its textual information.

The project also uses MongoDB to store and manage structured and semi-structured issue data.

## 🎯 Objectives

- Analyze software issue data.
- Perform data cleaning and preprocessing.
- Store and manage issue records using MongoDB and PyMongo.
- Classify software issues using Logistic Regression.
- Predict issue resolution time using Random Forest Regression.
- Evaluate model performance using appropriate metrics.
- Visualize results and test database operations.

## 🛠️ Technologies Used

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Database | MongoDB |
| Database Connectivity | PyMongo |
| Data Processing | Pandas, NumPy |
| Machine Learning | Scikit-learn |
| Text Processing | TF-IDF Vectorization |
| Visualization | Matplotlib, Seaborn |
| Development Environment | Jupyter Notebook, VS Code |
| Version Control | Git, GitHub |

## 📂 Project Structure

```text
BugRadar/
│
├── data/
│   ├── bugradar issues og.json
│   └── bugradar_issues_cleaned.json
│
├── EDA.ipynb
├── BugRadar_MongoDB.ipynb
├── BugRadar_ML.ipynb
├── BugRadar_Results_Testing.ipynb
│
├── .gitignore
└── README.md
```

## 📊 Dataset

Important attributes include:

- `id` – Unique issue identifier
- `title` – Issue title
- `body` – Issue description
- `issue_category` – Issue category
- `priority` – Issue priority
- `state` – Issue status (open or closed)
- `created_at` – Issue creation timestamp
- `closed_at` – Issue closure timestamp
- `resolution_hours` – Time taken to resolve an issue

The dataset also contains nested information such as users, repositories, labels, assignees, and environment details.

## ⚙️ Project Workflow

1. **Data Exploration and Preprocessing:** Load the original JSON dataset, inspect its structure, handle missing values and duplicates, process timestamps, and generate a cleaned dataset.

2. **MongoDB Implementation:** Create the database and collections, insert issue records, perform CRUD operations, execute queries, and use aggregation pipelines.

3. **Machine Learning:**
   - Classification: TF-IDF + Logistic Regression.
   - Regression: TF-IDF + Random Forest Regressor.

4. **Results and Testing:** Evaluate the models, generate visualizations, test database operations, and document project limitations.


## 🗄️ MongoDB Implementation

MongoDB is used to store and manage the software issue dataset.

Database: `bugradar_db`

Collections:
- `issues_raw`
- `issues_cleaned`

Database operations include:
- Create
- Read
- Update
- Delete
- Filtering and querying
- Aggregation pipelines

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/M-anvi/BugRadar.git
cd BugRadar
```

### 2. Create a virtual environment (optional)

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install pandas numpy scikit-learn matplotlib seaborn pymongo jupyter
```

### 4. Start MongoDB

Ensure your local MongoDB server is running.

The project uses the local connection:

```text
mongodb://localhost:27017/
```

### 5. Run the notebooks

Open the project in VS Code or Jupyter Notebook and execute the notebooks in this order:

1. `EDA.ipynb`
2. `BugRadar_MongoDB.ipynb`
3. `BugRadar_ML.ipynb`
4. `BugRadar_Results_Testing.ipynb`


## ⚠️ Future Improvements

- Incorporate additional features such as priority, category, and issue complexity.
- Experiment with alternative machine learning algorithms.
- Improve regression accuracy through feature engineering and hyperparameter tuning.
- Develop a user interface for submitting issues and viewing predictions.

## 👩‍💻 Author

**Manvi**

B.Tech – Computer Science and Engineering

GitHub: [M-anvi](https://github.com/M-anvi)

---

⭐ If you find this project interesting, feel free to explore the repository!
