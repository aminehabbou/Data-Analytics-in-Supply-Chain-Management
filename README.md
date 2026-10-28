<div align="center">

# 🚢 Data Analytics in Supply Chain Management

### Analytics in 

**How can data help us understand dispatch decisions, demand patterns, and inventory operations, and energy consumption across different supply chain scenarios?**

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white" alt="Jupyter">
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/NumPy-Numerical%20Computing-013243?logo=numpy&logoColor=white" alt="NumPy">
  <img src="https://img.shields.io/badge/Plotly-Interactive%20Visualization-3F4F75?logo=plotly&logoColor=white" alt="Plotly">
  <img src="https://img.shields.io/badge/SciPy-Scientific%20Computing-8CAAE6?logo=scipy&logoColor=white" alt="SciPy">
  <img src="https://img.shields.io/badge/ResearchPy-Statistical%20Analysis-4051B5" alt="ResearchPy">
</p>

<p>
  <img src="https://img.shields.io/badge/Focus-Exploratory%20Data%20Analysis-2E8B57" alt="Exploratory Data Analysis">
  <img src="https://img.shields.io/badge/Domain-Supply%20Chain%20Management-6A5ACD" alt="Supply Chain Management">
  <img src="https://img.shields.io/badge/Data-Not%20Committed%20to%20Git-orange" alt="Data not committed">
  <img src="https://img.shields.io/badge/Status-Research%20%26%20Development-blue" alt="Research and development">
</p>

</div>

---

## 🔎 Project Overview

**Data Analytics in Supply Chain Management** is an evolving analytics project that applies a consistent, question-led exploratory data analysis (EDA) workflow to different supply chain scenarios. The objective is to understand each dataset, identify data-quality issues, explore operational patterns, and develop evidence-based hypotheses that can inform future predictive or prescriptive modelling.

The repository currently covers two primary scenarios—**port logistics dispatching** and **retail inventory and sales**—along with a reusable logistics classification EDA template.

Rather than treating visualization as an end in itself, the notebooks connect statistical and visual exploration to operational questions. They document assumptions, include feature context where available, and use checkpoints to encourage interpretation before modelling.

## 🎯 Scenarios Under Investigation

### 🚛 1. Port Logistics Dispatching

Imagine a port-logistics control tower where dispatchers must make decisions while traffic, terminal conditions, incidents, transport availability, and time constraints evolve.

The notebook explores operational features and their relationship with the recommended dispatch action.

**Areas of investigation**

- Terminal and road incidents, congestion, and weather conditions
- Terminal, corridor, vehicle, and transport-object characteristics
- Operational constraints such as slots, customs, and driver or vehicle availability where represented in the data
- Missing values, duplicates, variable distributions, and data consistency
- Relationships between operational conditions and `Recommended_Dispatch_Action`
- Domain-informed brainstorming and hypotheses for future feature engineering and classification

**Notebook:** [`EDA_Port_Logistics_Dispatching.ipynb`](src/EDA_Port_Logistics_Dispatching.ipynb)

### 🏪 2. Retail Inventory & Sales

This scenario investigates daily store–product observations to understand demand and the operational context surrounding sales and inventory. The notebook uses **`Units Sold`** as its regression target.

The dataset described in the notebook contains **73,100 rows and 15 columns**, with observations spanning **1 January 2022 to 1 January 2024**.

**Areas of investigation**

- Sales distributions across stores, products, categories, regions, and dates
- Inventory levels, units ordered, prices, discounts, and promotions
- Weather and calendar-related patterns where available
- Numerical and categorical relationships, including chi-square tests and Cramér’s V
- Data-quality checks and target-focused exploration
- Potential data leakage and the availability of features at prediction time

**Notebook:** [`EDA_Retail_Inventory_sales.ipynb`](src/EDA_Retail_Inventory_sales.ipynb)

> **Modelling caution:** The notebook is an EDA workflow, not a trained forecasting model. Features such as `Demand Forecast` or `Units Ordered` must be assessed carefully before modelling. Their suitability depends on when and how they were generated and whether they would be available at the intended prediction time.

### 📦 3. Logistics Classification — Reusable EDA Template

