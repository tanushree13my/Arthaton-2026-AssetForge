
# AssetForge 
### Build income from what you already have. Prepare for what comes next.

AssetForge is an AI-powered financial resilience and asset-building platform designed to help people discover additional income opportunities using their existing skills, free time, and unused assets.

It also helps users understand how long they can financially survive if their primary income suddenly stops.

Our mission is simple:

**Help people build income-producing assets BEFORE a financial crisis happens.**

---

##  About AssetForge

Financial security is not just about earning more money. It is about having multiple income sources, managing expenses, and building assets that generate additional income.

AssetForge combines two intelligent engines:

###  1. Asset Maker Engine
Discovers income-generating opportunities based on:
- Existing skills
- Available free time
- Available assets
- Location
- Investment budget
- Personal preferences

###  2. Survival Runway Engine
Measures how long a person can financially survive if their primary income stops.

It analyses:
- Available liquid savings
- Essential monthly expenses
- Mandatory EMI payments
- Additional income sources
- Financial obligations

---

##  Problem Statement

Millions of salaried employees, students, freelancers, and young professionals depend heavily on a single income source.

However:
- People do not know how long their savings would last without income.
- Existing skills and unused assets remain underutilised.
- Finding realistic second-income opportunities is difficult.
- People often start preparing for financial emergencies too late.

AssetForge aims to solve this problem by helping people turn their existing resources into income-producing opportunities while improving financial preparedness.

---

##  Key Features

### 1. Survival Runway Calculator
Calculate how long your available savings can support your essential financial obligations.

### 2. Income Dependency Analysis
Understand how dependent you are on your primary income source.

### 3. AI Opportunity Radar
Discover income opportunities based on skills, assets, available time, location, and preferences.

### 4. Skill-to-Income Mapper
Explore practical ways to monetise existing skills.

### 5. Idle Asset Finder
Identify opportunities to generate income from resources you already own.

### 6. Income Loss Simulator
Simulate hypothetical financial situations if your primary income stops.

### 7. Second Income Simulator
Understand how an additional income stream could improve financial resilience.

### 8. Asset Building Roadmap
Convert selected opportunities into actionable tasks and milestones.

### 9. Asset Liquidity Analysis
Understand how quickly different assets could potentially be converted into cash.

### 10. AI Financial Coach
Get contextual financial explanations and practical suggestions.

---

##  Technology Stack

### Frontend
- Next.js 14
- React 18
- TypeScript
- Tailwind CSS
- Recharts
- Lucide React
- Framer Motion

### Backend
- Python
- FastAPI
- SQLite
- Pydantic

### Additional Technologies
- REST API
- Supabase client integration
- OpenAI integration dependencies
- Local browser storage

---

##  Project Architecture

```text
AssetForge/
│
├── backend/
│   ├── app/
│   │   ├── api/
│   │   │   └── endpoints.py
│   │   ├── core/
│   │   │   ├── config.py
│   │   │   ├── currency.py
│   │   │   └── database.py
│   │   ├── data/
│   │   │   └── official_opportunities.json
│   │   ├── engines/
│   │   │   ├── matcher_engine.py
│   │   │   ├── runway_engine.py
│   │   │   └── simulator_engine.py
│   │   ├── schemas/
│   │   ├── services/
│   │   └── main.py
│   ├── data/
│   ├── tests/
│   ├── requirements.txt
│   └── .env.example
│
├── frontend/
│   ├── app/
│   │   ├── dashboard/
│   │   ├── financial-coach/
│   │   ├── financial-profile/
│   │   ├── onboarding/
│   │   ├── opportunities/
│   │   ├── settings/
│   │   ├── survival-runway/
│   │   ├── page.tsx
│   │   └── layout.tsx
│   ├── components/
│   ├── lib/
│   ├── types/
│   ├── package.json
│   └── .env.example
│
└── database/
    ├── migrations/
    ├── prisma/
    └── schema.sql
````

# ** HOW TO RUN ASSETFORGE LOCALLY**

Follow these instructions to run the complete application on your computer.

The frontend and backend must run simultaneously in two separate terminals.

## **1. Prerequisites**

Install the following software before starting:

| Software | Recommended Version   |
| -------- | --------------------- |
| Node.js  | 18.17 or later        |
| npm      | Included with Node.js |
| Python   | 3.10 or later         |
| pip      | Latest version        |
| Git      | Latest version        |
| VS Code  | Recommended           |

Check whether the software is installed:

```
node -v
npm -v
python --version
pip --version
git --version
```

## **2. Download the Project**

Clone the GitHub repository:

```
git clone https://github.com/YOUR-USERNAME/AssetForge.git
```

Navigate into the project:

```
cd AssetForge
```

If you downloaded the ZIP file instead, extract it and open the extracted project folder in VS Code.

Make sure you are inside the directory containing both `frontend` and `backend`.

## **3. Start the Backend (FastAPI)**

Open Terminal 1.

Navigate to the backend directory:

```
cd backend
```

### **Create a Python Virtual Environment**

```
python -m venv .venv
```

### **Activate the Virtual Environment**

**Windows (PowerShell):**

```
.venv\Scripts\Activate.ps1
```

**Windows (Command Prompt):**

```
.venv\Scripts\activate.bat
```

**macOS / Linux:**

```
source .venv/bin/activate
```

### **Install Backend Dependencies**

```
pip install -r requirements.txt
```

### **Configure Environment Variables**

Create a `.env` file inside the backend directory.

Copy the example configuration:

**macOS / Linux:**

```
cp .env.example .env
```

**Windows:**

```
copy .env.example .env
```

The environment file contains optional configuration for services such as OpenAI and Supabase.

For a local development setup, configure the frontend URL and allowed origins as needed.

Never commit API keys or private credentials to GitHub.

### **Run the Backend Server**

Execute:

```
uvicorn app.main:app --reload --host 127.0.0.1 --port 8000
```

The backend will start at:

[http://127.0.0.1:8000](http://127.0.0.1:8000?utm_source=chatgpt.com)

### **Verify Backend**

Open the following URL in your browser:

[http://127.0.0.1:8000/health](http://127.0.0.1:8000/health?utm_source=chatgpt.com)

Expected response:

```
{
  "status": "healthy",
  "service": "AssetForge Engine"
}
```

### **API Documentation**

FastAPI automatically generates interactive API documentation.

Open:

[http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs?utm_source=chatgpt.com)

You can explore and test the backend API endpoints directly from your browser.

## **4. Start the Frontend (Next.js)**

Keep the backend terminal running.

Open Terminal 2.

Navigate to the frontend directory:

```
cd frontend
```

### **Install Frontend Dependencies**

```
npm install
```

### **Configure Environment Variables**

Create the frontend environment file:

**macOS / Linux:**

```
cp .env.example .env.local
```

**Windows:**

```
copy .env.example .env.local
```

The example file contains:

```
NEXT_PUBLIC_API_URL=http://localhost:8000/api/v1

