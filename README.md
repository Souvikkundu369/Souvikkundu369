# Souvik Kundu — BI & Automation Engineer

> **Self-taught. Solo. 22 outlets. Everything — from POS data to dashboard to AI — built by one person.**

I design and run the complete data + AI stack for a multi-outlet family-entertainment chain across India. No data team, no enterprise tools budget. Just real business problems that needed solving, and whatever it took to solve them.

---

## The scale

<table>
<tr>
<td align="center"><b>22</b><br><sub>outlets across India</sub></td>
<td align="center"><b>3</b><br><sub>POS systems unified</sub></td>
<td align="center"><b>25+</b><br><sub>analytics modules</sub></td>
<td align="center"><b>8+</b><br><sub>production systems</sub></td>
<td align="center"><b>1</b><br><sub>person</sub></td>
</tr>
</table>

---

## What I've built

### 📊 Real-Time BI Platform — 25+ analytics modules

A single-page analytics dashboard covering an entire entertainment chain. Three POS systems, two brands, 22 outlets — one source of truth.

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
- Live Geo Map — all 22 outlets on Leaflet.js, click-through to store detail
- Multi-company — Jus Jumpin (FEC) + The Knockout (sports bar) in one dashboard
- Multi-POS — Semnox/Parafait (arcade/wallet) + PetPooja (F&B) + internal activity API
- AI Assistant — ask questions in plain English via Gemini LLM (voice + text, live data context)
- Global Export — PDF and Excel from every single tab
- Daily Digest — automated 9am IST email to management via Brevo

---

### 🎤 ARIA — AI Interview System *(live in production)*

Automated candidate interviews: candidates answer in their own time, Gemini LLM scores structured rubrics, hiring managers read a summary instead of 40 recorded calls. Deployed at `jusjumpin-hr-interviews.netlify.app`.

---

### 🧮 Incentive Automation API

Web API + dashboard that replaced a full day of monthly Excel work for salesman voucher-incentive calculations across 22 stores. 63,000+ voucher records, per-store owner-active logic, charm pricing baked in. A day's work → one click.

---

### 💬 WhatsApp Birthday Marketing Engine

Escalating DOB-driven birthday campaigns (7 / 5 / 2 / 0 days out) via AiSensy WhatsApp API. Pulls live customer DOBs, generates personalised offer codes, tracks redemption. 22,000+ customer base.

---

### 👤 HR & Attendance Systems

- **ESSL + GratyHR Astra integration** — biometric punch data auto-synced into GratyHR Astra HR software via API
- **ESSL Biometric API** — auto employee provisioning and automated monthly attendance reports
- **Kolkata HO Salary Attendance** — biometric export → formula-driven payroll status (P / H / A / W/O) for 87 employees

---

### 🏦 Cashbook & Payments

- **Cashbook Intelligence** — daily cash-closing per store, HO consolidated dashboard
- **ICICI Bank API** *(in progress)* — auto bank reconciliation against cashbook entries
- **Store QR Payment Gateway** *(in progress)* — outlet-level UPI payment flows

---

### 📞 Call Analysis CRM

AI-powered sales call pipeline: MacroDroid call-end popup → Google Sheets webhook → automatic recording attachment per salesperson → AI summary. ~10 salespeople, ~1-minute sync.

---

### ⭐ Google Review AI

Automated Google My Business reply generation with Gemini + negative-review escalation to management *(pending GBP API access)*.

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

---

## GitHub Stats

![Souvik's GitHub stats](https://github-readme-stats.vercel.app/api?username=Souvikkundu369&show_icons=true&theme=default&hide_border=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Souvikkundu369&layout=compact&hide_border=true)

---

## Let's connect

- 💼 [linkedin.com/in/souvik-kundu-bi](https://linkedin.com/in/souvik-kundu-bi)
- 🌐 Live demos and code walkthroughs available on request

> *I don't wait for a data team. I am the data team.*