A configurable EDA notebook intended to be adapted to logistics classification datasets. It includes dataset and column-role settings, reusable loading logic, numerical and categorical analysis, and interactive visualizations.

**Notebook:** [`EDA_Classification_Logistics.ipynb`](src/EDA_Classification_Logistics.ipynb)

---

## 🧪 Analytical Workflow

The notebooks follow a structured workflow, adapted to each scenario:

```text
Configure dataset and analysis settings
                 │
                 ▼
         Load and inspect data
                 │
                 ▼
      Understand shape and variables
                 │
                 ▼
        Assess data quality
     (missing values, duplicates,
      types and unusual values)
                 │
                 ▼
       Univariate exploration
    (distributions and frequencies)
                 │
                 ▼
       Multivariate exploration
 (relationships, group comparisons,
      correlations and associations)
                 │
                 ▼
      Interpret and brainstorm
                 │
                 ▼
     Summarize findings, caveats,
       and next modelling steps
```

The notebooks use interactive charts where useful. Hover over points to inspect values, drag to zoom, double-click to reset the view, and click legend entries to show or hide groups.

### 🔬 Methods and analysis techniques

- **Data profiling:** dimensions, data types, descriptive statistics, and completeness.
- **Data-quality checks:** missing values, duplicate records, and potentially inconsistent values.
- **Univariate analysis:** numerical distributions and categorical frequencies.
- **Multivariate analysis:** scatter plots, grouped comparisons, correlation heatmaps, and pairwise views.
- **Statistical association:** chi-square tests and Cramér’s V for categorical variables where applicable.
- **Distribution diagnostics:** kernel density estimation and z-scores where appropriate.
- **Hypothesis development:** translating observed patterns into questions for further validation.
- **Student checkpoints:** structured pauses for interpretation and domain reasoning.

These methods support exploration. They do not, by themselves, establish causation or demonstrate that a predictive model will perform well.

## 🛠️ Technology Stack

### Core language and data analysis

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white" alt="NumPy">
</p>

| Technology | Role |
|---|---|
| **Python** | Core language for the analysis workflows |
| **Pandas** | Tabular data loading, manipulation, summaries, and data-quality checks |
| **NumPy** | Numerical operations and array-based computation |
| **Jupyter Notebook / IPython** | Interactive analysis, explanatory markdown, code execution, and rich notebook output |

### Visualization and statistical analysis

<p>
  <img src="https://img.shields.io/badge/Plotly-Interactive%20Charts-3F4F75?logo=plotly&logoColor=white" alt="Plotly">
  <img src="https://img.shields.io/badge/SciPy-8CAAE6?logo=scipy&logoColor=white" alt="SciPy">
  <img src="https://img.shields.io/badge/Statsmodels-Statistical%20Tools-4051B5" alt="Statsmodels">
  <img src="https://img.shields.io/badge/ResearchPy-Categorical%20Analysis-6A5ACD" alt="ResearchPy">
</p>

| Technology | Role |
|---|---|
| **Plotly Express** | Interactive statistical and exploratory charts |
| **Plotly Graph Objects** | Customized chart construction |
| **Plotly Figure Factory** | Specialized visualizations, including pairwise views where used |
| **SciPy** | Statistical utilities, kernel density estimation, z-scores, and hierarchical clustering |
| **statsmodels** | Statistical modelling utilities available in the environment |
| **ResearchPy** | Statistical summaries and categorical association analysis, including Cramér’s V workflows |
| **openpyxl** | Excel file-reading support through Pandas |
| **IPython.display** | Rich display of tables, HTML, and other notebook output |

The repository's `requirements.txt` records the Python environment's pinned package dependencies. Some entries are transitive dependencies rather than libraries imported directly by every notebook.

## 🗂️ Repository Structure

```text
Data-Analytics-in-Supply-Chain-Management/
├── src/
│   ├── EDA_Classification_Logistics.ipynb
│   ├── EDA_Port_Logistics_Dispatching.ipynb
│   └── EDA_Retail_Inventory_sales.ipynb
├── requirements.txt
├── .gitignore
└── README.md
```

### 📂 Dataset management

