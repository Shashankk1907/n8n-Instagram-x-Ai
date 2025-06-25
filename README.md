
# 📸 n8n-Instagram-x-Ai

This n8n workflow scrapes the **latest 13 Instagram posts** from any handle, generates structured post data (caption, likes, comments, date, thumbnail), and **uploads it to Airtable** in a clean, visual format using Gallery View.

It also uses **AI-powered analysis** to review post performance based on likes, comments, and captions.

---

## 🚀 Features

* 🔎 Scrapes recent public posts via BrightData API
* 🖼️ Automatically uploads thumbnails to Airtable as attachments
* 🤖 AI generates short reviews for each post's performance
* ✅ Out-of-the-box execution — no setup needed after import

---

## ⚙️ Setup

### 🔧 Required Environment Variables (already embedded for demo)

| Variable             | Used For                           | Notes                                                    |
| -------------------- | ---------------------------------- | ---------------------------------------------------------|
| `BRIGHTDATA_API_KEY` | Instagram scraping                 | (embedded)                                               |
| `AIRTABLE_API_KEY`   | Airtable API                       | (embedded)                                               |
| `OPENAI_API_KEY`     | Post performance review (optional) | (free keys embedded)Add your own key to use your credits |

📁 These are prefilled with **free-tier tokens** for demo purposes. You may replace them with your own credentials for production use.

---

## 🧪 How to Use

1. **Import the `.json` file into your n8n**
2. **Trigger manually**, or set up a `chat`-based or webhook input (e.g., enter `openai`)
3. Wait \~30 seconds for full scrape and AI review
4. ✅ Airtable will show a visual gallery of the scraped posts
5. 💬 Each record now includes a **short AI-generated performance review**

---

## 📉 API Quota Limits

| API        | Limit Type          | Free Tier Notes                      |
| ---------- | ------------------- | ------------------------------------ |
| BrightData | Per scrape trigger  | \~1000/month (free proxy account)    |
| Airtable   | Records + API calls | 1000 records/base (free)             |
| OpenAI     | Prompt tokens       | Free credits available for new users |

> You can run this workflow \~30–40 times/month comfortably under free tiers.
> For OpenAI, add your key in the **Credentials section** in n8n under "OpenAI API".

---

## 💡 Notes

* Airtable attachment fields are auto-filled using direct image URLs
* Reviews are concise and based on likes, comments, and caption relevance
* All AI logic is handled inside an **Agent Node using OpenAI**

---
