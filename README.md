# 🚀 GigOrbit - Next-Gen Autonomous Service Marketplace

![Hackathon Ready](https://img.shields.io/badge/Status-Hackathon_Ready-success?style=for-the-badge)
![Powered By](https://img.shields.io/badge/Engine-Google_Vertex_AI-blue?style=for-the-badge)
![Tech Stack](https://img.shields.io/badge/Stack-Node.js_|_Socket.IO_|_Tailwind-black?style=for-the-badge)

**GigOrbit** is an AI-driven, two-sided gig economy platform designed to seamlessly connect customers with verified home service professionals (Plumbers, Electricians, AC Technicians, etc.) using the power of Generative AI and Real-Time Websockets.

![GigOrbit Banner](https://placehold.co/1200x400/1e3a8a/ffffff?text=GigOrbit+|+AI+Powered+Service+Marketplace)

## 🌟 The Problem We Solve
Finding reliable, verified, and transparently priced home service workers in the informal sector is a nightmare. Customers face price gouging, while skilled workers struggle to find consistent jobs. GigOrbit eliminates the friction of manual searching, bargaining, and trust issues by letting an AI Agent handle the entire orchestration—from initial matchmaking to final booking.

## ⚠️ The "Zero-Hardcoding" Hackathon Promise
Unlike standard prototypes, **GigOrbit is a fully dynamic, real-time engine.** Every worker proposed by the AI is fetched live from our backend database (`workers.json`). The entire booking flow, from client request to partner acceptance, operates in milliseconds via a custom Socket.IO implementation. What you see is a real, breathing software architecture.

## ✨ Hackathon-Winning Features
* 🤖 **Autonomous AI Matchmaking:** Powered by **Google Vertex AI**. Users chat naturally in English or Roman Urdu. The AI parses the intent, scans the database, calculates real-world distances using the Haversine formula, and proposes the absolute best worker for the job.
* ⚡ **Real-Time Orchestration (Socket.IO):** A fully functional two-sided marketplace. When a customer confirms a booking, it instantly pings the Partner Dashboard via websockets (Zero Latency) with full client details (Name, Phone, Location, Problem Intent).
* 🧠 **AI Confidence Scoring:** The AI evaluates distance, ratings, and problem match to dynamically generate and display a glowing Confidence Score (e.g., 96%) before the user books, ensuring maximum trust.
* 🛡️ **Smart Dual-Auth System:** A seamless entry gate that separates Customers and Partners, validating users against our mock file-based database for instant logins without redundant registrations.
* ⭐ **Dynamic Rating Engine:** A true closed-loop feedback system dynamically reading and displaying real reviews from the data source, steering clear of hardcoded UI elements.
* 📱 **Mobile-First PWA UI:** A hyper-premium Glass-morphism design, flawless dark/light mode integration, and interactive Lottie animations built entirely with Tailwind CSS.

## 🛠️ Tech Stack
* **Frontend:** Vanilla JavaScript (ES6), HTML5, Tailwind CSS. (SPA Architecture)
* **Backend:** Node.js, Express.js, Socket.IO.
* **Database:** JSON/FS File System (`bookings.json` & `workers.json` for Hackathon Demo).
* **AI Engine:** Google Vertex AI.

## 🚀 How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/rizuuuuu-bot/GigOrbit-Submission.git
   cd GigOrbit-Submission
   ```

2. **Install Dependencies:**
   ```bash
   npm install
   ```

3. **Configure Authentication:**
   GigOrbit uses Google Vertex AI. Place your `credentials.json` (Service Account Key) file in the root directory. 
   Rename the provided `.env.example` file to `.env` and add your Google Cloud Project ID:
   ```env
   GOOGLE_APPLICATION_CREDENTIALS="./credentials.json"
   PROJECT_ID="your-google-cloud-project-id"
   PORT=5000
   ```

4. **Start the Real-Time Server:**
   ```bash
   npm start
   ```

5. **Open the App:**
   Navigate to `http://localhost:5000` in your browser. For the best experience, open two separate windows (one as a Customer, one as a Partner) to experience the real-time Socket.IO synchronization.
