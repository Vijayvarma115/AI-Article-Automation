# 🧠 AI Article Automation Workflow

This project automates the generation and delivery of weekly AI-related articles using **n8n**, a powerful workflow automation tool. It integrates external APIs, leverages LLMs, and sends styled HTML emails directly to your inbox.

---

## 🚀 Features

- ⏰ **Scheduled Trigger** – Runs every Monday at 10:00 AM
- 📰 **NewsAPI Integration** – Fetches the latest articles on "Artificial Intelligence"
- 🧠 **LLM-Based Article Generation** – Uses `meta-llama/llama-4-scout-17b` via Groq for creating 600-word articles
- 💡 **Prompt Engineering** – Simulates a seasoned AI writer for article generation
- 🖼 **HTML Formatting** – Converts plain text into responsive, styled HTML
- 📧 **Gmail Integration** – Sends the article to your email inbox as a newsletter

---

## 🛠 Technologies Used

- [n8n](https://n8n.io/) – Workflow automation
- [NewsAPI](https://newsapi.org/) – Real-time article sources
- [Groq](https://groq.com/) – LLM API (Meta LLaMA backend)
- JavaScript – Data parsing and HTML formatting
- Gmail API – OAuth2 authenticated email delivery

---

## Workflow

![image](https://github.com/user-attachments/assets/026c39a3-5500-46a9-af71-16877032dbfe)

## 🔧 Workflow Breakdown

1. **Trigger**: `Schedule Trigger` runs the workflow weekly.
2. **Fetch Articles**: `HTTP Request` to NewsAPI fetches the latest AI news.
3. **Select Topic**: `Code Node` randomly selects one article title as the article topic.
4. **Generate Article**: `LLM Chain` sends a prompt to Groq to generate a professional article.
5. **Format HTML**: `Code Node` formats the article into a styled HTML email.
6. **Send Email**: `Gmail Node` sends the email with subject: _“🚀 Weekly AI Article - DeepSeek Movement”_.

---

## Output

![image](https://github.com/user-attachments/assets/1416d573-e8b4-4f4d-a9b5-e00cffa6748e)

## 📌 Future Enhancements

- Archive articles to Notion or Google Drive
- Add topic filtering or quality control
- Include summaries or TL;DR sections

---

## 🧠 Lessons Learned

- How to orchestrate data flow and logic using n8n
- Prompt design for high-quality LLM outputs
- Dynamic HTML email formatting with JavaScript
- Integration with third-party APIs using tokens and OAuth

---

## 📩 Example Output

> A weekly email with a clean, professional AI article, automatically generated and beautifully formatted.

---

## 🤝 Contributing

Feel free to fork, improve, or contribute ideas to this automation. PRs are welcome!

---

## 📜 License

MIT License – see [LICENSE](LICENSE) for details.
