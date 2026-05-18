# 🔍 Wuzzuf Job Scraper

A Python web scraping project that collects job listings from [Wuzzuf.net](https://wuzzuf.net) — Egypt's leading job platform — and exports the results to a structured CSV file for analysis.

---

## 📌 Overview

This scraper automates job searching across multiple tech roles and extracts key details from each listing, including job title, company, location, employment type, and experience requirements.

---

## 🚀 Features

- Searches multiple job titles in a single run
- Scrapes across multiple pages per search query
- Extracts: Job Title, Company, Location, Tags (job type/work model), Experience, and Search Query
- Handles stale elements and dynamic page loading gracefully
- Exports all results to a clean `Jobs.csv` file

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| Selenium | Browser automation & scraping |
| Pandas | Data handling & CSV export |
| ChromeDriver | Headless Chrome browser control |

---

## ⚙️ Setup & Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/YoussefNasser05/wuzzuf-job-scraper.git
   cd wuzzuf-job-scraper
   ```

2. **Install dependencies**
   ```bash
   pip install selenium pandas
   ```

3. **Install ChromeDriver**  
   Download the version matching your Chrome browser from [chromedriver.chromium.org](https://chromedriver.chromium.org/) and add it to your PATH.

---

## ▶️ Usage

Open and run `selenium.ipynb` in Jupyter Notebook, or convert and run as a script:

```bash
jupyter nbconvert --to script selenium.ipynb
python selenium.py
```

To change the job titles being searched, edit the `jobssearch` list at the top of the file:

```python
jobssearch = ['Python Developer', 'Data Engineer', 'AI Developer', 'Data Scientist']
```

---

## 📂 Output

Results are saved to `Jobs.csv` with the following columns:

| Column | Description |
|--------|-------------|
| `job_title` | Title of the job listing |
| `company` | Company name |
| `location` | City and country |
| `tags` | Employment type and work model (e.g. Full Time, Remote) |
| `exp` | Required years of experience |
| `search_query` | The job title used to find this listing |

---

## 📊 Sample Data

| job_title | company | location | tags | exp | search_query |
|-----------|---------|----------|------|-----|--------------|
| Senior Data Engineer | GB Corp | Giza, Egypt | Full Time, On-site | 3-7 Yrs | Data Engineer |
| AI Developer (Python) | Afaqy | Maadi, Cairo | Full Time, Hybrid | 3-6 Yrs | Python Developer |

---

## ⚠️ Notes

- The scraper uses anti-detection options to reduce the chance of being blocked
- A small `time.sleep()` delay is used between actions to mimic human behavior
- CSS class names on Wuzzuf may change over time — update selectors if the scraper breaks


---

## 📄 License

This project is for educational and personal use only. Always respect a website's `robots.txt` and terms of service before scraping.
