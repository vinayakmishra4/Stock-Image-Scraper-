# 📸 Stock Image Scraper

A powerful, beginner-friendly Python web scraping automation project designed to extract stock images and metadata from dynamically loaded websites. By combining **Selenium** for browser automation with **BeautifulSoup** for HTML parsing, this tool effortlessly bypasses "infinite scroll" mechanics to capture a complete dataset.

Easily collect **Image URLs, Tags, Likes, and Comments**, and export everything into a clean, ready-to-use CSV dataset.

🔗 **[View the Code Repository Here](https://www.google.com/search?q=https://github.com/vinayakmishra4/Stock-Image-Scraper-)**

---

## ✨ Features

* **Bypasses Infinite Scrolling:** Uses Selenium JavaScript execution to continuously load new dynamic content.
* **Comprehensive Data Extraction:** Scrapes direct image URLs, descriptive tags, likes, and comment counts.
* **Automated Data Cleaning:** Uses Pandas to structure the raw HTML data into a tabular format.
* **Ready-to-Use Dataset:** Automatically exports the final scraped data to a `.csv` file.
* **Visual Progress Tracking:** Implements `tqdm` so you can monitor the scraping progress in real-time.

---

## 🛠️ Built With

* **Python** — Core programming language
* **Selenium** — Automates the browser to handle dynamic JS loading
* **BeautifulSoup4** — Parses the DOM to extract specific HTML tags
* **Pandas** — Structures and exports the data
* **Requests** — Handles HTTP requests
* **tqdm** — Displays execution progress bars

---

## 🌐 Target Website

This project is built to scrape data from the following demo site:

```bash
https://stock-pictures.netlify.app

```

---

## ⚙️ Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/vinayakmishra4/Stock-Image-Scraper-.git
cd Stock-Image-Scraper-

```

### 2️⃣ Install Required Dependencies

Ensure you have Python installed, then run the following command to install the required libraries:

```bash
pip install requests pandas tqdm selenium beautifulsoup4 chromedriver-binary

```

---

## ▶️ How to Run

This project's main logic is contained within a Jupyter Notebook.

**Option A: Using Jupyter Notebook (Recommended)**

1. Open your terminal in the project directory.
2. Launch Jupyter:
```bash

```



jupyter notebook

```
3. Open `stockimagescrapper.ipynb` and run the cells sequentially. 

**Option B: Running as a Python Script**
If you prefer a terminal-based workflow, convert the notebook to a standard Python script and run it:
```bash
python scraper.py

```

**The scraper will automatically:**

1. Open a Chrome browser window.
2. Scroll to the bottom of the page dynamically until all images load.
3. Parse the HTML and extract the metadata.
4. Generate a `.csv` file in your directory containing all the results.

---

## 📊 Output Format

The generated `output.csv` dataset contains the following structured fields:

| Field | Description |
| --- | --- |
| **🖼️ Image URL** | Direct `src` link to the high-resolution image |
| **🏷️ Tags** | The category or descriptive tags attached to the image |
| **❤️ Likes** | Total number of likes the image received |
| **💬 Comments** | Total number of comments on the image |

---

## 🚀 Future Improvements

We are continuously looking to enhance this scraper. Planned updates include:

* [ ] **Automatic Image Downloading:** Fetching the physical image files locally using `requests`.
* [ ] **Multi-threaded Scraping:** Implementing concurrent execution for significantly faster data extraction.
* [ ] **Headless Browser Mode:** Running Selenium without a GUI to save system resources.
* [ ] **Database Integration:** Exporting directly to MongoDB or MySQL.

---

## 📚 What You’ll Learn

Exploring this codebase is a great way to understand:

* **Web Scraping Fundamentals:** Navigating DOM structures and CSS selectors.
* **Browser Automation:** Using Selenium WebDriver to simulate human behavior.
* **Handling Dynamic Content:** Overcoming JavaScript-heavy sites that block traditional requests.
* **Data Engineering:** Structuring raw web data into clean, analytical datasets.

---

## ⚠️ Disclaimer

This project is developed for **educational purposes only**. Please respect the target website’s Terms of Service and `robots.txt` before scraping any content, and avoid sending an overwhelming number of automated requests.

---

## 📄 License

This project is licensed under the **MIT License**.

---

*If you found this project useful, consider giving it a ⭐ on [GitHub](https://www.google.com/search?q=https://github.com/vinayakmishra4/Stock-Image-Scraper-).*