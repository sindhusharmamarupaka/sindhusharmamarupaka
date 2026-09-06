![Sindhu Marupaka](https://raw.githubusercontent.com/sindhusharmamarupaka/sindhusharmamarupaka/main/profile_banner.png)

I work with data to uncover patterns, answer business questions, and communicate insights through analysis and visualization. Most dashboards answer "what happened" — I try to build ones that also answer "so what should we do about it."

I'm drawn to public-interest data in particular — labour force surveys, railway operations, agricultural risk — because I'd rather practice on real, messy questions that affect people than polish a textbook dataset.

---

## 📌 Case Studies

### 01 · India Gender Gap Analytics
![SQL](https://img.shields.io/badge/SQL-d64545?style=for-the-badge&logo=mysql&logoColor=white) ![Power Query](https://img.shields.io/badge/Power%20Query-e75480?style=for-the-badge&logo=powerquery&logoColor=white) ![DAX](https://img.shields.io/badge/DAX-2e8b57?style=for-the-badge) ![Power BI](https://img.shields.io/badge/Power%20BI-d4a017?style=for-the-badge&logo=powerbi&logoColor=black)

**Question**
Why do fewer women work than men in India, and does the gap shift with location, education, or marital status?

**Approach**
An end-to-end pipeline on 319,773 working-age PLFS 2023–24 records — MySQL for cleaning and joins, Power Query for decoding, DAX for a 13-page Power BI dashboard with Story Mode navigation, a Key Influencers ML visual, and a state-level what-if explorer.

**What I caught**
A DAX measure meant for arithmetic was silently pulling from a `FORMAT()`-wrapped text field instead of its raw numeric counterpart, throwing off downstream calculations. Traced it and split every display measure from its `_Raw` numeric twin.

**Delivered**
A 13-page interactive dashboard, a 31-page written report, and per-page SQL validation files cross-checked against the raw microdata.

<img src="https://raw.githubusercontent.com/sindhusharmamarupaka/sindhusharmamarupaka/main/badge_completed.png" width="140">

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

I don't stop at "what happened" — every project here is built to answer "so what should we do about it." A few habits that show up consistently across my work:

- **I distrust raw numbers until I've stress-tested them.** Aggregates hide bias. On the accident dataset, raw counts made "Normal" weather look safest simply because it's the most common condition — switching to within-category percentages flipped that story entirely.
- **I audit the pipeline before I trust the output.** On the Railways analysis, rows were silently dropping during CSV import. I traced it to an encoding mismatch before it could quietly skew 1,900 records of delay data — not after. On the Gender Gap dashboard, a DAX measure was silently pulling from a formatted text field instead of its raw number — I caught it before it reached the dashboard.
- **I choose real, messy, public-interest data on purpose** — labour force surveys, railway operations, accident records — because that's where analytical judgment is actually tested, not a cleaned textbook dataset.
- **I use GenAI for execution, not judgment.** Every interpretive call — what the data means, which comparison matters, what to recommend — is mine. AI supports implementation; it doesn't make the call.

---

## 🛠️ Toolkit

*Click a skill badge to see the list of projects — then click a project name to open its repo.*

<details>
<summary><img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"></summary>
<br>

- [**India Gender Gap Analytics**](https://github.com/sindhusharmamarupaka/gender-gap-labour-force-india) — MySQL cleaning and joins across 319,773 PLFS records
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

- [**India Gender Gap Analytics**](https://github.com/sindhusharmamarupaka/gender-gap-labour-force-india) — 13-page dashboard, Story Mode navigation, Key Influencers ML visual, what-if explorer
</details>

<details>
<summary><img src="https://img.shields.io/badge/Power%20Query-217346?style=for-the-badge&logo=powerquery&logoColor=white"></summary>
<br>

- [**India Gender Gap Analytics**](https://github.com/sindhusharmamarupaka/gender-gap-labour-force-india) — Decoding raw PLFS indicator columns
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
- [x] India Gender Gap Analytics
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
