# 🎬 Netflix Movies — "Exploratory Data Analysis"(EDA)

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C72B0)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Plots-orange)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)

> A data-driven exploration of Netflix's movie catalogue — uncovering genre trends, popularity patterns, and release year distributions across **9,827 films**.

---

## 📌 Project Overview

This project performs an in-depth **Exploratory Data Analysis (EDA)** on a Netflix movies dataset (`Netflix.csv`). The goal is to answer five key analytical questions about genre frequency, audience voting patterns, popularity extremes, and content release trends.

---

## ❓ Questions Answered

|  #   | Question  | Answer  |
|---|----------|--------|
| 1 | What is the most frequent genre of movies on Netflix? | **Drama** (3,744 occurrences) |
| 2 | Which genre has the highest votes? | Movies in the **'popular'** vote tier dominate |
| 3 | Which movie got the highest popularity? | **Spider-Man: No Way Home (2021)** — Score: 5,083.954 |
| 4 | Which movie got the lowest popularity? | **The United States vs. Billie Holiday** & **Threads (1984)** — Score: 13.354 |
| 5 | Which year had the most movies released? | **2020** (peak of the streaming content boom) |

---

## 📂 Dataset

- **File:** `Netflix.csv`
- **Records:** 9,827 movies
- **Columns:** Release_Date, Title, Overview, Popularity, Vote_Count, Vote_Average, Original_Language, Genre, Poster_Url

---

## 🛠️ Tech Stack

- **Python 3**
- **Pandas** — data manipulation & cleaning
- **NumPy** — numerical operations
- **Matplotlib** — base plotting
- **Seaborn** — statistical visualisations

---

## 🧹 Data Cleaning Steps

1. **Date Conversion** — `Release_Date` converted from string to datetime; only the year was retained.
2. **Dropped Columns** — `Overview`, `Original_Language`, and `Poster_Url` were removed as irrelevant to the analysis.
3. **Vote Categorisation** — `Vote_Average` was binned into 4 ordered categories using percentile boundaries:
   - `Not_popular` → `Below_Avg` → `Average` → `popular`
4. **Null & Duplicate Check** — No duplicates found; NaN rows dropped after binning.
5. **Genre Explosion** — Multi-genre strings (e.g., `"Action, Adventure"`) were split and exploded into individual rows, expanding the dataset to **25,793 rows**.

---

## 📊 Visualisations

### 1. Genre Frequency Distribution
A horizontal count plot showing how often each of the 19 genres appears across the dataset.
> **Drama** leads significantly, followed by Comedy and Action.

### 2. Movies by Vote Popularity Tier
A count plot displaying how many movies fall into each of the four voting categories.
> The **popular** tier has the most movies, indicating Netflix hosts predominantly well-rated content.

### 3. Release Year Distribution
A histogram showing the number of movies released per year across the entire dataset.
> A sharp spike is visible around **2019–2022**, reflecting the streaming content production boom.

---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/netflix-eda.git
   cd netflix-eda
   ```

2. **Install dependencies**
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```

3. **Launch the notebook**
   ```bash
   jupyter notebook EDA.ipynb
   ```

4. Make sure `Netflix.csv` is in the same directory as the notebook.

---

## 📁 Project Structure

```
netflix-eda/
│
├── EDA.ipynb           # Main Jupyter Notebook with full analysis
├── Netflix.csv         # Dataset (not included — add your own)
├── README.md           # Project documentation
└── Netflix_EDA_Report.pdf  # Full PDF report of the analysis
```

---

## 💡 Key Takeaways

- Netflix's catalogue is heavily weighted towards **Drama**, reflecting global audience preferences for narrative-driven content.
- The dataset shows a strong **recency bias** — most content was produced post-2010.
- **Mainstream blockbusters** dominate popularity scores; niche and older films sit at the lower end.
- Many movies span **multiple genres**, making the genre explosion technique essential for accurate frequency analysis.
- Netflix's library is overall **well-rated**, with the majority of titles landing in the average-to-popular tier.

---

## 👤 Author

**Mrinmoy Talukdar**  
📧 *[mrinmoytalukdargcu@gmail.com]*  


---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
