📌 Project Description

GigShield is an AI-powered risk assessment and autonomous micro-insurance platform designed specifically for the growing gig economy workforce, including delivery partners from platforms like Swiggy, Zomato, Amazon, and Zepto. These workers often face unpredictable income loss due to environmental and urban disruptions such as heavy rainfall, extreme heat, high pollution levels, traffic congestion, or government-imposed restrictions. Traditional insurance systems are not optimized for such dynamic and short-term risks, making financial protection inaccessible or inefficient for gig workers.

GigShield addresses this gap by providing real-time, data-driven insurance coverage that adapts to a worker’s location, activity level, and risk exposure. The platform continuously analyzes multiple factors such as weather conditions, air quality index (AQI), traffic patterns, and historical disruption trends to generate a city-specific risk score (0–100%). This score helps determine the likelihood of disruptions that could affect a worker’s earnings.

A key innovation of GigShield is its autonomous insurance system, which eliminates the need for manual claim filing. When predefined disruption conditions are met (for example, extreme rainfall or high temperature thresholds), the system automatically triggers payouts to eligible workers. This ensures instant financial support without delays or paperwork. Additionally, the platform includes pro-rata refund mechanisms, allowing users to receive fair reimbursements if they become inactive or discontinue their work.

The platform also incorporates a smart fraud detection system that verifies claims using GPS activity logs, claim frequency patterns, and policy status checks. Suspicious claims are flagged for further review, ensuring system integrity and preventing misuse.

GigShield features multi-role dashboards tailored for both workers and administrators. Workers can monitor their risk levels, insurance coverage, and claim status, while administrators can oversee platform analytics, manage users, and handle flagged claims efficiently.

The AI component of GigShield is implemented using a deterministic and rule-based approach built with Python and FastAPI. Instead of relying on black-box models, it uses weighted scoring algorithms, threshold-based predictions, and heuristic logic, ensuring transparency, explainability, and auditability—critical requirements for financial and insurance systems.

Additionally, the platform includes a rule-based AI chatbot that assists users by answering queries related to policies, claims, refunds, and system functionality in real time.

Overall, GigShield provides a scalable, transparent, and intelligent insurance solution that empowers gig workers with financial security while leveraging AI to automate decision-making and risk management.


✨ Features

🔹 AI-Powered Risk Assessment

Generates real-time risk scores (0–100%) for each worker based on their city.
Uses a multi-factor weighted model:

🌦️ Weather conditions
🌫️ Air Quality Index (AQI)
🚦 Traffic patterns
📊 Historical disruption data

Helps workers understand daily earning risks before going online.

🔹 Predictive Disruption Alerts

Predicts upcoming disruptions like heavy rain, extreme heat, or pollution spikes.
Uses threshold-based probability models.
Enables workers to:
Plan work schedules
Purchase insurance in advance

🔹 Autonomous Insurance System

Offers flexible micro-insurance plans (weekly/monthly).
Fully automated:

✅ Detects disruption events
✅ Triggers claims automatically
❌ No manual claim filing required
Ensures instant and hassle-free payouts.

🔹 Automatic Payout Mechanism

Payouts are triggered when conditions exceed thresholds:
Example: Heavy rainfall (>80mm), extreme heat (>42°C)
Payments processed for active policyholders only.
Provides fast financial support during crises.

🔹 Pro-Rata Refund System

Calculates refunds for:
Inactive workers
Early policy termination
Ensures fair usage-based billing.

🔹 Smart Fraud Detection

Prevents misuse using:
📍 GPS activity validation
📉 Claim frequency tracking
🔁 Pattern recognition
Flags suspicious claims as “Under Review” for admin verification.

🔹 Multi-Role Dashboard System
👤 Worker Dashboard

View risk score & predictions
Manage insurance plans
Track claims and payouts
Monitor activity & earnings

🛠️ Admin Dashboard

Monitor platform-wide analytics
Manage users, policies, and claims
Detect and review fraudulent activities
Trigger manual disruption events

🔹 GigShield AI Chatbot

Provides real-time assistance to workers
Answers queries about:
Insurance plans
Claims & payouts
Refund policies
Worker classification
Built using rule-based NLP logic

🔹 Scalable AI Architecture

AI services built with FastAPI
Uses:
Weighted scoring algorithms
Threshold-based prediction models
Heuristic fraud detection
Ensures high transparency and reliability

