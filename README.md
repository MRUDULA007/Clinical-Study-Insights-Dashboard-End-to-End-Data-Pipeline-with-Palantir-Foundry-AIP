# Clinical Study Insights: End-to-End Data Pipeline & Analysis

### 🎯 Project Overview
This project explores the correlation between patient demographics and adverse events associated with drug consumption during a clinical study. The primary challenge addressed is the reconciliation of unstructured clinical documents (PDFs) with structured demographic databases. 

By leveraging **Palantir Foundry** and the **Artificial Intelligence Platform (AIP)**, I built an end-to-end data pipeline that automatically extracts insights from raw text using Large Language Models (LLMs), processes the data, and feeds it into a Jupyter-based analytical environment for exploration and deployment.

### 🛠️ Tech Stack
* **Enterprise Platform:** Palantir Foundry, Palantir AIP
* **Data Engineering:** Foundry Pipeline Builder
* **AI/LLM Integration:** AIP Logic (for unstructured PDF parsing)
* **Data Science & Analytics:** Python, JupyterLab, Pandas, Matplotlib/Seaborn
* **Deployment:** Streamlit (Interactive Application)

---

### 🚀 What I Did: The Workflow

#### 1. Data Ingestion & Integration
The project began with importing two distinct data sources into the Foundry ecosystem: structured tabular data containing patient demographics and unstructured PDF documents containing clinical study logs and adverse event reports.

