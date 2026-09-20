# Souvik Kundu — BI & Automation Engineer

> **Self-taught. Solo. 25+ outlets. Everything — from POS data to dashboard to AI — built by one person.**

I design and run the complete data + AI stack for a multi-outlet family-entertainment chain across India. No data team, no enterprise tools budget. Just real business problems that needed solving, and whatever it took to solve them.

---

## The scale

<table>
<tr>
<td align="center"><b>25+</b><br><sub>outlets across India</sub></td>
<td align="center"><b>3</b><br><sub>POS systems unified</sub></td>
<td align="center"><b>25+</b><br><sub>analytics modules</sub></td>
<td align="center"><b>13+</b><br><sub>production systems</sub></td>
<td align="center"><b>1</b><br><sub>person</sub></td>
</tr>
</table>

---

## What I've built

### 📊 Real-Time BI Platform — 25+ analytics modules

I built a single-page analytics dashboard covering an entire entertainment chain — **25+ outlets, 2 brands, 3 POS systems unified into one source of truth**. Leadership now opens a browser instead of waiting on manual spreadsheet exports.

I reconciled **Semnox/Parafait** (arcade/wallet), **PetPooja** (F&B), and the internal activity API into a single trusted revenue definition. I diagnosed and fixed a POS API bug that silently **double-counted F&B revenue ~2× every night** — dashboard numbers now match source systems exactly. I migrated the full data layer to **Supabase/PostgreSQL + GitHub Actions** sync pipelines, eliminating the 10-second timeout failures on the previous cache system.

**Revenue & Operations**
- Revenue & Total Sales — per outlet, per company, per day; activity / F&B / combined views
- Footfall & Spend-per-Head — separates "more people" from "bigger spend"
- Time-wise & Hourly Sales — peak-hour identification with counter staffing recommendations
- Staffing Optimizer — peak-hour → recommended counter headcount, automated
- Voucher Analytics — denomination breakdown, usage, OTP funnel (14-day / 21-day cohorts)
- Socks Sale Pattern — attach-rate by package and store (paid sessions, net >₹60)
- Socks Ratio Maintenance — target vs actual attach-rate alert

**F&B Deep-Dive**
- F&B Compare — period A vs B across outlet / category / item / channel / payment method
- Menu Engineering Quadrant — Star / Plough-horse / Puzzle / Dog with editable food-cost %
- F&B Attach Rate — F&B revenue per guest beyond the activity ticket
- Day-Part Sales — breakfast / lunch / dinner / late-night breakdown
- Channel Economics — dine-in vs aggregator (Zomato / Swiggy) with commission P&L
- Discount & Void Leakage — reconciled to PetPooja source exactly

**Customer Intelligence**
- Cohort & RFM Retention — which acquisition months retain vs churn?
- Customer LTV & Cohort-Retention Triangle — lifetime value mapped by first-visit month
- Top Spenders — ranked client spend, filterable by date range and outlet
- Age Analysis — child/adult segmentation + age-band breakdown from 22,000+ customer DOBs

**Predictive & Intelligence**
- Forecasting & Accuracy — expected vs actual with model accuracy tracking
- Anomaly Detection — automated spike/dip alerts with deviation severity scores
- Weather-Sensitivity — live Open-Meteo API, rainfall and temperature vs revenue correlation
- Store Performance Prediction — forward projections with ML confidence bands
- Targets & Pulse — WoW / MoM / YoY deltas against editable RAG targets per KPI

**Operations & Compliance**
- SOP & CCTV Performance — store compliance scores with deviation-revenue linkage
- Deviations & Operations Monitor — automated flag → impact correlation
- Promotions Analysis — incentive programme ROI tracking

**Platform Features**
- Live Geo Map — all 25+ outlets on Leaflet.js, click-through to store detail
- Multi-company — Jus Jumpin (FEC) + The Knockout (sports bar) in one dashboard
- Multi-POS — Semnox/Parafait (arcade/wallet) + PetPooja (F&B) + internal activity API
- AI Assistant — ask questions in plain English via Gemini LLM (voice + text, live data context)
- Global Export — PDF and Excel from every single tab
- Daily Digest — automated 9am IST email to management via Brevo

---

### 🎤 ARIA — AI Interview System *(live in production)*

I built an async AI interview system deployed at `jusjumpin-hr-interviews.netlify.app`. Candidates answer in their own time → **Gemini LLM scores structured rubrics → hiring managers read one summary instead of listening to 40+ recorded calls per cycle**. Built on Netlify Functions + Google Drive storage.

---

### 🧮 Incentive Automation API

