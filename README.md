# ProctorAI - Frontend

Modern, high-performance React + Vite frontend for **ProctorAI**, an AI-powered assessment, live proctoring, and evaluation platform.

## Features

- **Candidate Examination Engine**:
  - Token-validated exam access and verification flow.
  - Multi-stage onboarding: System diagnostics (camera, mic, network, fullscreen), instructions, identity verification, and exam consent.
  - Rich question renderers: Single/multiple-choice MCQs and multi-language coding questions with embedded code editor and test execution.
  - Live proctoring monitoring with automatic face tracking, tab switch detection, and anti-cheating alerts.
- **Recruiter & Admin Dashboard**:
  - Live candidate attempt monitoring with risk-tier sorting.
  - Assessment builder with dynamic rules, timing constraints, and negative marking configurations.
  - Question bank management with versioning and difficulty tagging.
  - Cohort analytics, percentile rankings, and CSV/PDF export.
- **Live Proctor Reviewer Portal**:
  - Multi-feed grid view of active candidates with real-time WebSocket anomaly event telemetry.
  - Incident flagging, manual warnings, and exam termination controls.

## Tech Stack

- **Framework**: React 18, Vite 5
- **Styling**: Tailwind CSS
- **Icons**: Lucide React
- **Routing**: Client-side hash routing with history synchronization
- **Communication**: REST API + WebSockets (`/api` and `/ws` reverse-proxied to backend)

## Getting Started

### 1. Install Dependencies
```bash
npm install
```

### 2. Configure Environment
Copy `.env.example` to `.env`:
```bash
cp .env.example .env
```

Ensure `VITE_API_BASE_URL` points to your running backend:
```env
VITE_API_BASE_URL=http://localhost:8000
```

### 3. Run Development Server
```bash
npm run dev
```
The application will launch on `http://localhost:3000`.

### 4. Build for Production
```bash
npm run build
```
Build outputs are generated in the `dist/` directory.

## License
MIT
