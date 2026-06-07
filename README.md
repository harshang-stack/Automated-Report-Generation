# 📊 Automated PDF Reports with Python

COMPANY: CODTECH IT SOLUTIONS

NAME: RANA HARSHANG HIREN

INTERN ID: CTIS9957

DOMAIN: PYTHON PROGRAMMING 

BATCH DURATION: MAY 09th,2026 to JUNE 6th, 2026

MENTOR NAME : NEELA SANTHOSH KUMAR

Automatically generate, schedule, and email PDF reports from a Jupyter Notebook — no manual effort required.

This project demonstrates a full automated reporting pipeline: it fetches **TSLA stock data** daily, builds a financial report inside a Jupyter Notebook, exports it as a PDF, and sends it via email. The live report runs every weekday at **9:00 AM (Europe/Warsaw)**.

---

## 🚀 Features

- 📈 Fetches live stock market data via `yfinance`
- 📉 Renders financial charts using `mplfinance`
- 📄 Converts Jupyter Notebooks to interactive web apps with [Mercury](https://github.com/mljar/mercury)
- 🕘 Schedules automatic daily report execution (Mon–Fri)
- 📧 Sends the report as a PDF attachment by email
- 🌐 Deployable as a web application (Heroku-ready via `Procfile`)

---

## 🗂️ Project Structure

```
automated-pdf-reports-python/
├── report.ipynb        # Main report notebook (data fetching + charts)
├── welcome.md          # Mercury app welcome page content
├── requirements.txt    # Python dependencies
├── Procfile            # Heroku deployment config
├── .gitignore
├── LICENSE             # MIT
└── media/              # Demo GIFs and banner image
```

---

## ⚙️ Installation

**1. Clone the repository**

```bash
git clone https://github.com/pplonski/automated-pdf-reports-python.git
cd automated-pdf-reports-python
```

**2. Install dependencies**

```bash
pip install -r requirements.txt
```

**3. Run the Mercury app locally**

```bash
mercury run
```

Then open `http://localhost:8000` in your browser.

---

## 📦 Dependencies

| Package | Purpose |
|---|---|
| `mljar-mercury >= 1.0.1` | Converts notebooks to web apps, handles scheduling & PDF export |
| `yfinance` | Fetches stock market data from Yahoo Finance |
| `mplfinance` | Renders financial candlestick and OHLC charts |

---

## 🖥️ Demo

### Convert Report to PDF

![convert report to pdf](https://github.com/pplonski/automated-pdf-reports-python/raw/main/media/report-to-pdf.gif)

### Interactive Report

![interactive report](https://github.com/pplonski/automated-pdf-reports-python/raw/main/media/interactive-report.gif)

---

## ☁️ Deployment

This project includes a `Procfile` for one-click deployment to **Heroku**.

```
web: mercury run 0.0.0.0:$PORT
```

Deploy steps:
1. Create a Heroku app
2. Push this repo to Heroku
3. Set any required environment variables (e.g. email credentials for notifications)

