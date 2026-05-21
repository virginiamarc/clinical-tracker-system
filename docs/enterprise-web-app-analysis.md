# Clinical Tracker System – Architecture Analysis

## 📌 Overview
This document analyzes the technology stack and architecture of a real-world enterprise application (**myClinicalExchange**) and outlines a modern approach to rebuilding a similar system using current best practices.

---

## 🧠 Key Findings
- Legacy web application architecture (AngularJS + ASP.NET)
- Hosted on Microsoft IIS
- Likely uses SQL Server as a relational database
- Follows a traditional 3-tier architecture

---

## ❌ Is This a MERN Application?

**No — this is not a MERN stack application.**

### Why:
- MERN = MongoDB + Express + React + Node.js
- Observed:
  - Microsoft IIS (not Node/Express)
  - AngularJS (not React)

---

## 🧱 Identified Tech Stack

### ✅ Frontend
- **AngularJS (1.x)**
  - Found in: `/WebAPI/AngularJS/Scripts/app.js`
  - Legacy JavaScript framework (pre-2017)

- **jQuery**
  - Confirmed via: `jquery.stickylabelheaders.js`
  - Used for DOM manipulation and UI interactions

- **FullCalendar**
  - Found in: `fullcalendar.min.js`
  - Used for appointment/calendar functionality

### 👉 Frontend Summary
A hybrid frontend:
- AngularJS → application logic
- jQuery → UI behavior and plugins

---

### ✅ Backend
- **ASP.NET (C#)**
- **Hosted on Microsoft IIS**

Evidence:
- Header: `Microsoft-IIS/10.0`
- API-style structure implied by `/WebAPI/`

### 👉 Backend Summary
- ASP.NET Web API likely used for RESTful services
- IIS handles HTTP requests and routing

---

### ✅ Database (Inferred)
- Likely **Microsoft SQL Server**

### Why:
- Common pairing with ASP.NET + IIS
- Suitable for structured enterprise data

---

## 🏗️ Architecture Overview

### Frontend
- AngularJS (application logic)
- jQuery (UI interactions)
- FullCalendar (scheduling)

### Backend
- ASP.NET Web API (C#)
- Hosted on IIS

### Database
- SQL Server (relational)

---

## 🧭 Architecture Type
- Traditional 3-tier architecture:
  1. Presentation layer (Frontend)
  2. Application layer (Backend/API)
  3. Data layer (Database)

- Not a modern SPA architecture (React/Vue)
- Not Node-based

---

## 🔥 Observations (Important Insights)

### ✅ Legacy Enterprise Stack
- AngularJS (deprecated)
- jQuery-heavy frontend
- IIS + ASP.NET backend

### ✅ Likely System Age
- Built ~2013–2018
- Maintained rather than rebuilt

### ✅ Common Use Cases
- Healthcare systems
- Educational platforms
- Enterprise portals

---

## 🧪 How to Further Verify the Stack

Using browser DevTools (Network tab):

### Look for:
- `/api/`, `/WebAPI/`, `/services/`

### Response types:
- JSON → confirms REST API
- `.asmx` → legacy services
- `.svc` → WCF services

---

## ⚙️ How the System Works (Request Flow)

1. User visits the site
2. Request hits IIS (web server)
3. IIS forwards request to ASP.NET
4. ASP.NET processes logic
5. API queries SQL Server
6. Response sent back to browser

---

## ☁️ Hosting Model

### Option A: On-Premise
- Windows Server
- IIS installed
- SQL Server installed

### Option B: Cloud (more likely today)
- Azure Virtual Machine
- Azure App Service (IIS managed)

---

## 💰 Cost Considerations

### Hosting (IIS / Azure)
- Small: $15–$50/month
- Medium: $50–$200/month
- Enterprise: $300–$1000+/month

### Database (SQL Server)
- Small: $5–$30/month
- Medium: $50–$200/month
- Enterprise: $500+/month+

### Development
- Self-built: low cost (time investment)
- Outsourced: $10k–$100k+

---

## ⚖️ Pros vs Cons

### ✅ Pros
- Stable and mature
- Strong security ecosystem
- Excellent for structured data
- Long-term enterprise support

### ❌ Cons
- Higher cost (licensing + hosting)
- Less flexible than modern stacks
- AngularJS is outdated

---

## 🆚 Modern Alternative Stack

If rebuilding today:

- **Frontend:** React
- **Backend:** ASP.NET Core or Node.js
- **Database:** PostgreSQL
- **Hosting:** Cloud (Azure, Vercel, Render)

### Estimated Cost:
- $0–$50/month (small-scale project)

---

## 🚀 Modern Rebuild Plan

### Tech Stack
- React (frontend)
- ASP.NET Core API (backend)
- SQL Server or PostgreSQL (database)
- Azure App Service (deployment)

---

## 🧱 Suggested Project: Clinical Tracker App

### Features
- User authentication (JWT)
- Student management (CRUD)
- Appointment scheduling
- Dashboard analytics

---

## 🧠 Key Takeaways

- This is a **traditional enterprise Microsoft stack**
- Understanding it builds strong **system architecture skills**
- Modern apps use more flexible and cost-efficient alternatives

---

## ✅ Final Conclusion

myClinicalExchange is built with:

- **Frontend:** AngularJS + jQuery  
- **Backend:** ASP.NET (C#) on IIS  
- **Database:** Likely SQL Server  

It represents a **legacy enterprise system architecture** still widely used in production environments today.
