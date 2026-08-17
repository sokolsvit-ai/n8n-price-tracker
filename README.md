# 🛒 n8n Price Tracker & Alert System

An automated e-commerce price-tracking workflow built in **n8n** that scrapes product prices, compares historical data using **PostgreSQL**, and sends instant price-drop alerts via **Telegram**.

## 🏗 Workflow Architecture
1. **Schedule Trigger:** Runs the tracking process automatically on a regular schedule.
2. **HTTP Request:** Fetches the target product page from the online store.
3. **HTML Extract:** Parses the raw HTML to pull out the current product price.
4. **PostgreSQL (Select):** Queries the database to retrieve the previous/historical price for comparison.
5. **Code Node:** Processes data and calculates the price difference percentage.
6. **PostgreSQL (Insert):** Saves the new price entry into the database.
7. **If Node:** Evaluates whether a price drop condition is met (`true`/`false`).
8. **Telegram Bot:** Sends an alert notification straight to your chat if a price drops.

## 🛠 Tech Stack
- **Automation:** n8n
- **Database:** PostgreSQL
- **Notifications:** Telegram Bot API
- **Data Extraction:** HTML Extract & Custom Code Logic

## 🚀 How to Use
1. Import the `workflow.json` file into your n8n instance.
2. Configure your **PostgreSQL** database credentials.
3. Set up your **Telegram Bot** token and chat ID.
4. Update the target URL in the **HTTP Request** node and adjust the CSS selectors in the **HTML Extract** node.

📩 **Contact & Custom Solutions:** [My Telegram Channel - Workflow & Scripts ](https://t.me/vladiksonchik)
