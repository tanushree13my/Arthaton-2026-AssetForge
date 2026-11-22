AI-powered financial resilience platform that helps users discover second-income opportunities, monetise existing skills and assets, and calculate their financial survival runway.
AssetForge 
### Build income from what you already have. Prepare for what comes next.

**AssetForge** is an AI-powered financial resilience and asset-building platform designed to help people discover additional income opportunities using their existing skills, free time, and unused assets — while understanding how financially prepared they are for an unexpected loss of income.

Instead of waiting for a financial emergency, AssetForge helps users build a second income engine before they need one.


 Overview

Financial security is not just about earning more money. It is also about having multiple income sources, managing expenses, and building assets that can generate additional income.

AssetForge addresses this challenge through two intelligent engines:

| Engine | Purpose |
|---|---|
|  Asset Maker Engine | Discovers personalised opportunities to generate additional income. |
|  Survival Runway Engine | Calculates how long a person can financially survive if their primary income stops. |

The platform combines financial calculations, personalised recommendations, interactive simulations, and AI-powered guidance to help users improve their financial resilience.

---

##  Problem Statement

Millions of students, salaried employees, freelancers, and young professionals depend heavily on a single income source.

However:

- Most people do not know how long their savings would last without income.
- Existing skills and unused assets often remain unmonetised.
- People struggle to identify realistic second-income opportunities.
- Financial planning tools rarely connect emergency preparedness with income generation.
- Many people start preparing for financial instability only after a crisis occurs.

**AssetForge aims to change this by helping people turn existing resources into income-producing opportunities.**

---

## Key Features

### 1. Survival Runway Calculator
Calculate how many months your available savings can support your essential financial obligations.

Features:
- Available liquid savings.
- Essential monthly expenses.
- Mandatory EMI payments.
- Estimated survival duration.
- Financial safety indicators.
- Expense improvement suggestions.

**Formula:**


Survival Runway =
Usable Liquid Savings /
(Essential Expenses + Mandatory EMIs)


### 2. Income Dependency Score

Understand how dependent you are on your primary income source.

Features:
- Primary income analysis.
- Secondary income tracking.
- Income distribution visualisation.
- Dependency percentage.
- Financial dependency risk category.

**Formula:**


Income Dependency =
(Primary Income / Total Monthly Income) × 100


### 3.  AI Opportunity Radar

Discover income opportunities based on your:

- Existing skills.
- Available free time.
- Location.
- Available assets.
- Investment budget.
- Risk tolerance.
- Income preferences.

Example opportunities:
- Python tutoring.
- Freelance development.
- Graphic design.
- Content creation.
- Photography services.
- Digital products.
- Online workshops.

Each opportunity includes estimated earnings, investment requirements, difficulty, time commitment, and a recommended first step.

*All earning ranges are illustrative estimates, not guaranteed income.*

### 4.  Skill-to-Income Mapper

Convert existing skills into practical income opportunities.

Example:

| Skill | Potential Income Opportunities |
|---|---|
| Python | Tutoring, automation, web development |
| Graphic Design | Freelancing, social media creatives |
| Writing | Content writing, blogging |
| Teaching | Online tutoring, workshops |
| Photography | Photography assignments, content services |

### 5. Idle Asset Finder

Discover income opportunities from resources you already own.

Examples:

- Laptop → Freelancing and online tutoring.
- Camera → Photography and content creation.
- Bike → Local service opportunities.
- Spare room → Potential rental opportunities, subject to local regulations.

### 6. Income Loss Simulator

Explore hypothetical financial situations if your primary income suddenly stops.

Features:
- Adjustable savings.
- Monthly expenses.
- EMI obligations.
- Secondary income.
- Month-by-month financial projections.
- Estimated savings depletion.
- Potential borrowing requirements.

### 7.  Second Income Simulator

Understand how additional income could improve your financial resilience.

Compare your financial position before and after introducing another income stream.

### 8.  Asset Building Roadmap

Turn an income opportunity into an actionable plan.

Features:
- Weekly milestones.
- Individual tasks.
- Progress tracking.
- Task completion.
- Due dates.
- Editable action plans.

### 9.  Asset Liquidity Map

Understand how quickly your assets can potentially be converted into cash.

Liquidity categories:

- Immediate liquidity.
- Near-cash.
- Delayed liquidity.
- Illiquid assets.

Restricted investments and property are not automatically treated as emergency cash.

### 10.  AI Financial Coach

An interactive assistant that helps users:

- Understand their financial scores.
- Explore additional income opportunities.
- Improve financial preparedness.
- Create action plans.
- Understand financial concepts.
- Compare hypothetical scenarios.

The application supports a rule-based fallback when an external AI API is unavailable.

---

##  Technology Stack

### Frontend
- React.js
- Vite
- Tailwind CSS
- React Router
- Recharts
- Lucide React

### Backend
- Python
- FastAPI
- SQLAlchemy
- SQLite

### AI Integration
- OpenAI API / Google Gemini API
- Rule-based fallback engine

### Additional Technologies
- REST API
- JWT authentication
- Password hashing
- Environment variables
- Responsive UI design

---

##  Application Architecture

```text
                  ASSETFORGE
                       |
          +------------+------------+
          |                         |
       FRONTEND                  BACKEND
          |                         |
     React + Vite              FastAPI
          |                         |
     Tailwind CSS              SQLAlchemy
          |                         |
       Recharts                 SQLite
          |                         |
          +------------+------------+
                       |
                CORE ENGINES
                       |
          +------------+------------+
          |                         |
    ASSET MAKER ENGINE       SURVIVAL RUNWAY
          |                         |
    Opportunity Matching     Financial Analysis
    Skill Mapping            Dependency Scoring
    Idle Asset Finder        Income Simulations
    Roadmap Generation       Liquidity Analysis
          |                         |
          +------------+------------+
                       |
                  AI COACH
                       |
             OpenAI / Gemini API
                Rule-based Fallback
```

---

##  Project Structure

```text
AssetForge/
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── layouts/
│   │   ├── context/
│   │   ├── hooks