NEXT_PUBLIC_SUPABASE_URL=https://your-project.supabase.co

NEXT_PUBLIC_SUPABASE_ANON_KEY=your-anon-key
```

The local API URL is the important setting for connecting the frontend to FastAPI.

Supabase credentials are only needed if you configure a real Supabase project.

Do not expose private service-role keys in frontend environment variables.

### **Run the Frontend**

Execute:

```
npm run dev
```

The Next.js development server will start.

Open:

[http://localhost:3000](http://localhost:3000?utm_source=chatgpt.com)

## **5. Access the Complete Application**

Once both servers are running:

| Service              | URL                                                                                 |
| -------------------- | ----------------------------------------------------------------------------------- |
| AssetForge Frontend  | [http://localhost:3000](http://localhost:3000?utm_source=chatgpt.com)               |
| FastAPI Backend      | [http://localhost:8000](http://localhost:8000?utm_source=chatgpt.com)               |
| API Documentation    | [http://localhost:8000/docs](http://localhost:8000/docs?utm_source=chatgpt.com)     |
| Backend Health Check | [http://localhost:8000/health](http://localhost:8000/health?utm_source=chatgpt.com) |

**Important:** Keep both terminal windows running while using the application.

## **6. Database Information**

AssetForge uses SQLite for its local opportunity database.

The backend automatically:

- Creates the SQLite database when it starts.
- Creates the required database tables.
- Loads the bundled official opportunity catalog.
- Updates existing catalog records when the backend starts.

Database location:


backend/data/assetforge.db


No separate database server is required for local development.

## **7. Running Tests**

Navigate to the backend directory and activate your Python virtual environment.

Run:


pytest


This executes the available backend engine tests.

## **8. Troubleshooting**

### **Problem: Node command not found**

Install Node.js and restart your terminal.

### **Problem: Python command not found**

Check your Python installation.

On some Windows systems, use:


py --version


You can also replace `python` with `py` in the setup commands.

### **Problem: Backend connection failed**

Make sure the FastAPI server is running at:


http://localhost:8000


Also verify that the frontend `.env.local` contains:

```
NEXT_PUBLIC_API_URL=http://localhost:8000/api/v1
```

Restart the frontend after changing environment variables.

### **Problem: Port 3000 is already in use**

Stop the other application using port 3000 or use a different available port.

### **Problem: Port 8000 is already in use**

Stop the other backend process or choose another port and update the frontend API URL accordingly.

### **Problem: Python dependency installation failed**

Update pip:

```
python -m pip install --upgrade pip
```

Then install the dependencies again:

```
pip install -r requirements.txt
```

## **Core Financial Calculations**

### **Survival Runway**

```
Survival Runway =
Liquid Savings /
(Essential Monthly Expenses + Mandatory EMIs)
```

### **Income Dependency**

```
Income Dependency =
(Primary Income / Total Monthly Income) × 100
```

### **Monthly Net Cash Flow**

```
Net Cash Flow =
Total Monthly Income -
Total Monthly Expenses -
Mandatory EMIs
```

These calculations help users understand their current financial position and explore hypothetical improvements.

## ** Designed for Indian Users**

AssetForge uses Indian financial examples and INR currency formatting.

The platform focuses on opportunities and financial resources relevant to students, salaried employees, freelancers, gig workers, and small business owners in India.

## ** Privacy and Security**

- Financial profiles are stored locally in the browser.
- Opportunity data is stored in SQLite.
- The AI coach uses contextual rule-based responses.
- Supabase authentication and cloud syncing are not configured in the current application.
- Never commit secrets, API keys, or private credentials.

## ** Future Enhancements**

- Advanced AI-powered financial recommendations.
- More personalised opportunity matching.
- Regional opportunity discovery.
- Multi-language support.
- Advanced financial forecasting.
- Secure cloud profile synchronisation.
- Financial goal tracking.
- Notifications and progress reminders.

## ** Disclaimer**

AssetForge is an educational financial planning and income-opportunity discovery platform.

Financial projections and earning estimates are illustrative and do not guarantee future income or financial outcomes.

The platform does not execute financial transactions and does not replace professional financial advice.

## **Contributing**

Contributions and suggestions are welcome!

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Commit your changes.
5. Submit a pull request.

## **License**

Add an appropriate open-source license before permitting reuse or redistribution.

## ** Built With AssetForge**

Don't wait for your primary income to disappear before building your second income source.

Discover what you already have.\
Turn your skills into opportunities.\
Build financial resilience.

# **AssetForge**

### **Build income from what you already have. Prepare for what comes next.**

