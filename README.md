# StockMarket App

A comprehensive stock market tracking application built with Next.js, featuring real-time data, personalized watchlists, and intelligent market insights. Track your favorite stocks, receive personalized news summaries, and stay informed with AI-powered market analysis.

[Live Demo](https://stockmarket-app-demo.vercel.app)

## Features

- 📈 **Real-time Stock Data** - Live stock prices and market data via Finnhub API
- 📊 **Interactive Charts** - TradingView widgets for advanced technical analysis
- 👤 **User Authentication** - Secure sign-up/sign-in with Better Auth
- 📋 **Personal Watchlists** - Add and manage your favorite stocks
- 📧 **AI-Powered News** - Daily personalized market news summaries via Inngest
- 🔍 **Stock Search** - Fast and intuitive stock symbol search
- 📱 **Responsive Design** - Mobile-first design with Tailwind CSS
- 🌙 **Dark Mode** - Professional dark theme for comfortable viewing
- ⚡ **Real-time Alerts** - Price and volume notifications for watchlist items

## Tech Stack

**Client:**

- Next.js 15 (App Router)
- React 18
- TypeScript
- Tailwind CSS
- ShadCN/UI Components
- TradingView Widgets

**Server:**

- Next.js API Routes
- MongoDB with Mongoose
- Better Auth (Authentication)
- Inngest (Background Jobs)
- Nodemailer (Email Service)

**APIs & Services:**

- Finnhub API (Market Data)
- Google Gemini API (News Summarization)
- Inngest (Scheduled Jobs)

## Run Locally

Clone the project

```bash
git clone https://github.com/ErenSahbaz1/StockMarketApp
```

Navigate to project directory

```bash
cd StockMarketApp
```

Install dependencies

```bash
npm install
```

Set up environment variables

```bash
cp .env.example .env.local
```

Fill in your environment variables:

```env
NODE_ENV='development'
NEXT_PUBLIC_BASE_URL=http://localhost:3000

# Database
MONGODB_URI=your_mongodb_connection_string

# Better Auth
BETTER_AUTH_SECRET=your_auth_secret
BETTER_AUTH_URL=http://localhost:3000

# Finnhub API
NEXT_PUBLIC_FINNHUB_API_KEY=your_finnhub_api_key


# Email (Nodemailer)
NODEMAILER_EMAIL=your@email.com
NODEMAILER_PASSWORD=yourpassword

# Gemini
GEMINI_API_KEY=your_openai_api_key
```

Start the development server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Documentation

**Core Technologies:**

[Next.js](https://nextjs.org/docs) - React framework with App Router for server-side rendering and API routes. Used throughout the application for routing, server components, and API endpoints.

[Better Auth](https://better-auth.com/) - Modern authentication library for Next.js. Handles user registration, login, and session management in `/lib/better-auth/auth.ts`.

[MongoDB & Mongoose](https://mongoosejs.com/) - Database and ODM for user data and watchlists. Schema definitions in `/database/models/`.

[Finnhub API](https://finnhub.io/docs/api) - Real-time stock market data provider. Integration in `/lib/actions/finnhub.actions.ts` for stock prices, company info, and market news.

[TradingView Widgets](https://www.tradingview.com/widget/) - Professional financial charts and market data visualization. Configuration in `/lib/constants.ts` and implementation in `/components/TradingViewWidget.tsx`.

[Inngest](https://www.inngest.com/) - Serverless queue for background jobs. Handles scheduled news emails and user onboarding in `/lib/inngest/functions.ts`.

**UI & Styling:**

[Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS framework for responsive design and dark mode theming.

[ShadCN/UI](https://ui.shadcn.com/) - Modern React component library. Components in `/components/ui/` for forms, tables, buttons, and modals.

[React Hook Form](https://react-hook-form.com/) - Form validation and management in authentication and user input components.

**Email & Communication:**

[Nodemailer](https://nodemailer.com/) - Email service for welcome emails and daily news summaries. Templates and configuration in `/lib/nodemailer/`.

[Gemini API](hhttps://cloud.google.com/apis) - AI-powered news summarization and personalized content generation via Inngest functions.

## Project Structure

```
├── app/                    # Next.js App Router
│   ├── (auth)/            # Authentication pages
│   ├── (root)/            # Protected dashboard pages
│   └── api/               # API routes
├── components/            # Reusable React components
│   ├── forms/            # Form components
│   └── ui/               # ShadCN UI components
├── database/             # MongoDB models and connection
├── lib/                  # Utilities and services
│   ├── actions/          # Server actions
│   ├── better-auth/      # Authentication config
│   ├── inngest/          # Background job functions
│   └── nodemailer/       # Email services
├── hooks/                # Custom React hooks
├── middleware/           # Next.js middleware
└── types/               # TypeScript type definitions
```

## Author

[**Eren Sahbaz**](https://github.com/ErenSahbaz1)

MCT Student @ Erasmushogeschool Brussel

Languages: Dutch, Turkish, English, French

Contact: eren.sahbaz@student.ehb.be / nendari01@gmail.com


## Extra's

- **AI-Powered Insights**: Personalized news summaries based on your watchlist
- **Professional Charts**: Advanced technical analysis with TradingView integration
- **Email Notifications**: Daily market updates and personalized welcome emails
- **Real-time Data**: Live stock prices and market movements
- **Mobile Optimized**: Responsive design for trading on the go

---

