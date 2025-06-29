# IMDb Data Extractor 🎬

A lightweight yet powerful command‑line tool that **scrapes key metadata from any IMDb movie page**, downloads the poster, grabs the trailer link, and neatly shows the storyline.  

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| **Poster Downloader** | Saves the official movie poster as **`poster.jpg`** |
| **Trailer Link Finder** | Prints the first available trailer URL |
| **Metadata Extraction** | Title, genres, directors, cast (top 10), and IMDb rating |
| **Clean, Extensible Code** | Only ~50 lines, powered by `requests` + `BeautifulSoup` |

---

## 🔧 Tech Stack

- [`requests`](https://pypi.org/project/requests/) – HTTP requests  
- [`beautifulsoup4`](https://pypi.org/project/beautifulsoup4/) – HTML parsing  
- Built‑in `json`, `argparse`, `os` (no heavyweight deps)

---

## 📦 Installation

```bash
# 1 – Clone the repo
git clone https://github.com/your‑username/imdb-data-extractor.git
cd imdb-data-extractor

# 2 – Create (optional) virtual environment
python -m venv venv
source venv/bin/activate   # or venv\Scripts\activate on Windows

# 3 – Install dependencies
pip install -r requirements.txt
```

---

## 🚀 Usage

```bash
python imdb_scraper.py "https://www.imdb.com/title/tt1375666/"
```

Example output:

```
Storyline:
 A thief who steals corporate secrets through dream-sharing technology ...
✔️ Poster saved as poster.jpg

Genre: Action, Sci‑Fi, Thriller

🎬 Directors: Christopher Nolan
👥 Cast: Leonardo DiCaprio, Elliot Page, Tom Hardy, Joseph Gordon‑Levitt, Ken Watanabe
⭐ IMDb Rating: 8.8

Trailer link: http://www.imdb.com/video/vi4219471385/
```

Files created:

```
poster.jpg
```

---

## 🗂️ Project Structure

```
imdb_scraper.py        # Main script
requirements.txt       # Dependencies
README.md              # This file
```

---

## 🧩 How It Works

1. **Validate** the IMDb URL (`/title/tt…`).  
2. **Download** the page using a browser‑like User‑Agent.  
3. **Parse** embedded `application/ld+json` block for structured data.  
4. **Extract** poster (`image`), storyline (`description`), ratings, etc.  
5. **Save** poster image; print the rest to stdout.

---

## 📄 License

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.

---

> **Made with ☕ &nbsp;and a love for movies.**
