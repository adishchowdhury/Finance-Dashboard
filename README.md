# Finance-Dashboard
A clean, interactive, and responsive finance dashboard built to track and understand financial activity. This project was developed as a frontend evaluation assignment, focusing on UI/UX design, component structure, and client-side state management.

## ✨ Features

### Core Functionality
* **Dashboard Overview**: Summary cards displaying Total Balance, Total Income, and Total Expenses.
* **Data Visualization**: 
  * Bar chart comparing Income vs. Expenses over time.
  * Pie chart showing a breakdown of spending by category.
* **Transactions Management**: 
  * View a detailed list of transactions (Date, Description, Category, Type, Amount).
  * Search transactions by description or category.
  * Filter transactions by type (Income/Expense/All).
* **Role-Based UI**: Toggle between `Viewer` (read-only) and `Admin` (can add, edit, and delete transactions) modes to simulate RBAC on the frontend.
* **Smart Insights**: Automatically calculates the highest spending category, month-over-month expense comparisons, and provides dynamic observations based on spending trends.

### Enhancements Included
* **Dark Mode**: Fully supported dark/light theme toggle.
* **Data Persistence**: Transactions and user roles are saved to `localStorage` so data isn't lost on refresh.
* **Animations**: Smooth page transitions and component entrances powered by `framer-motion`.
* **Responsive Design**: Mobile-first approach ensuring the dashboard looks great on phones, tablets, and desktops.

## 🛠️ Tech Stack

* **Framework**: React 19 with TypeScript (via Vite)
* **Styling**: Tailwind CSS v4
* **UI Components**: shadcn/ui (Radix UI primitives)
* **State Management**: Zustand (with `persist` middleware)
* **Charts**: Recharts
* **Icons**: Lucide React
* **Date Formatting**: date-fns
* **Animations**: Framer Motion

## 🚀 Getting Started

### Prerequisites
Make sure you have [Node.js](https://nodejs.org/) (v18 or higher) installed.

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd finance-dashboard
Install dependencies:
code
Bash
npm install
Start the development server:
code
Bash
npm run dev
Open your browser and navigate to http://localhost:3000 (or the port provided in your terminal).
📁 Project Structure
code
Text
src/
├── components/
│   ├── ui/                   # Reusable shadcn/ui components (Buttons, Cards, Inputs, etc.)
│   ├── DashboardOverview.tsx # Summary cards and Recharts visualizations
│   ├── Insights.tsx          # Analytical insights and month-over-month comparisons
│   ├── RoleSwitcher.tsx      # Dropdown to toggle between Admin and Viewer roles
│   ├── ThemeToggle.tsx       # Dark/Light mode toggle
│   ├── TransactionForm.tsx   # Modal form for adding/editing transactions
│   └── TransactionsSection.tsx # Data table with search, filter, and CRUD actions
├── lib/
│   └── utils.ts              # Utility functions (e.g., Tailwind class merging)
├── store/
│   └── useFinanceStore.ts    # Zustand store for global state and localStorage persistence
├── types/
│   └── index.ts              # TypeScript interfaces and types
├── App.tsx                   # Main application layout and tab routing
├── index.css                 # Global CSS and Tailwind directives
└── main.tsx                  # React entry point
