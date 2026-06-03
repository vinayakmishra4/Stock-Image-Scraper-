# 📸 Stock Image Scraper

A powerful Python web scraping project that extracts stock images and metadata from dynamically loaded websites using **Selenium** and **BeautifulSoup**.

Easily collect:

* 🖼️ Image URLs
* 🏷️ Tags
* ❤️ Likes
* 💬 Comments

and export everything into a clean CSV dataset.

---

## ✨ Features

✅ Scrapes stock image URLs automatically
✅ Extracts image tags and metadata
✅ Collects likes & comments count
✅ Handles infinite scrolling websites
✅ Saves scraped data into CSV format
✅ Beginner-friendly and easy to customize

---

## 🛠️ Built With

* **Python**
* **Selenium**
* **BeautifulSoup4**
* **Pandas**
* **Requests**
* **tqdm**

---

## 🌐 Target Website

```bash
https://stock-pictures.netlify.app
```

---

## ⚙️ Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/stock-image-scraper.git
cd stock-image-scraper
```

### 2️⃣ Install Required Libraries

```bash
pip install requests pandas tqdm selenium beautifulsoup4 chromedriver-binary
```

---

## ▶️ How to Run

```bash
python scraper.py
```

The scraper will:

* Open the website automatically
* Scroll through the page dynamically
* Extract image data and metadata
* Generate a CSV file containing all results

---

## 📊 Output

The generated dataset contains:

| Field         | Description        |
| ------------- | ------------------ |
| 🖼️ Image URL | Direct image link  |
| 🏷️ Tags      | Image category/tag |
| ❤️ Likes      | Number of likes    |
| 💬 Comments   | Number of comments |

---

## 🚀 Future Improvements

* 📥 Automatic image downloading
* ⚡ Multi-threaded scraping
* 🗄️ Database integration (MongoDB/MySQL)
* 🖥️ GUI/Desktop version
* 📁 Export to JSON format
* ☁️ Cloud deployment support

---

## 📚 What You’ll Learn

This project helps you understand:

* Web scraping fundamentals
* Browser automation using Selenium
* Parsing HTML with BeautifulSoup
* Handling infinite scrolling pages
* Data collection & CSV generation
* Real-world scraping workflows

---

## ⚠️ Disclaimer

This project is developed for **educational purposes only**.
Please respect the website’s terms of service before scraping any content.

---

## 📄 License

This project is licensed under the **MIT License**.

---

## ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub!