**Dataset files are intentionally not committed to this repository.** This keeps the Git repository focused on code and documentation, avoids unnecessary repository bloat, and allows local datasets to remain under the owner's control.

After cloning the project:

1. Obtain the relevant dataset through its permitted source or project materials.
2. Store it locally—for example, in a `data/` directory—or keep it in another local location.
3. Open the relevant notebook and update its `DATASET_PATH` setting.
4. Verify the target and optional grouping columns, then run the notebook from top to bottom.

A local layout might look like this:

```text
Data-Analytics-in-Supply-Chain-Management/
├── data/                                  # Local only; not committed
│   ├── port_logistics_dispatching.csv     # Example filename
│   └── retail_store_inventory_data.csv    # Example filename
├── src/
│   ├── EDA_Classification_Logistics.ipynb
│   ├── EDA_Port_Logistics_Dispatching.ipynb
│   └── EDA_Retail_Inventory_sales.ipynb
├── requirements.txt
├── .gitignore
└── README.md
```

The filenames above are examples of local organization, not a guarantee that the datasets are distributed with this repository. The retail notebook refers to `retail_store_inventory_data.csv`; the port-logistics notebook's configured path should be checked in the notebook before execution.

The notebooks' reusable loading logic supports **CSV/TXT, Excel, Parquet, and JSON** files. Confirm that the selected file format and read options match the dataset you have locally.

## 🚀 Getting Started

### 1. Prerequisites

- Python environment compatible with the pinned dependencies
- Git
- Jupyter Notebook, JupyterLab, or a notebook-enabled IDE
- The dataset required by the notebook you intend to run

### 2. Clone the repository

Replace the placeholders with your actual GitHub username and repository name:

```bash
git clone https://github.com/<your-username>/Data-Analytics-in-Supply-Chain-Management.git
cd Data-Analytics-in-Supply-Chain-Management
```

### 3. Create a virtual environment

**Windows PowerShell**

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

**macOS / Linux**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 4. Install dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 5. Configure your dataset

Open the notebook you want to run and locate its dataset configuration cell. Update `DATASET_PATH` to the path of your local data file. Review any target, grouping, hue, and excluded-column settings as well.

For the retail scenario, the target is `Units Sold`. For the port-logistics scenario, inspect the feature dictionary and notebook settings to confirm the configured target and available columns.

### 6. Launch Jupyter

```bash
jupyter notebook
```

Open the relevant notebook in `src/` and execute its cells in order. For the retail notebook, the documented workflow recommends **Kernel → Restart & Run All** after dependencies and paths are configured.

## 🧭 Reproducibility and Responsible Interpretation

- **Data remains local:** users are responsible for sourcing the datasets and configuring correct file paths.
- **Inspect before cleaning:** missing values, duplicates, and outliers should be interpreted in context before deciding how to handle them.
- **Avoid target leakage:** a feature should only be used for prediction if it would be available at the intended decision time.
- **Association is not causation:** visual patterns and statistical tests generate evidence and hypotheses, not causal conclusions.
- **Document assumptions:** record data versions, preprocessing decisions, and notebook configuration changes when conducting follow-up experiments.
- **Validate before modelling:** use appropriate train/test splits, time-aware validation where needed, suitable metrics, and operational context before evaluating model performance.

## 🗺️ Roadmap

- [x] Establish a reusable exploratory data analysis workflow
- [x] Explore port logistics dispatching
- [x] Explore retail inventory and sales
- [x] Include feature context and interpretation checkpoints in the scenario notebooks
- [x] Document local dataset configuration and dependency installation
- [ ] Standardize reusable preprocessing and validation utilities
- [ ] Build baseline dispatch-action classification models
- [ ] Build and evaluate retail demand-forecasting and sales regression baselines
- [ ] Explore scenario-specific operational optimization
- [ ] Add further supply chain scenarios

## 👨‍💻 Author

**Amine Habbou**  
M.Sc. Data Engineering — Constructor University  
Bremen, Germany

This repository is developed as an applied data analytics project focused on understanding operational datasets and building a foundation for scenario-specific supply chain modelling.

---

<div align="center">

**If you find this project useful, consider giving the repository a ⭐**

*From exploratory insights to data-informed supply chain decisions.*

</div>
