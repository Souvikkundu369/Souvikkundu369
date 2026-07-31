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
<td align="center"><b>8+</b><br><sub>production systems</sub></td>
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

I built a REST API + dashboard that replaced a full day of monthly manual Excel work. **63,000+ voucher records, 25+ stores, per-store owner-active rule, 28 rate tiers, charm pricing** — all computed server-side. Month-end incentive calculation: **8 hours → one click**. Stack: `Node.js` `Supabase` `PostgreSQL` `Netlify Functions`.

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

- **Cashbook Intelligence** — daily cash-closing per store, HO consolidated dashboard
- **ICICI Bank API** *(in progress)* — auto bank reconciliation against cashbook entries
- **Store QR Payment Gateway** *(in progress)* — outlet-level UPI payment flows

---

### 📞 Call Analysis CRM

I built a zero-manual AI call analysis pipeline: `FolderSync` → `Google Drive` → `Google Apps Script` → `Gemini LLM`. **30,000+ recordings backfilled**. New calls appear scored in the dashboard **within 60 seconds** of hanging up. Gemini scores pitch quality, objection handling, close attempt, and brand knowledge (0–10) — flagged calls auto-surface for manager coaching. ~10 salespeople, 3 brands, zero extra app installs required.

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
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)

`JavaScript` · `Node.js` · `Python` · `PostgreSQL` · `Supabase` · `REST APIs` · `LLM / Gemini API` · `PetPooja POS API` · `Semnox / Parafait API` · `ESSL Biometric API` · `GratyHR Astra API` · `AiSensy WhatsApp API` · `ICICI Bank API` · `Brevo` · `Netlify Functions` · `GitHub Actions` · `Google Apps Script` · `Leaflet.js` · `Chart.js`

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
