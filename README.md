# Website Scraper

A Python-based web scraping application developed as part of the **Information Assurance and Security** course at Tunis Business School (TBS), Academic Year 2025–2026.

The application allows users to extract structured data from websites through a simple Flask-based web interface and export the results in multiple formats.

## Project Overview

The Website Scraper provides an accessible way to collect and organize website content while incorporating basic security and responsible scraping practices.

**Key Features**
- Extract website content such as headings, links, and paragraphs.
- Check website `robots.txt` rules before scraping.
- Apply request delays to reduce server load.
- Verify TLS certificates for secure HTTPS connections.
- Export extracted data in CSV, JSON, and Excel formats.
- Download results directly through the web interface.

## Technologies Used

- **Python** – Core programming language
- **Flask** – Web application framework
- **Requests** – HTTP requests
- **BeautifulSoup** – HTML parsing and data extraction
- **OpenPyXL** – Excel file generation
- **HTML/CSS** – Web interface

## Project Structure

```text
webscraper/
│
├── app.py                  # Flask application
├── requirements.txt        # Project dependencies
│
├── scraper/
│   └── scraper.py          # Core scraping logic
│
├── templates/
│   └── index.html          # Web interface
│
└── output/                 # Exported files
```

## Getting Started

### Prerequisites

- Python 3.9 or higher
- Git (optional)

### 1. Clone the Repository

```bash
git clone <repository-url>
cd webscraper
```

Alternatively, download the repository and open its folder in your terminal.

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the Application

```bash
python app.py
```

Once the server starts, open your browser and navigate to:

```text
http://127.0.0.1:5000
```

## How to Use

1. **Enter a URL:** Provide the website address you want to scrape.
2. **Select Data Fields:** Choose the content to extract, such as headings, links, and paragraphs.
3. **Choose an Export Format:** Select CSV, JSON, or Excel.
4. **Run the Scraper:** Start the extraction process.
5. **Download Results:** Review the extraction status and download the generated file.

## Security Features

The application incorporates several checks to encourage responsible and secure scraping.

| Security Measure | Description |
|---|---|
| **robots.txt Compliance** | Checks website scraping permissions before extraction and stops if access is disallowed. |
| **Rate Limiting** | Introduces a 1–3 second delay between requests to reduce server load. |
| **TLS Verification** | Verifies HTTPS certificates to ensure secure connections. |
| **User-Agent Handling** | Uses browser-like User-Agent headers when sending requests. |

## Testing

The following websites are suitable for testing the application:

| Website | Purpose |
|---|---|
| [Books to Scrape](https://books.toscrape.com/) | Extracting book information |
| [Quotes to Scrape](https://quotes.toscrape.com/) | Extracting quotes and authors |
| [Example.com](https://example.com/) | Basic HTML extraction |

Always respect website access policies and scraping permissions.

## Scraping Workflow

```text
       User Input
      (URL + Fields)
            |
            v
    Check robots.txt
            |
       +----+----+
       |         |
    Allowed    Blocked
       |         |
       v         v
  Rate Limiting  Stop
       |
       v
   Fetch HTML
       |
       v
   Parse HTML
       |
       v
 Extract Data
       |
       v
  Clean Data
       |
       v
 Export Results
 (CSV / JSON / Excel)
       |
       v
   Download File
```

## Troubleshooting

| Issue | Possible Solution |
|---|---|
| `ModuleNotFoundError` | Install dependencies again using `pip install -r requirements.txt`. |
| `Address already in use` | Change the Flask application port, for example to `5001`. |
| No records extracted | The website may load content dynamically using JavaScript. Try a static website. |
| `robots.txt` blocks the URL | Select another website that permits scraping. |

## Academic Context

**Course:** Information Assurance and Security  
**Institution:** Tunis Business School (TBS)  
**Academic Year:** 2025–2026

---

*Developed as an academic cybersecurity project exploring web scraping, data extraction, and security considerations.*
