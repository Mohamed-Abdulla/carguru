# CarGuru - AI Car Research Assistant

CarGuru is a full-stack application designed to help users find their perfect car using AI-powered voice and text interaction.

## 🏗 Project Architecture

- **Frontend**: Next.js (React), Framer Motion, ElevenLabs Conversational AI.
- **Backend**: Node.js, Express, TypeScript.
- **Database**: PostgreSQL (managed via Docker).
- **Orchestration**: Docker Compose.

## 🚀 Quick Start (Docker)

The easiest way to run the entire stack is using Docker Compose from this root directory:

1.  **Clone the repository**.
2.  **Configure environment variables**:
    - Copy `.env.example` to `.env` in the root directory.
    - (Optional) Configure sub-project `.env` files in `./carguru-frontend` and `./carguru-backend` if running locally without Docker.
3.  **Run everything**:
    ```bash
    docker compose up -d --build
    ```
4.  **Access the apps**:
    - Frontend: [http://localhost:3000](http://localhost:3000)
    - Backend Health: [http://localhost:3003/health](http://localhost:3003/health)

## 📂 Directories

- [carguru-frontend](./carguru-frontend): Next.js application (Standalone mode for production).
- [carguru-backend](./carguru-backend): Express API and database management.

## 🛠 Tech Notes (Docker Networking)

For maximum compatibility across Docker and local development, the frontend uses **client-side data fetching** for main sections (Stats, Popular, Shortlist). This ensures requests to `http://localhost:3003` always resolve correctly from the user's browser, bypassing complex container-to-container networking hurdles.

---

## 🚀 Key Features

- **Voice Assistant**: Multilingual support (English, Hindi, Tamil) via ElevenLabs.
- **Smart Shortlist**: Personalized car recommendations based on budget, use case, and priorities.
- **Premium UX**: Smooth Framer Motion animations and a glass-morphism design language.

## 🧠 Project Reflection

### 1. What was built and why?

I built **CarGuru** to bridge the gap between complex car technical specs and everyday buyers. By combining a modern, premium UI with conversational AI, we make car research feel personal and intuitive.

### 2. Tech Stack Rationale

- **Next.js**: Hybrid rendering capabilities allow for a fast, SEO-friendly experience.
- **Node.js & TypeScript**: Unified language across the stack ensures type safety and rapid backend iteration.
- **Docker**: Containerization ensures that PostgreSQL and the Node services run identically on every machine.

### 3. AI as a Co-Pilot

AI was heavily utilized for structural scaffolding, implementing complex physics-based UI transitions, and generating the recommendation logic. It allowed for high-velocity development without sacrificing code quality or aesthetic polish.

### 4. Roadmap

1. **Comparison Engine**: Real-time side-by-side comparison of shortlisted car models.
2. **Dynamic Visuals**: Visual feedback that updates as the Voice AI suggests specific cars.
3. **Advanced Filtering**: More granular search options including safety data and resale value trends.
