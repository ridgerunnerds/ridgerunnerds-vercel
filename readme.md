# Calgary Tax Sale Properties

Migrated from [PythonAnywhere](https://ridgerunnerds.pythonanywhere.com/) to Vercel.

## Overview

Access Calgary's annual property tax sale auction list with real-time updates, street view photos, and detailed property information for investors.

## Tech Stack

- **Frontend:** React SPA (static build)
- **Backend API:** Vercel Serverless Functions (`/api/contact`)
- **Analytics:** Vercel Web Analytics & Speed Insights
- **Hosting:** Vercel

## Project Structure

```
├── api/
│   └── contact.js          # Contact form API endpoint
├── assets/
│   ├── index-ypvK7Op_.js   # Main JS bundle
│   └── index-CsZxpd5M.css  # Main CSS bundle
├── properties/
│   └── {id}/
│       ├── thumbnail.jpg
│       ├── detail.jpg
│       └── large.jpg
├── index.html              # Entry point (with Vercel Analytics)
├── vercel.json             # SPA routing & config
└── package.json
```

## Local Development

```bash
# Install Vercel CLI
npm i -g vercel

# Run locally
vercel dev
```

## Deployment

```bash
# Deploy to production
vercel --prod
```

## Analytics

Vercel Web Analytics and Speed Insights are enabled via script tags in `index.html`. Make sure to enable these features in your [Vercel Dashboard](https://vercel.com/dashboard) for this project.

## Contact API

- **Endpoint:** `POST /api/contact`
- **Body:** `{ name, email, subject, message }`
- **Returns:** `{ success: true, message: "Message sent successfully" }`

> **Note:** The contact API currently logs submissions to the console. Integrate your preferred email provider (Resend, SendGrid, etc.) in `api/contact.js` to send actual emails.
