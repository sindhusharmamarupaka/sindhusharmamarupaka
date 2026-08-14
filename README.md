![Sindhu Marupaka](https://raw.githubusercontent.com/sindhusharmamarupaka/sindhusharmamarupaka/main/profile_banner.png)

I work with data to uncover patterns, answer business questions, and communicate insights through analysis and visualization. Most dashboards answer "what happened" — I try to build ones that also answer "so what should we do about it."

I'm drawn to public-interest data in particular — labour force surveys, railway operations, agricultural risk — because I'd rather practice on real, messy questions that affect people than polish a textbook dataset.

---

## 🔎 Currently Investigating

**India Gender Gap Analytics**

An end-to-end analysis of gender disparities in labour force participation across India, using PLFS 2023–24 data. Built as a full analytical model — star-schema data, DAX measures, drill-through dashboard — not just a chart wrapped in a dashboard shell.

<img src="https://raw.githubusercontent.com/sindhusharmamarupaka/sindhusharmamarupaka/main/badge_in_progress.png" width="140">

**Key questions driving this project:**
1. How does female LFPR vary across Indian states?
2. Which states show the largest gender gap?
3. How does participation differ between rural and urban areas?
4. Which demographic groups show the largest disparities?

---

## 📌 Case Studies

### 01 · India Gender Gap Analytics
![SQL](https://img.shields.io/badge/SQL-d64545?style=for-the-badge&logo=mysql&logoColor=white) ![Power Query](https://img.shields.io/badge/Power%20Query-e75480?style=for-the-badge&logo=powerquery&logoColor=white) ![DAX](https://img.shields.io/badge/DAX-2e8b57?style=for-the-badge) ![Power BI](https://img.shields.io/badge/Power%20BI-d4a017?style=for-the-badge&logo=powerbi&logoColor=black)

Real-world analysis of gender and labour-force participation patterns across India.

<img src="https://raw.githubusercontent.com/sindhusharmamarupaka/sindhusharmamarupaka/main/badge_in_progress.png" width="140">

---

### 02 · Indian Railways Punctuality Analysis
![SQL](https://img.shields.io/badge/SQL-d64545?style=for-the-badge&logo=mysql&logoColor=white) ![MySQL Workbench](https://img.shields.io/badge/MySQL%20Workbench-d64545?style=for-the-badge&logo=mysql&logoColor=white)

**Question**
Where does Indian Railways lose the most time — by route, station, or time of day?

**Approach**
A 5–7 level SQL query progression across a 1,900-row real delay dataset — aggregation, CASE WHEN logic, subqueries, CTEs, window functions.

**What I caught**
Rows were silently dropping during CSV import. Traced it to an encoding mismatch and fixed it with `LOAD DATA LOCAL INFILE` and explicit NULL handling.

**Delivered**
9 structured SQL files and a 210-question study bank, from raw import through reusable views.

<img src="https://raw.githubusercontent.com/sindhusharmamarupaka/sindhusharmamarupaka/main/badge_completed.png" width="140">

---

### 03 · Customer Feedback Analysis
![Python](https://img.shields.io/badge/Python-355c7d?style=for-the-badge&logo=python&logoColor=white) ![Pandas](https://img.shields.io/badge/Pandas-e75480?style=for-the-badge&logo=pandas&logoColor=white) ![HuggingFace API](https://img.shields.io/badge/HuggingFace%20API-2e8b57?style=for-the-badge&logo=huggingface&logoColor=white)

**Problem statement**
Can genuine complaint signals be reliably separated from noisy customer review text, at scale?

**Approach**
Wrangled a Kaggle clothing-reviews dataset and built a rule-based complaint filter using differential word-rate analysis, then automated response drafting via the HuggingFace Inference API.

**What I caught**
My first pass used raw keyword frequency — common words drowned out real complaints. Rebuilt it around differential word-rate analysis instead, and re-architected the email step from Gemini to HuggingFace after hitting quota limits mid-project.

**Delivered**
Shortlisted from ~25 students at Imarticus. Full pipeline — notebook, README, chart, cleaned dataset, submission package.

<img src="https://raw.githubusercontent.com/sindhusharmamarupaka/sindhusharmamarupaka/main/badge_completed.png" width="140">

---

### 04 · Accident Dataset Analysis
![Python](https://img.shields.io/badge/Python-355c7d?style=for-the-badge&logo=python&logoColor=white) ![Pandas](https://img.shields.io/badge/Pandas-e75480?style=for-the-badge&logo=pandas&logoColor=white) ![GenAI](https://img.shields.io/badge/GenAI-2e8b57?style=for-the-badge)

**Question:** Given limited safety-intervention resources, which time windows, vehicle categories, weather conditions, and locations should be prioritized to reduce accident frequency and severity?

**Approach:** Cleaned 12,316 real road traffic accident records (16 of 32 fields had missing data), engineered time-of-day features, and ran percentage-normalized comparisons to avoid volume bias skewing the results.

**What I caught:** Raw counts would have made "Normal" weather look artificially safe purely because it's the most common condition. Switching to within-category percentages revealed the opposite: Normal weather has a **1.3% fatal rate**, Rain has **1.7%** — challenging the assumption that bad weather is the bigger danger.

**Delivered:** A full case study identifying 5PM as the highest-risk accident hour, office-area traffic as the top location risk, and a GenAI-usage framework where every analytical decision was made independently — GenAI supported implementation, not interpretation.

<img src="https://raw.githubusercontent.com/sindhusharmamarupaka/sindhusharmamarupaka/main/badge_completed.png" width="140">

---

## 🧭 How I Approach Data Problems
I focus on why the analysis matters, not only on producing charts.

---

## 🛠️ Toolkit

*Click a skill badge to see the list of projects — then click a project name to open its repo.*

<details>
<summary><img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"></summary>
<br>

- **India Gender Gap Analytics** — MySQL staging for PLFS 2023–24 data *(in progress)*
- [**Indian Railways Punctuality Analysis**](https://github.com/sindhusharmamarupaka/railways-sql-analysis) — 5–7 level query progression, CTEs, window functions, 1,900-row dataset
</details>

<details>
<summary><img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"></summary>
<br>

- [**Customer Feedback Analysis**](https://github.com/sindhusharmamarupaka/customer-feedback-analysis) — Pandas-based complaint filtering, differential word-rate analysis, HuggingFace API integration
- [**Accident Dataset Analysis**](https://github.com/sindhusharmamarupaka/accident-dataset-analysis) — Cleaned and analyzed 12,316 real accident records; found normal-weather accidents are more fatal than poor-visibility ones
</details>

<details>
<summary><img src="https://img.shields.io/badge/Power%20BI%20%2F%20DAX-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"></summary>
<br>

- **India Gender Gap Analytics** — Star-schema model, DAX measures, drill-through dashboard, bookmark navigation *(in progress)*
</details>

<details>
<summary><img src="https://img.shields.io/badge/Power%20Query-217346?style=for-the-badge&logo=powerquery&logoColor=white"></summary>
<br>

- **India Gender Gap Analytics** — Cleaning and reshaping raw PLFS indicator columns *(in progress)*
</details>

<details>
<summary><img src="https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white"></summary>
<br>

- **SME Retail Finance Cash Flow Dashboard** *(upcoming)* — Cash flow modeling and KPI reporting
</details>

<details>
<summary><img src="https://img.shields.io/badge/GenAI-4a9ef8?style=for-the-badge"></summary>
<br>

- [**Customer Feedback Analysis**](https://github.com/sindhusharmamarupaka/customer-feedback-analysis) — Automated response drafting via HuggingFace Inference API
- [**Accident Dataset Analysis**](https://github.com/sindhusharmamarupaka/accident-dataset-analysis) — Directed, reviewed use across feature engineering, debugging, and insight-writing — analytical decisions made independently, GenAI used for implementation support only
</details>

<details>
<summary><img src="https://img.shields.io/badge/Currently%20Developing-6c757d?style=for-the-badge"></summary>
<br>

Machine Learning · Advanced SQL · Statistical Modelling
</details>
## 🗺️ Roadmap

- [x] Indian Railways SQL Analysis
- [x] Customer Feedback Analysis — Internship
- [x] Accident Dataset Analysis
- [ ] India Gender Gap Analytics *(in progress — capstone)*
- [ ] SME Retail Finance Cash Flow Dashboard *(starts after capstone)*

---

## ✍️ Writing

📰 [Harvest of Certainty: How Data Science is Predicting Crop Yields and Reducing Farmer Risk in India](https://medium.com/@sindhusharmamarupakaa/harvest-of-certainty-how-data-science-is-predicting-crop-yields-and-reducing-farmer-risk-in-india-3f578baebbef)
*How predictive models can lower the financial risk Indian farmers face from unpredictable yields.*

---

## 🤝 Connect

📍 Hyderabad, India · **LinkedIn:** [linkedin.com/in/sindhu-sharma-data-analyst](https://www.linkedin.com/in/sindhu-sharma-data-analyst) · **Email:** [sindhusharmamarupakaa@gmail.com](mailto:sindhusharmamarupakaa@gmail.com) · **Medium:** [medium.com/@sindhusharmamarupakaa](https://medium.com/@sindhusharmamarupakaa)

---

*Data → Analysis → Insight → Decision*
