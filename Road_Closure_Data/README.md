# Analysis of Unstructured Data: Road Closure Data

## Executive Summary

- This project demonstrates two  approaches to working with unstructured data: 
- Automated web scraping of dynamically rendered web content
- Structured data acquisition via a public API. The work compares alternative data acquisition methods

---

## Project Overview

The project addresses a unstructured data challenges relevant to infrastructure and service operations:

Road closure intelligence collected from public sources to demonstrate alternative data acquisition techniques.

Two notebooks are provided to illustrate and compare approaches to unstructured data processing, scraping and API integration.

## Directory Structure

BPPUnstructuredData
├── notebooks
    ├── BP0306130_M7USD_Selenium.ipynb
    ├── BP0306130_M7USD_API.ipynb
├── .env
├── .gitignore
└── README.md

---

## Notebook Overview

### 1. Selenium_web_Scrape.ipynb

Purpose: Demonstrate extraction of road closure data from a dynamically rendered website
Rationale: Selenium was required due to client‑side rendering that prevents static HTML scraping
Outcome: Used as a comparative and exploratory approach rather than the final data pipeline

---

### 2. API.ipynb

Purpose: Retrieve structured road closure data using the National Highways API
Rationale: Improved reliability, performance, and data quality compared to browser‑based scraping
Outcome: Selected as the preferred method for structured data acquisition

---

## Comparison: Selenium vs API

| Aspect | Selenium | API |
|--------|----------|-----|
| **Method** | Web scraping rendered HTML | Direct HTTP requests |
| **Complexity** | Higher (browser automation) | Lower (structured data) |
| **Reliability** | Subject to UI changes | Stable interface |
| **Speed** | Slower (browser overhead) | Faster (lightweight) |
| **Data Format** | Unstructured HTML | Structured XML/JSON |
| **Rate Limiting** | Polite delays required | API quota management |
| **Selection Rationale** | Exploratory; comparison | Final pipeline (selected) |

---

## Reproducability & Setup

Requirements:
    - Python 3.8+
    - Core libraries: pandas, selenium, requests, python-dotenv
    - API key stored in a .env file
    - Edge Driver can be installed using web browser (selnium web scrape)