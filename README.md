# 💰 Personal Finance Dashboard

A clean, modern, fully client-side Personal Finance Dashboard built with **HTML**, **CSS**, and **Vanilla JavaScript** — no backend, no database, no build step required.

![screenshot](https://raw.githubusercontent.com/bingethecode4u/personal-finance-dashboard/main/preview.png)

## ✨ Features

- **Add transactions** — income or expense, with amount, category, date, and optional note
- **Summary cards** — live totals for balance, income, and expenses
- **Transaction history** — sorted newest-first, color-coded, with delete support
- **Filters** — filter by type (pill toggle), category, and month; one-click "Clear filters"
- **Charts (Chart.js)**
  - Bar chart: Income vs Expenses — last 6 months
  - Doughnut chart: Expenses by category with percentage breakdown
- **Export JSON** — download all transactions as a formatted `.json` file
- **Import JSON** — merge transactions from a previously exported file (validates & deduplicates)
- **LocalStorage persistence** — data survives page refreshes automatically

## 🚀 Getting Started

No installation needed.

```bash
git clone https://github.com/bingethecode4u/personal-finance-dashboard.git
cd personal-finance-dashboard
```

Then just open `index.html` in any modern browser:

```bash
# macOS / Linux
open index.html

# Windows
start index.html
```

Or use the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) VS Code extension for a better development experience.

## 📁 Project Structure

```
personal-finance-dashboard/
├── index.html   # Entire app — HTML + CSS + JS in one file
└── README.md
```

## 📦 Dependencies

| Library | Version | Loaded via CDN |
|---------|---------|----------------|
| [Chart.js](https://www.chartjs.org/) | 4.4.3 | ✅ |

No npm, no bundler, no framework.

## 🗂️ Data Format (Import / Export)

Transactions are stored as a JSON array. Each item follows this shape:

```json
{
  "id": "lcy3x2abc",
  "type": "expense",
  "amount": 42.50,
  "category": "Food",
  "date": "2026-04-26",
  "note": "Lunch with team"
}
```

| Field | Type | Required | Notes |
|-------|------|----------|-------|
| `id` | string | ✅ | Unique identifier (used for dedup on import) |
| `type` | `"income"` \| `"expense"` | ✅ | |
| `amount` | number > 0 | ✅ | |
| `category` | string | ✅ | |
| `date` | string (YYYY-MM-DD) | ✅ | |
| `note` | string | ❌ | Max 100 chars |

## 📜 License

[MIT](LICENSE) © 2026 bingethecode4u