I built a REST API + dashboard that replaced a full day of monthly manual Excel work. **63,000+ voucher records, 25+ stores, per-store owner-active rule, 28 rate tiers, charm pricing** — all computed server-side. Month-end incentive calculation: **8 hours → one click**. When Netlify's 10-second function limit forced a clunky chunked-fetch workaround, I migrated the whole pipeline to **Cloudflare Workers** — the full month now pulls in one request in **4.4 seconds**, no chunking needed. Now a full multi-tab payout suite — non-voucher bonuses (birthday/feedback/review), a manual F&B/kitchen points entry tab for staff not captured by POS data, an HO consolidated report, and one Final Merge export combining every incentive type into a single payout sheet. Stack: `Cloudflare Workers` `Supabase` `PostgreSQL`.

---

### 💬 WhatsApp Birthday Marketing Engine

I built an escalating DOB-driven campaign engine for a **22,000+ customer base**. Sends personalised WhatsApp messages at **7 / 5 / 2 / 0 days before birthday** via `AiSensy API` — auto-generates unique offer codes from live POS DOB data, tracks redemption per customer. Zero manual steps after setup.

---

### 👤 HR & Attendance Systems

- **ESSL + GratyHR Astra integration** — biometric punch data auto-synced into GratyHR Astra HR software via API
- **ESSL Biometric API** — auto employee provisioning and automated monthly attendance reports
- **ESSL server login recovery** — diagnosed complete login failure on the iClock web server; traced root cause to SQL Server `essl` service account password auto-expiry; reset credentials via SSMS, ran `iisreset`, and disabled password-expiry policy on the service account to prevent recurrence. Attendance sync restored in under 10 minutes

---

### 🏦 Cashbook & Payments

