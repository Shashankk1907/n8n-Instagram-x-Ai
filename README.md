
# 📸 n8n-Instagram-x-Ai

This n8n workflow scrapes the **latest 13 Instagram posts** from any handle, generates structured post data (caption, likes, comments, date, thumbnail), and **uploads it to Airtable** in a clean, visual format using Gallery View.

---

## 🚀 Features
- 🔎 Scrapes recent public posts via BrightData API
- 🖼️ Automatically uploads thumbnails to Airtable as attachments
- ✅ Out-of-the-box execution — no setup needed after import

---

## ⚙️ Setup

### 🔧 Required Environment Variables (already embedded for demo)
| Variable               | Used For             | Notes                        |
|------------------------|----------------------|-------------------------------|
| `BRIGHTDATA_API_KEY`   | Instagram scraping   | (embedded)                   |
| `AIRTABLE_API_KEY`     | Airtable API         | (embedded)                   |

📁 These are prefilled with **free-tier tokens** for demo purposes. You may replace them with your own.

---

## 🧪 How to Use

1. **Import the `.json` file into your n8n**
2. **Trigger manually**, or set up a `chat`-based or webhook input (e.g., enter `openai`)
3. Wait ~30 seconds for full scrape
4. ✅ Airtable will show a visual gallery of the scraped posts

---

## 📉 API Quota Limits

| API       | Limit Type          | Free Tier Notes                    |
|-----------|---------------------|------------------------------------|
| BrightData| Per scrape trigger  | ~1000/month (free proxy account)   |
| Airtable  | Records + API calls | 1000 records/base (free)           |

> You can run this workflow ~30–40 times/month comfortably under free tiers.

---

## 💡 Notes
- Airtable attachment fields are auto-filled using direct image URLs
