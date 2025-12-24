# BeyondChats Article Scraper & Rewriter

## 📌 Overview
This project automatically improves blog articles by:
- Finding top-ranking competitor articles
- Scraping their content
- Rewriting/enriching existing articles
- Saving improved content back to the database

## 🛠 Tech Stack
- Laravel (Backend API)
- Node.js (Scraper & Rewriter)
- MySQL (Database)
- Axios & Cheerio (Scraping)

## 📐 Architecture
Node.js fetches articles from Laravel API, searches Google/DuckDuckGo for top-ranking competitors, scrapes and rewrites content, then updates Laravel via REST API.

## 🚀 How It Works
1. Laravel stores base articles
2. Node.js fetches articles via `/api/articles`
3. Search engine finds top results
4. Competitor content scraped
5. Content rewritten
6. Updated article sent back via `PUT /api/articles/{id}`

## ▶️ How to Run

### Backend
```bash
cd backend-laravel
php artisan migrate
php artisan serve
