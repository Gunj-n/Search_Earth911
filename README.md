Target:
Scrapes recycling facility details (title, address, materials accepted, last updated date) from Earth911’s search result pages for electronics recycling in New York, NY.

Steps:
1. Visit Search URL – Opens the search result page for electronics recycling.
2. Extract Links – Scrapes facility detail page links.
3. Scrape Details – From each facility page, extracts:
   - Title
   - Address
   - Last Updated
   - Material Accepted
   - URL
4. Store in CSV – Compiles all data and exports it to a UTF-8 encoded CSV file.

Pagination:
Currently only the first page is processed. 

Data Cleaning:
- Uses `.text.strip()` to clean text.
- CSV exported in `utf-8-sig` to support Excel.

Error Handling:
- Each extraction block uses `try/except` to avoid script crashes.
- Logs error messages to console.



## 🧰 Libraries and Tools Used
`selenium`- Controls the browser to handle JavaScript-rendered content 
`webdriver_manager`- Automatically manages the correct version of ChromeDriver 
`csv`- For writing structured data to a file 
`time`- For inserting delays (can be improved with WebDriverWait) 