🔹 Modular API System

Clean API structure for easy integration:
/risk-score → Risk calculation
/predict-disruption → Event prediction
/chat → AI chatbot

Backend handles:
Users
Policies
Claims
Fraud flags

INSTALLATION STEPS

To set up and run the GigShield project, you need to initialize three separate services: the Frontend, the Backend, and the AI Service.

Follow these steps for each service:

1. Prerequisites
Ensure you have the following installed on your system:

Node.js (v18 or higher)
npm or yarn
Python (v3.10 or higher)
MongoDB (Local instance or MongoDB Atlas)
2. Backend Setup (Node.js/Express)
The backend manages the database and core business logic.

Navigate to the backend directory:
powershell
cd backend
Install dependencies:
powershell
npm install
Configure environment variables:
Create a .env file in the backend/ folder.
Add your MongoDB connection string and a JWT secret:
env
MONGO_URI=mongodb://localhost:27017/gigshield
JWT_SECRET=your_secret_key_here
PORT=5000
Start the backend server:
powershell
npm start
The backend will now be running at http://localhost:5000.
3. AI Service Setup (Python/FastAPI)
The AI service handles risk scores, disruption predictions, and the chatbot.

Navigate to the AI service directory:
powershell
cd ai-service
Install required Python libraries:
powershell
pip install fastapi uvicorn pydantic
Start the AI service:
powershell
python -m uvicorn main:app --reload --port 8000
The AI service will now be running at http://localhost:8000.
4. Frontend Setup (React/Vite)
The frontend provides the user interface for workers and admins.

Navigate to the frontend directory:
powershell
cd frontend
Install dependencies:
powershell
npm install
Start the development server:
powershell
npm run dev
The frontend will usually be available at http://localhost:5173.
5. Summary of Running Ports
Once everything is set up, verify that all three services are running:

Frontend: http://localhost:5173 (UI)
Backend: http://localhost:5000 (Database & Auth)
AI Service: http://localhost:8000 (Risk Scoring & Chat)
TIP

Admin Access: To access the Admin Panel, ensure you have at least one worker in your MongoDB collection with is_admin: true. You can then log in through the /admin/login page.

▶️ Usage Instructions

🔹 1. Start the Application

Run all three services:
Frontend (React)
Backend (Node.js/Express)
AI Service (FastAPI)
Open the application in your browser:
http://localhost:5173

🔹 2. User Registration & Login

Create a new account or log in with existing credentials.
Secure authentication is handled using JWT.
Users are classified as gig workers within the platform.

🔹 3. Access the Worker Dashboard

After logging in, users can:
View their real-time risk score (0–100%)
Check predicted disruptions (e.g., rain, heat, pollution)
Monitor activity and performance metrics

🔹 4. Purchase Insurance Plan

Choose a suitable micro-insurance plan (weekly or monthly).
Complete payment (mock/UPI integration).
Once purchased, the policy becomes active immediately.

🔹 5. Monitor Risk & Work Activity

The system continuously evaluates:
Weather conditions
Air quality (AQI)
Traffic patterns
Risk scores update dynamically to reflect current conditions.

🔹 6. Automatic Claim & Payout System

When a disruption occurs (e.g., heavy rainfall, extreme heat):
The system detects the event automatically
Verifies eligible users
Triggers instant payouts
No manual claim submission is required.

🔹 7. Refund Processing

If a user:
Becomes inactive OR
Cancels the insurance early
The system calculates a pro-rata refund based on unused days.

🔹 8. Use of AI Chatbot

Users can interact with the chatbot to:
Understand policies
Check claim status
Get help with refunds or risk scores
The chatbot provides instant, rule-based responses.

🔹 9. Admin Panel Usage

Admins can:
Monitor platform-wide analytics
Manage users, policies, and claims
Review flagged fraud cases
Trigger or manage disruption events manually

🔹 10. API Interaction (Optional)

Developers can use:
POST /risk-score → Get risk score
POST /predict-disruption → Predict disruptions
POST /chat → Chatbot interaction
/api → Backend operations (users, claims, policies)

🔹 11. End-to-End Workflow

User logs in
Checks risk score
Purchases insurance
Continues work
Disruption occurs
System auto-detects event
Payout is processed instantly


