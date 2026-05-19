# Film_BoxOffice_ETL_Data_Pipeline
End-to-end ETL pipeline scraping 1,000 films from Box Office Mojo (2019-2023), cleaning raw messy data, and building an interactive analytics dashboard using Python and Plotly.

---

## 📊 Dashboard Preview
> Download `film_dashboard.html` and open it in any browser to view the full interactive dashboard.

---

## 📁 Project Structure
```
├── Film_BoxOffice_ETL_Pipeline.ipynb  # Google Colab notebook
├── film_dashboard.html                # Final interactive dashboard
└── README.md
```

---

## 🔍 Problem Statement
Raw web data is messy — inconsistent formats, missing values, dollar signs in numeric columns, and duplicate records. This project builds a complete ETL pipeline that extracts real box office data, transforms it into a clean analytical dataset, and loads it into an interactive dashboard.

---

## ⚙️ ETL Pipeline Stages

**Extract**
- Scraped 5 years of box office data (2019–2023) from Box Office Mojo
- Used Python `requests` and `BeautifulSoup` with polite delay between requests
- Collected 200 films per year → 1,000 raw records

**Transform**
- Removed `$` and `,` from money columns → converted to float
- Standardised release dates → extracted month and year
- Replaced `-` placeholder values with `NaN`
- Removed duplicate records
- Engineered `performance_tier` column (Blockbuster / Hit / Average / Underperformer)
- Cleaned distributor names and filled missing values

**Load**
- Exported clean master CSV (`clean_boxoffice_master.csv`)
- Built interactive HTML dashboard with Plotly

---

## 📦 Dataset
- **Source:** Box Office Mojo (boxofficemojo.com)
- **Years:** 2019, 2020, 2021, 2022, 2023
- **Size:** 1,000 films
- **Key columns:** release, gross, total_gross, theaters, distributor, year, month, performance_tier

---

## 🛠️ Tools Used
| Tool | Purpose |
|------|---------|
| Python | Core language |
| Requests | HTTP scraping |
| BeautifulSoup | HTML parsing |
| Pandas | Data cleaning and transformation |
| Plotly | Interactive charts |
| WordCloud | Film title visualisation |
| Google Colab | Development environment |

---

## 📈 Dashboard Features
- **KPI Cards** — Total films, total box office ($43.6B), avg gross per film ($44M), blockbuster count, highest grossing film
- **Bar Chart** — Total gross by year
- **Donut Chart** — Performance tier distribution
- **Horizontal Bar** — Top 10 highest grossing films (2019–2023)
- **Line Chart** — Number of releases by month
- **Stacked Bar** — Performance tiers by year
- **Bar Chart** — Top 8 distributors by total gross
- **Word Cloud** — Film titles across 5 years

---

## 💡 Key Findings
- Total box office across 2019–2023 reached **$43.6B**
- Only **32 out of 1,000 films** qualified as Blockbusters (>$300M gross)
- **781 films (78%)** were Underperformers — showing how selective box office success really is
- **Avengers: Endgame** was the highest grossing film of the period
- **Walt Disney Studios** dominated distributor gross across all 5 years

---

## 🚀 How to Run
1. Open `Film_BoxOffice_ETL_Pipeline.ipynb` in Google Colab
2. Run all cells in order
3. Dashboard auto-downloads as `film_dashboard.html`
4. Open in any browser

---

## 👩‍💻 Author
**Varshini**
Aspiring Data Analyst | Chennai, Tamil Nadu
[LinkedIn](https://www.linkedin.com/in/varshini-anburaj-530260227/) · 

---

*Project 4 of a 60-day data analytics portfolio challenge.*
