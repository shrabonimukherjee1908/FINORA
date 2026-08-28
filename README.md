# Finora — Intelligent Personal Finance OS 💎

> **Finora** is a privacy-first, startup-grade personal finance and expense management application designed to bring calm, immediate clarity to your everyday capital flow. Built with pure HTML5, CSS3, and modern Vanilla JavaScript, Finora operates 100% offline with zero build steps or external runtime dependencies.

![Finora Preview Banner](https://images.unsplash.com/photo-1554224155-8d04cb21cd6c?auto=format&fit=crop&w=1200&q=80)

---

## 🌟 Key Highlights & Philosophy

- **Zero-Dependency Architecture**: Runs natively in any browser directly or via a lightweight static server.
- **Privacy First**: 100% of your financial data lives locally in your browser’s `localStorage`. No trackers, no backend required.
- **Data-Driven Smart Insights**: Computes true statistical spending velocity, weekend vs. weekday patterns, largest expenses, and Month-over-Month (MoM) pace.
- **Precision Design System**: Fully responsive UI with custom CSS tokens, native dark mode, smooth micro-interactions, and accessible focus states.
- **Seamless Data Portability**: Export your transactions to formatted CSV (Excel/Sheets ready) and download/restore full JSON state backups.

---

## 🚀 Core Features

### 1. 📊 Executive Dashboard
- **Dynamic Time Greeting**: Contextual greeting (`Good evening, Shraboni 👋`) with real-time spending pace assessment.
- **Four Core Financial Metrics**: Total Balance, Monthly Income, Monthly Expenses, and Net Savings Rate with trend badges.
- **Monthly Spending Pace**: Real-time progress bar reflecting monthly baseline consumption.
- **Smart Insights Engine**: Real-time data-driven statistical cards analyzing your actual transaction history.
- **Recent Activity Stream**: Grouped recent transactions with 1-click edit, delete, and undo toast support.
- **Active Subscriptions Mini-Widget**: Upcoming recurring payments overview.

### 2. ↔️ Interactive Transactions Hub
- **Instant Search**: Real-time debounce search matching merchants, notes, categories, and amounts.
- **Multi-Faceted Filtering**: Filter concurrently by **Type** (*Expense / Income / Transfer*), **Category** (*12 distinct sectors*), **Payment Method** (*UPI / Card / Cash / Bank*), and **Date Range**.
- **Smart Grouping**: Transactions seamlessly grouped into `Today`, `Yesterday`, `This Week`, and `Earlier`.
- **Keyboard Shortcuts**: Press <kbd>N</kbd> or <kbd>+</kbd> anywhere to trigger the quick Add Transaction modal.

### 3. 📈 High-DPI Visual Analytics
- **Spending Trajectory Line/Area Chart**: Canvas-based smooth quadratic bezier curve chart with gradient fill.
- **Category Donut Breakdown**: High-DPI interactive donut chart with center total and detailed legend.
- **Month-over-Month (MoM) Bar Chart**: Side-by-side comparative visualization of current vs previous month income and outflow.
- **Ranked Category Leaderboard**: Ranked spending leaderboard with percentage shares and progress bars.
- **Time Periods**: Toggle between *This Month*, *Last Month*, *Last 90 Days*, and *Year-to-Date (YTD)*.

### 4. 🎯 Category Budgeting
- **Visual Budget Cards**: Spent vs limit progress gauges (`₹5,000 / ₹7,000` • `71% used`).
- **Dynamic Status Thresholds**: Automatically flags budgets as **On Track** (Green), **Near Limit 80%** (Amber), or **Exceeded** (Crimson).
- **Full CRUD**: Create, customize, edit thresholds, and delete category budgets.

### 5. 🔄 Recurring Bills & Subscriptions
- **Fixed Commitment Calculator**: Computes exact monthly fixed subscription load (Netflix, Rent, Internet, Gym, Spotify).
- **Status Toggles**: Pause or activate subscriptions anytime.
- **Next Due Tracker**: Automatic countdown to next renewal date.

### 6. 🗓️ Financial Calendar Matrix
- **Daily Cashflow Grid**: Full monthly calendar view showing days with active expenses.
- **Day Drill-Down**: Click any date cell to reveal that day's specific itemized receipts and instant quick-add.

### 7. ⚙️ Preferences & Data Portability
- **Currency Switcher**: Instant switching between `₹ INR`, `$ USD`, `€ EUR`, `£ GBP`, `¥ JPY`, `C$ CAD`, `A$ AUD`, and `AED`.
- **Dark Mode Support**: Seamless toggle between *Light*, *Dark*, and *System OS Preference*.
- **Data Export/Import**: One-click CSV export, JSON backup download, and JSON restore.
- **Demo Data vs Clean Slate**: Switch between rich demo mode and a clean starting state.

---

## 🛠️ Tech Stack & Architecture

```
finora-app/
├── index.html              # Semantic HTML5 shell with accessible modals & templates
├── css/
│   ├── main.css            # Design tokens, typography, dark/light themes, animations
│   ├── layout.css          # Desktop sidebar, top header, mobile bottom navigation
│   ├── components.css      # Reusable cards, inputs, buttons, chips, toasts, empty states
│   └── views.css           # View grids (Dashboard, Transactions, Analytics, Budgets, etc.)
├── js/
│   ├── app.js              # Application coordinator, router, keyboard shortcuts
│   ├── store.js            # Reactive LocalStorage state store with full mutation logic
│   ├── utils.js            # Currency & date formatters, sanitization, debounce, downloads
│   ├── insights.js         # Statistical insights engine (MoM velocity, weekend ratio)
│   ├── charts.js           # High-DPI Canvas charting engine (Area, Donut, Bar)
│   ├── components/
│   │   ├── modal.js        # Accessible modal & bottom-sheet controller
│   │   └── toast.js        # Non-intrusive toast notifications with Undo action
│   └── views/
│       ├── dashboard.js    # Executive summary & quick actions
│       ├── transactions.js # Multi-filter & date-grouped transaction manager
│       ├── analytics.js    # Visual charts and category rankings
│       ├── budgets.js      # Monthly category spending limits
│       ├── recurring.js    # Subscriptions & recurring commitments
│       ├── calendar.js     # Financial calendar matrix
│       └── settings.js     # Profile, theme, and CSV/JSON backups
└── README.md
```

---

## ⚡ How to Run Locally

Because Finora uses standard ES Modules, it can be served using any local web server or directly opened:

### Option 1: Using Python (Recommended)
```bash
cd finora-app
python -m http.server 8000
```
Then visit `http://localhost:8000` in your browser.

### Option 2: Using Node.js / npx
```bash
cd finora-app
npx serve .
```

### Option 3: VS Code Live Server
Right click `index.html` and click **"Open with Live Server"**.

---

## 🎨 Design System Specifications

| Token | Light Value | Dark Value | Description |
| :--- | :--- | :--- | :--- |
| `--primary-500` | `#6366F1` (Indigo) | `#818CF8` | Primary brand accent |
| `--bg-app` | `#F8FAFC` | `#0B0F19` | Main application background |
| `--bg-surface` | `#FFFFFF` | `#111827` | Elevated card surfaces |
| `--text-primary` | `#0F172A` | `#F8FAFC` | High-contrast body typography |
| `--success` | `#10B981` | `#10B981` | Inflow & positive trends |
| `--danger` | `#EF4444` | `#EF4444` | Outflow & budget exceedances |
| `--warning` | `#F59E0B` | `#F59E0B` | Near-limit budget warnings |

---

## 🔒 Privacy & Offline Guarantee

- **Zero Telemetry**: No third-party tracking scripts or remote analytics.
- **Offline First**: All assets and fonts are local/fallbacked. Once loaded, it functions 100% offline.
- **Data Retention**: Your financial records remain strictly within your device's browser sandbox.