![Raw Datasets](https://github.com/MRUDULA007/Clinical-Study-Insights-Dashboard-End-to-End-Data-Pipeline-with-Palantir-Foundry-AIP/blob/9e5b47e87f9c93183ff52984fc84ea5768de8e31/AE_AdverseEvents_rawdatasest.png)

![Raw Datasets](https://github.com/MRUDULA007/Clinical-Study-Insights-Dashboard-End-to-End-Data-Pipeline-with-Palantir-Foundry-AIP/blob/9e5b47e87f9c93183ff52984fc84ea5768de8e31/DM_Demographics_rawdataset.png)


*Raw tabular demographic data and unstructured clinical study PDFs ingested into Foundry.*

#### 2. AI-Driven Data Engineering (Pipeline Builder & AIP)
To make the unstructured PDF data usable, I engineered a data pipeline using Foundry's Pipeline Builder. I integrated Palantir's AIP to prompt an LLM to read the raw PDF text, extract the relevant adverse events, and structure them into a tabular format. I then joined this newly structured dataset with the existing patient demographic tables.

![Pipeline Architecture](https://github.com/MRUDULA007/Clinical-Study-Insights-Dashboard-End-to-End-Data-Pipeline-with-Palantir-Foundry-AIP/blob/9e5b47e87f9c93183ff52984fc84ea5768de8e31/PipeLine_Architecture.png)
*Visual pipeline architecture demonstrating the LLM-powered extraction and data join.*

#### 3. Exploratory Data Analysis (JupyterLab)
With the fully structured and joined dataset ready, I transitioned into a Foundry-hosted JupyterLab environment. Using Python, I conducted exploratory data analysis to identify trends, frequencies, and distributions of adverse events across different patient cohorts.

![Jupyter Analysis](https://github.com/MRUDULA007/Clinical-Study-Insights-Dashboard-End-to-End-Data-Pipeline-with-Palantir-Foundry-AIP/blob/9e5b47e87f9c93183ff52984fc84ea5768de8e31/Jupyter_AgeDistributionbyArm.png)

![Jupyter Analysis](https://github.com/MRUDULA007/Clinical-Study-Insights-Dashboard-End-to-End-Data-Pipeline-with-Palantir-Foundry-AIP/blob/9e5b47e87f9c93183ff52984fc84ea5768de8e31/Jupyter_AgeDistributionbyAdverseEventCatergory.png)

*Statistical analysis and data visualization executed in JupyterLab using Python.*

#### 4. Interactive Dashboard Deployment
To make the findings accessible to non-technical stakeholders, I wrapped the analytical logic into a Streamlit application. This web app allows users to interactively filter patient demographics and view the associated risks and adverse event occurrences in real-time.

*The final production-ready Streamlit dashboard for stakeholder consumption.*

![Streamlit Dashboard](https://github.com/MRUDULA007/Clinical-Study-Insights-Dashboard-End-to-End-Data-Pipeline-with-Palantir-Foundry-AIP/blob/9e5b47e87f9c93183ff52984fc84ea5768de8e31/Streamlit%20App.png)

![Streamlit Dashboard](https://github.com/MRUDULA007/Clinical-Study-Insights-Dashboard-End-to-End-Data-Pipeline-with-Palantir-Foundry-AIP/blob/9e5b47e87f9c93183ff52984fc84ea5768de8e31/streamlit_vomiting.png)

![Streamlit Dashboard](https://github.com/MRUDULA007/Clinical-Study-Insights-Dashboard-End-to-End-Data-Pipeline-with-Palantir-Foundry-AIP/blob/9e5b47e87f9c93183ff52984fc84ea5768de8e31/streamlit_nausea.png)

![Streamlit Dashboard](https://github.com/MRUDULA007/Clinical-Study-Insights-Dashboard-End-to-End-Data-Pipeline-with-Palantir-Foundry-AIP/blob/9e5b47e87f9c93183ff52984fc84ea5768de8e31/streamlit_decappetite.png)

![Streamlit Dashboard](https://github.com/MRUDULA007/Clinical-Study-Insights-Dashboard-End-to-End-Data-Pipeline-with-Palantir-Foundry-AIP/blob/9e5b47e87f9c93183ff52984fc84ea5768de8e31/streamlit_anxiety.png)


#### 5. Data Lineage & Governance
A critical component of enterprise data science is trust. I established and verified the complete data lineage, ensuring that every data point in the final Streamlit application can be traced back through the Jupyter transformations, the AIP extractions, and ultimately to the raw source files.

![Data Lineage](https://github.com/MRUDULA007/Clinical-Study-Insights-Dashboard-End-to-End-Data-Pipeline-with-Palantir-Foundry-AIP/blob/9e5b47e87f9c93183ff52984fc84ea5768de8e31/dataLineage.png)
*Complete data lineage tracking the flow from raw inputs to the published application.*

---

### 📊 Key Insights & Findings

Based on the interactive dashboard and exploratory data analysis, several key patterns emerged regarding patient demographics and drug side effects:

* **Study Arm Distribution:** The "Miracle Drug 10 mg" arm accounts for the vast majority of the recorded data and adverse events, significantly outnumbering the Placebo group. The patient age distribution for the active drug arm is heavily concentrated in the 55–65 age range.
* **Age-Specific Event Correlations:** Different adverse events show distinct age-related patterns:
  * **Decreased Appetite:** Exhibits a sharp, isolated spike in occurrences for patients around 60 years of age.
  * **Anxiety:** Displays a much broader, multi-modal distribution, prominently affecting younger demographics (late 20s to early 30s) as well as older cohorts (60s and 80s).
  * **Nausea & Vomiting:** These events are primarily clustered among middle-aged patients, specifically within the 40–60 age brackets.
* **AI-Extracted Qualitative Sentiment:** By leveraging LLMs to parse unstructured patient feedback, the dashboard reveals that despite experiencing adverse events of varying severities (from "mild vomiting" to "severe nausea"), patients frequently expressed positive sentiment regarding the study's organization and the attentiveness of the clinical staff.

### 💡 Future Work
* **Predictive Modeling:** Train a machine learning model using `scikit-learn` in Jupyter to predict the probability of a patient experiencing an adverse event based on their demographic profile.
* **Pipeline Automation:** Set up automated build schedules in Foundry so the dashboard updates dynamically as new clinical PDFs are uploaded.



<br>
<br>
<br>
<br><br>
<br>
Acknowledgements: This project was developed as part of the Palantir course. The datasets used are notional and provided by Palantir for educational purposes to demonstrate enterprise-grade data engineering, AI integration, and analytical workflows within the Foundry ecosystem.
