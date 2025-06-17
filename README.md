# LSE Academic Staff Collaboration Analysis

**Python • pandas • BeautifulSoup • Selenium • matplotlib • seaborn**

## 1. Introduction

This project explores the research interests of academic staff across eight LSE departments to identify opportunities for interdisciplinary collaboration. By scraping “Key Expertise” entries from public profile pages, we quantify shared topics between departments and individual staff pairs, and surface the most popular and most diverse research areas.

## 2. Data

- **Source:** LSE department “People” pages for Statistics, Mathematics, Finance, Accounting, Management, Economics, Data Science Institute, and Methodology  
- **Collection method:** Selenium for dynamic pages (first four departments) + BeautifulSoup for static pages (last four)  
- **Final dataset:** `merged.csv` (one row per professor, including name, title, department, and cleaned “Key Expertise” strings)  
- **Approximate size:** _[fill in total rows after merge]_ observations × 7 columns

## 3. Methods

1. **Data Acquisition**  
   - Automated browser navigation to collect profile URLs  
   - Scraped professor name, prefix, languages, modules, key expertise, and department  
2. **Data Preparation**  
   - Consolidated individual CSVs into one DataFrame  
   - Standardized “Key Expertise” text (removed brackets, split on commas/semicolons)  
   - Filled missing expertise entries with blank  
3. **Exploratory Analysis**  
   - Counted professors per department and missing‐value assessment  
   - Visualized distribution of number of shared topics  
4. **Collaboration Metrics**  
   - **Q1:** Counted department‐pair co‐occurrences on shared topics  
   - **Q2:** Identified staff‐pair with highest number of common interests  
   - **Q3:** Ranked topics by number of distinct departments interested  
   - **Q4:** Listed top 10 topics across all departments and top 5 per department  

## 4. Key Findings

- **Q1 (Department Pairs):**  
  - Economics & Management: 15 shared‐interest occurrences  
  - Economics & Finance: 11  
  - Accounting & Finance: 9  

- **Q2 (Top Staff Pair):**  
  - **Mohan Bijapur & Ricardo Reis** share 3 topics: monetary economics, financial economics, macroeconomics  

- **Q3 (Most Diverse Topics):**  
  1. Innovation (15 professors across 5 departments)  
  2. Econometrics (16 across 4)  
  3. Machine learning (8 across 4)  
  4. Risk management (4 across 4)  
  5. Economics of information (3 across 3)  

- **Q4 (Most Popular Topics):**  
  1. Macroeconomics (24 professors)  
  2. Econometrics (16)  
  3. Innovation (15)  
  4. Accounting (14)  
  5. Labour (14)  
  6. Development economics (13)  
  7. Political economy (12)  
  8. Asset pricing (11)  
  9. Economic theory (10)  
  10. Corporate finance (10)
