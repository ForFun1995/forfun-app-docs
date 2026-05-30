---
title: Privacy Policy
---

# Privacy Policy

_Last updated: 2026-05-26_

Hangar4 ("we," "us," "the app") is a Gunpla deal-tracking mobile app that scans publicly available retailer listings and surfaces deals matching your watchlists. This Privacy Policy describes what data we collect, how we use it, and your rights.

## 1. What we collect

When you use Hangar4, we collect the following:

- **Account information** — your email address and a hashed password (or, if you sign in with Apple, a pseudonymous Apple ID identifier). Stored in Supabase Auth.
- **Watchlists you create** — the plain-English descriptions of items you want to track (e.g., "RG Unicorn under $80") and the parsed criteria derived from them. Stored in our Supabase database, scoped to your account.
- **Deal matches** — listings our AI scored against your watchlists, including the score, summary, and your 👍/👎 feedback when you provide it.
- **Push notification token** — if you grant notification permission, an Expo Push token associated with your account so we can deliver deal alerts.
- **Crash and error reports** — when the app encounters an error, we send a stack trace and breadcrumb history to Sentry. We strip IP addresses from these reports.
- **Feedback submissions** — when you use the in-app Settings → Send Feedback flow, your category choice, message, app version, and platform (iOS) are stored in our Supabase database. Your identity is associated via your user ID.

We do **not** collect: your real name (unless you put it in your email), location data, contacts, calendar, photos, microphone audio, or any other device-level data.

## 2. How we use your data

We use the data we collect to:

- Score retailer listings against your watchlists using OpenAI's GPT-4o mini model.
- Deliver push notifications when deals match your criteria.
- Improve the app based on feedback submissions and error reports.
- Authenticate your sessions so only you can see your watchlists and deals.

We do **not** sell or share your data with advertisers. We do not run ads in the app.

## 3. Third parties

Hangar4 relies on the following third-party services to function:

- **Supabase** (database, authentication, email delivery) — your account credentials, watchlists, opportunities, push tokens, and feedback are stored on Supabase infrastructure.
- **OpenAI** — the canonical name and price of each candidate listing are sent to OpenAI's API for scoring. Your watchlist text is also included so the model can judge match quality. OpenAI's API does not train on this data by default.
- **Apple Push Notification Service (APNs)** — for delivering notifications to your iOS device. Apple does not see the contents of our notifications beyond what's needed to deliver them.
- **Sentry** — crash reports and error events. Sentry sees your app version, device model, and the stack trace at the moment of an error.
- **Browserbase** — used to scrape one retailer (BBTS) that requires a JavaScript-rendered browser session. No user data is sent to Browserbase.

Retailer listings we display are scraped from publicly accessible storefronts. We do not have any data exchange agreement with those retailers.

## 4. Data retention and deletion

- **Active data**: kept while your account is active.
- **Opportunities**: deals are marked "expired" 7 days after creation, or sooner if the underlying listing goes out of stock. Expired rows remain in the database but are hidden from the app.
- **Account deletion**: if you delete your account (or we delete it on your request), every row tagged with your user ID is automatically cascade-deleted from our database. This includes your watchlists, opportunities, push tokens, and feedback. To request deletion, email the address below.

## 5. Your rights

You can:

- Sign out at any time (Settings → Sign Out).
- Request account deletion via the contact email below.
- Request a copy of your data (export via SQL query on our side).
- Withdraw consent for push notifications via iOS Settings → Notifications → Hangar4.

If you are a resident of the European Economic Area (GDPR), the UK, or California (CCPA/CPRA), additional rights apply including the right to object to processing, request rectification, and lodge a complaint with your supervisory authority.

## 6. Security

We protect your data with industry-standard measures:

- Supabase encrypts data at rest and in transit (TLS).
- Passwords are hashed with bcrypt; we never see your plaintext password.
- Database access is scoped per-user via Row-Level Security policies.
- The mobile app uses Apple's Keychain for token storage on iOS.

No system is perfectly secure. If we become aware of a breach affecting your data, we will notify you via email as required by applicable law.

## 7. Children

Hangar4 is not directed at children under 13. We do not knowingly collect data from children under 13. If you believe a child has provided data to us, please contact us so we can delete it.

## 8. Changes to this policy

We may update this policy as the app evolves. Material changes will be announced in-app or via email. The "Last updated" date at the top reflects the current version.

## 9. Contact

For privacy-related questions, account deletion requests, or any other concerns, contact:

**Jose Mercado** — hangar4beta@gmail.com
