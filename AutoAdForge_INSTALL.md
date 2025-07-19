
# AutoAdForge – INSTALL.md

## 🚀 Overview

AutoAdForge is a full-stack SaaS platform that automates ecommerce marketing across platforms like Google Ads, Meta, TikTok, YouTube, Microsoft Ads, and more. It features a Canva-like drag-and-drop UX for ad creation, post scheduling, and email marketing.

---

## 🧱 Stack Summary

- **Frontend**: React (Next.js), Tailwind CSS, Fabric.js / Konva
- **Backend**: Node.js + Express (or FastAPI)
- **AI Layer**: OpenAI Codex (ad copy, captions, email content)
- **Database**: PostgreSQL + Prisma, Redis (for scheduling)
- **Integrations**: Google Ads, Meta Ads, TikTok Ads, Microsoft Ads, YouTube, Shopify, Klaviyo/Mailchimp
- **Auth**: OAuth2 + social/email login
- **Media Storage**: Cloudinary or AWS S3
- **Analytics**: Mixpanel or Plausible

---

## 📁 Folder Structure

```
AutoAdForge/
│
├── frontend/                # Next.js + Tailwind UI
├── backend/                 # Node.js server
├── ai/                      # AI prompts, OpenAI integration
├── integrations/           # API connectors (Google, Meta, etc.)
├── database/               # Prisma schema + migrations
├── services/               # Shared utility services
└── README.md
```

---

## 🔧 Setup Instructions

### 1. Clone Repo and Initialize

```bash
git clone https://github.com/yourusername/AutoAdForge.git
cd AutoAdForge
```

### 2. Install Frontend

```bash
cd frontend
npx create-next-app .
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

### 3. Install Backend

```bash
cd ../backend
npm init -y
npm install express cors dotenv axios openai pg redis
```

### 4. Setup AI Services

```bash
cd ../ai
touch openaiClient.js
# Implement OpenAI wrapper to generate ad copy, captions, emails
```

### 5. Prisma Setup

```bash
cd ../database
npm install prisma --save-dev
npx prisma init
# Configure schema.prisma for User, Campaign, Creative, Post
```

---

## 🔌 OAuth & API Integration

Set up OAuth flows for:
- Google Ads
- Meta Ads
- TikTok Business
- Microsoft Ads
- YouTube
- Shopify
- ESPs (Mailchimp, Klaviyo)

Store tokens securely using Redis or encrypted DB.

---

## 🎨 Drag-and-Drop Editor (Optional)

Install in `frontend/components/Editor.js`:

```bash
npm install fabric
# or
npm install react-konva konva
```

---

## 📅 Post Scheduler + Email Builder

- Add Calendar view to manage post frequency
- Generate captions via OpenAI
- Drag & drop email templates for promotions, cart recovery, etc.

---

## 📊 Reporting Dashboard

Integrate charts with:
- CTR, CPC, ROI
- Platform-specific KPIs
- Sort by performance

---

## ✅ MVP Feature Checklist

- [x] AI-powered ad generation
- [x] Drag-and-drop post/email editor
- [x] Post scheduler w/ caption assistant
- [x] Shopify product sync
- [x] OAuth + campaign launch for Google/Meta/TikTok
- [x] Basic reporting dashboard

---

## 🧠 Need help with:

- `README.md` formatting for GitHub
- Prebuilt schema for Prisma
- Drag-and-drop image editor
- Serverless deployment (Render, Vercel)

Let me know!
