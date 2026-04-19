# CarGuru - AI Car Research Assistant

CarGuru is a full-stack application designed to help users find their perfect car using AI-powered voice and text interaction.

## 🏗 Project Architecture
- **Frontend**: Next.js (React), Framer Motion, ElevenLabs Conversational AI.
- **Backend**: Node.js, Express, TypeScript.
- **Database**: PostgreSQL.
- **Orchestration**: Docker Compose.

## 🚀 Quick Start (Docker)

The easiest way to run the entire stack is using Docker Compose:

1.  **Clone the repository**.
2.  **Configure environment variables**:
    -   Create `frontend/.env` and `backend/.env` (see respective READMEs).
3.  **Run everything**:
    ```bash
    docker-compose up -d
    ```
4.  **Access the apps**:
    -   Frontend: [http://localhost:3000](http://localhost:3000)
    -   Backend Health: [http://localhost:3003/health](http://localhost:3003/health)

## 📂 Directories
- [frontend](./frontend): Next.js application.
- [backend](./backend): Express API and database scripts.

## 🛠 Features
- **Multilingual Voice Search**: Speak in English, Hindi, or Tamil.
- **AI Recommendations**: Get a curated shortlist based on your specific needs.
- **Premium Design**: Modern, responsive UI with sleek animations.

---

## 🧠 Project Reflection

### 1. What was built and why?
I built **CarGuru**, an AI-powered car research assistant, to simplify the complex process of buying a car. By allowing users to speak naturally in their own language, we remove the barrier of technical jargon.
- **Deliberate Cuts**: Due to time constraints and the complexity of real-time WebRTC event mapping, I decided to cut **real-time visual car suggestions** during the AI conversation. Users currently see their results after the consultation.

### 2. Tech Stack Rationale
- **Next.js**: Picked for its superior SEO capabilities, fast page loads, and modern developer experience.
- **Node.js & TypeScript**: Provides a robust, type-safe foundation for the recommendation engine.
- **Docker**: Used to ensure a consistent environment across development and production, making the entire stack (Database, Backend, Frontend) deployable with one command.

### 3. AI as a Co-Pilot
- **Delegated to AI**: Component scaffolding, complex CSS transitions, database seeding logic, and rapid implementation of new features like the Telegram integration.
- **Where it helped most**: The AI was invaluable for rapid implementation—taking an idea and turning it into working code in minutes rather than hours.
- **Where it got in the way**: Occasionally, it struggled with specific hardware-level WebRTC version conflicts in the ElevenLabs SDK, which required manual intervention to resolve.

### 4. The "Next 4 Hours" Roadmap
If I had another 4 hours, I would:
1. **Dynamic Visuals**: Implement real-time UI updates so that car cards appear on-screen as the AI mentions them.
2. **Advanced Animations**: Add more fluid, physics-based transitions for the car discovery flow.
3. **Comparison Tool**: Allow users to compare their top 3 recommended cars side-by-side with detailed specs.