- **Cashbook Dashboard** — per-store daily cash-closing form → Apps Script `doPost` webhook → central Google Sheet → HO consolidated view. Live across all 25+ outlets. Grand = Card + Cash + UPI + Excess; CashInHand = CashTotal − Deposits. Late submissions auto-flagged; immutable audit log per store.
- **Manual Payments Ledger** — grew from a bank-reconciliation tool into a 6-module finance system on the same Cloudflare Worker: Bills, Party Master, Bill↔Payment Matching, Manage P&L, **GST Ledger**, and **TDS Ledger**. `/upload` parses bank statements and classifies PSP entity names (BharatPe = "Resilient Innovations", Zomato = "Eternal Limited"); `/reconcile` runs a three-stage match engine (exact → overnight fuzzy → flag) with traffic-light status per store per day; GST/TDS ledgers ingest real statutory source formats (GSTR-2B's 12 state sheets, per-vendor Form 16A PDFs). Live at `jusjumpin-payments.green-king-ac34.workers.dev`. Zero infrastructure overhead — `wrangler deploy` in 30 seconds.

---

### 🎂 Birthday WhatsApp Automation

18,700+ child DOBs sitting unused in the POS. I built an escalating offer engine on top of them: a daily cron pulls upcoming birthdays, assigns time-sensitive discount codes (7 / 5 / 2 / 0 days before the party), and fires personalised WhatsApp messages via AiSensy. 703 upcoming birthdays in the next 30 days across 25+ outlets, zero manual work per week. First redemption wins; sibling codes void automatically. Ops console shows every upcoming birthday, filterable by store and status, with Excel/CSV export. Stack: `Node.js` `Netlify Functions` `AiSensy WhatsApp API` `POS DOB API`.

---

### 📞 Call Analysis CRM

I built a zero-manual AI call analysis pipeline: `FolderSync` → `Google Drive` → `Google Apps Script` → `Gemini LLM`. **30,000+ recordings backfilled**. New calls appear scored in the dashboard **within 60 seconds** of hanging up. Gemini scores pitch quality, objection handling, close attempt, and brand knowledge (0–10) — flagged calls auto-surface for manager coaching. ~10 salespeople, 3 brands, zero extra app installs required.

---

### 🎙️ AI Conduct Audit

I built a call-conduct monitor for the CCTV/security department: recordings sync in automatically, and **Gemini Flash audits the audio directly — no transcription step** — for rudeness or hostility from either party. Flagged calls surface to managers within ~15 minutes for review and action. Kept deliberately separate from the sales call-scoring system since the two serve different audiences with different sensitivity. Stack: `Google Apps Script` `Gemini API`.

---

### ⭐ Google Review AI

I built an automated Google My Business reply system across **3 brands** (Jus Jumpin / Stoneberry Resort / Knockout Sports Bar). `Gemini LLM` generates brand-voice replies personalised to each review. Ratings ≤2 stars → **instant escalation to outlet manager via WhatsApp** before the complaint compounds. Stack: `Node.js` `Gemini API` `Netlify Functions` `GBP API`.

---

## Tech stack

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat&logo=supabase&logoColor=white)
![LLM/Gemini](https://img.shields.io/badge/LLM%20%2F%20Gemini-412991?style=flat&logo=google&logoColor=white)
![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=flat&logo=netlify&logoColor=white)
![Cloudflare Workers](https://img.shields.io/badge/Cloudflare_Workers-F38020?style=flat&logo=cloudflare&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)

`JavaScript` · `Node.js` · `Python` · `PostgreSQL` · `Supabase` · `REST APIs` · `LLM / Gemini API` · `PetPooja POS API` · `Semnox / Parafait API` · `ESSL Biometric API` · `GratyHR Astra API` · `AiSensy WhatsApp API` · `ICICI Bank API` · `Brevo` · `Netlify Functions` · `Cloudflare Workers` · `GitHub Actions` · `Google Apps Script` · `Leaflet.js` · `Chart.js`

---

## Featured repos

| | Project | Stack |
|---|---|---|
| 📈 | **[FEC Analytics Platform](https://github.com/Souvikkundu369/fec-analytics-platform)** — full case study with architecture and engineering highlights | `Node.js` `Supabase` `JS` |
| 🎤 | **[ARIA AI Interview System](https://github.com/Souvikkundu369/aria-ai-interview)** | `Gemini` `Netlify` |
| 🧮 | **[Incentive Automation API](https://github.com/Souvikkundu369/incentive-automation-api)** | `Supabase` `REST API` |
| 💬 | **[WhatsApp Marketing Automation](https://github.com/Souvikkundu369/whatsapp-marketing-automation)** | `Node.js` `AiSensy` |
| ⭐ | **[Google Review AI](https://github.com/Souvikkundu369/google-review-ai)** | `Gemini` `GBP API` |
| 📞 | **[AI Call Analysis CRM](https://github.com/Souvikkundu369/call-analysis-crm)** | `Gemini` `Apps Script` |
| 📅 | **[Monthly YoY Performance Reports](https://github.com/Souvikkundu369/monthly-yoy-reports)** — recurring BI pipeline, frozen monthly reports vs prior year | `Node.js` `Multi-POS` |
| 🏦 | **[Manual Payments Ledger](https://github.com/Souvikkundu369/manual-payments-ledger)** — bank statement ingestion + 3-stage reconciliation engine on Cloudflare Workers | `Cloudflare Workers` `KV` |
| 📒 | **[Cashbook Dashboard](https://github.com/Souvikkundu369/cashbook-dashboard)** — per-store daily cash-closing + HO consolidated view via Apps Script | `Apps Script` `Sheets` |
| 🎂 | **[Birthday Automation](https://github.com/Souvikkundu369/birthday-automation)** — escalating WhatsApp birthday offers across 18,700+ child DOBs from 25+ outlets | `Node.js` `AiSensy` `Netlify` |
| 📦 | **[Walk-in Package Report](https://github.com/Souvikkundu369/walkin-package-report)** — monthly pipeline classifying walk-in revenue by tier (Unlimited / 120 / 90 / Extension) | `Node.js` `ExcelJS` |
| 🎙️ | **[AI Conduct Audit](https://github.com/Souvikkundu369/ai-conduct-audit)** — CCTV/security call monitoring, audio straight to Gemini with no transcription step | `Apps Script` `Gemini` |
| 🕒 | **[ESSL Attendance Dashboard](https://github.com/Souvikkundu369/essl-attendance-dashboard)** — live biometric punch data direct from SQL Server, public read-only API | `Node.js` `SQL Server` |

---

## Skills

![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![ETL](https://img.shields.io/badge/ETL%20%2F%20Data%20Pipeline-FF6C37?style=flat-square&logo=apacheairflow&logoColor=white)
![REST API](https://img.shields.io/badge/REST_APIs-FF6C37?style=flat-square&logo=postman&logoColor=white)
![Google Gemini](https://img.shields.io/badge/LLM%20%2F%20Gemini_API-412991?style=flat-square&logo=google&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=flat-square&logo=netlify&logoColor=white)
![Google Apps Script](https://img.shields.io/badge/Apps_Script-34A853?style=flat-square&logo=google&logoColor=white)
![BI Platform](https://img.shields.io/badge/BI%20Platform-185FA5?style=flat-square&logo=chartdotjs&logoColor=white)
![Real-Time Analytics](https://img.shields.io/badge/Real--Time%20Analytics-0F6E56?style=flat-square&logo=grafana&logoColor=white)
![Data Integration](https://img.shields.io/badge/Data%20Integration-854F0B?style=flat-square&logo=databricks&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

---

## Let's connect

- 💼 [linkedin.com/in/souvik-kundu-bi](https://linkedin.com/in/souvik-kundu-bi)
- 🌐 Live demos and code walkthroughs available on request

> *I don't wait for a data team. I am the data team.*
