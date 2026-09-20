# FitFlow Redesign

Redesigned fitness tracking application delivering AI-personalized workout plans, private social communities, and camera-based nutrition logging.

## Tech Stack
- **Frontend:** React Native (+ React Native Web), TensorFlow Lite
- **Backend:** NestJS (core API), FastAPI (AI microservice)
- **Database:** PostgreSQL, Redis, Firebase Firestore/RTDB
- **Auth:** Firebase Authentication
- **Storage:** Amazon S3

## Repository Structure
```
fitflow-redesign/
├── frontend/      # React Native mobile & web client
├── backend/       # NestJS core API services
├── ai-service/    # FastAPI AI/ML microservice
└── docs/          # tech stack summary, comparison matrix, architecture diagram, ADRs
```

## Getting Started
See the `/docs` folder for the full technology comparison matrix, weighted decision matrix, architecture diagram, and architecture decision records (ADRs) produced for Lab Exercise 05 (IT3060 – Human Computer Interaction).

## Documentation
- [Tech Stack Summary](docs/tech-stack-summary.md)
- [Comparison Matrix](docs/comparison-matrix.md)
- [Architecture Decision Record (ADR-001)](docs/adr-001.md)
- [Architecture Diagram](docs/architecture-diagram.png)
