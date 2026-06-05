# 📸 Stock Image Scrapper

[![GitHub Repo](https://img.shields.io/badge/GitHub-Repository-blue?logo=github)](https://github.com/vinayakmishra4/Stock-Image-Scraper-)
[![Python 3.x](https://img.shields.io/badge/Python-3.x-yellow.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

A powerful, interactive Python web scraping tool designed to extract stock images and metadata from dynamically loaded websites. Built entirely inside a Jupyter Notebook, this project serves as a practical guide to combining **Selenium WebDriver** (for browser automation) with **BeautifulSoup4** (for HTML parsing) to effortlessly bypass "infinite scroll" mechanics and capture a complete dataset.

Easily collect **Image URLs, Tags, Likes, and Comments**, and export everything into a clean, ready-to-use CSV dataset for data analysis or machine learning pipelines.

🔗 **Direct Link to Code:** [stockimagescrapper.ipynb](https://github.com/vinayakmishra4/Stock-Image-Scraper-/blob/main/stockimagescrapper.ipynb)

---

## ✨ Key Features

* **Interactive Execution:** Run and test the scraping logic step-by-step using Jupyter Notebook, allowing you to observe the browser actions in real-time.
* **Bypasses Infinite Scrolling:** Uses automated JavaScript execution via Selenium to continuously scroll and load new dynamic content until the end of the page is reached.
* **Comprehensive Data Extraction:** Targets and scrapes direct image URLs, descriptive tags, like counts, and comment counts.
* **Automated Data Structuring:** Leverages Pandas to instantly convert raw, nested HTML data into a clean tabular DataFrame.
* **Visual Progress Tracking:** Implements `tqdm` to display execution progress bars, keeping you informed on the exact state of the scraping loop.

---

## 🛠️ Tech Stack & Libraries

* **Jupyter Notebook:** Interactive development environment.
* **Python 3.x:** Core programming language.
* **Selenium:** Automates the Google Chrome browser to trigger JavaScript events (like scrolling).
* **BeautifulSoup4 (bs4):** Parses the final, fully-loaded DOM tree to extract specific HTML tags efficiently.
* **Pandas:** Handles data manipulation and exports the final `.csv` dataset.
* **tqdm:** Generates dynamic progress bars during extraction loops.

---

## ⚙️ Prerequisites & Installation

Before running this project, ensure you have **Google Chrome** installed on your machine, as the script relies on the Chrome WebDriver architecture.

### 1️⃣ Clone the Repository

```bash
git clone [https://github.com/vinayakmishra4/Stock-Image-Scraper-.git](https://github.com/vinayakmishra4/Stock-Image-Scraper-.git)
cd Stock-Image-Scraper-

```

### 2️⃣ Install Required Dependencies

Ensure you have Python installed, then run the following command in your terminal to install the necessary libraries:

```bash
pip install jupyter requests pandas tqdm selenium beautifulsoup4 chromedriver-binary

```

*(Note: `chromedriver-binary` automatically handles downloding the correct WebDriver version required for Selenium to control Chrome).*

---

## ▶️ How to Run the Notebook

Because this project is built as an interactive notebook, you will execute the logic cell-by-cell.

1. **Launch Jupyter** in your terminal from the project directory:
```bash
jupyter notebook

```


2. **Open the file** named [`stockimagescrapper.ipynb`](https://github.com/vinayakmishra4/Stock-Image-Scraper-/blob/main/stockimagescrapper.ipynb) in your browser interface.
3. **Run the cells sequentially (Shift + Enter):**
* **Cell 1 (Imports):** Loads all necessary Python dependencies.
* **Cell 2 (Driver Setup):** Initializes the Chrome WebDriver. An automated Chrome browser window will pop up. **Do not close this window manually!**
* **Cell 3 (Scrolling & Scraping):** The core logic. Watch the automated browser scroll to the bottom of the page repeatedly until all images are loaded. The notebook will then capture and extract the HTML source code.
* **Cell 4 (Data Export):** Converts the extracted lists into a Pandas DataFrame and saves it to your folder as `output.csv`.



---

## 🧠 Under the Hood: How the Code Works

Traditional scraping libraries like `requests` fail on modern websites because images load dynamically via JavaScript as the user scrolls. Here is how this notebook solves that problem:

1. **Triggering Dynamic Content (Selenium):** The script uses a `while` loop combined with `driver.execute_script("window.scrollTo(0, document.body.scrollHeight);")`. It records the height of the page, scrolls to the bottom, waits for new images to load, and checks the new height. If the height hasn't changed, it determines it has reached the absolute bottom of the page.
2. **DOM Parsing (BeautifulSoup):** Once the page is fully expanded and all images are injected into the DOM by the site's JavaScript, `driver.page_source` grabs the massive HTML block and passes it to BeautifulSoup.
3. **Targeted Extraction:** BS4 searches for the specific HTML classes (e.g., the `<img>` and `<div>` tags holding the metadata). It isolates the `src` links and cleans the text of the tags, likes, and comments, appending them to synchronized Python lists.

---

## 📊 Output Format

The generated dataset will appear in your project root directory as an `output.csv` file. The data structure matches the layout below:

| 🖼️ Image URL | 🏷️ Tags | ❤️ Likes | 💬 Comments |
| --- | --- | --- | --- |
| `https://example.com/images/photo1.jpg` | Nature, Mountains, Sky | 1,204 | 45 |
| `https://example.com/images/photo2.jpg` | Technology, Computer, Code | 890 | 12 |

---

## ⚠️ Disclaimer

This project is developed for **educational purposes only**. Please respect the target website’s Terms of Service and `robots.txt` configurations before running scrapers. Avoid sending an overwhelming number of automated requests, as this can place unintended stress on the host server.

---

## 📄 License

This project is licensed under the **MIT License**.

```

```