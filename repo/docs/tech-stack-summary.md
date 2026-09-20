# FitFlow Redesign — Technology Stack Summary

## Frontend
**React Native** (+ React Native Web for browser support), with **TensorFlow Lite** for on-device AI inference.

Chosen because it shares a JavaScript/TypeScript layer with the Node.js backend, has the fastest hiring/onboarding path for a mid-sized team, and builds directly on FitFlow's existing Firebase and TensorFlow Lite investments.

## Backend
- **NestJS** (Node.js) — core API for user profiles, workouts, and social features.
- **FastAPI** (Python) — isolated AI microservice for workout personalization and computer-vision nutrition recognition.

## Database
- **PostgreSQL** — system of record for users, workouts, subscriptions, and nutrition logs (strong ACID guarantees for sensitive health data).
- **Firebase Firestore / Realtime Database** — real-time social feed, live notifications, and presence.
- **Redis** — caching layer for frequently accessed data (e.g., today's AI-recommended workout).

## Authentication
**Firebase Authentication** — consolidates identity with FitFlow's existing Firebase real-time services; supports social login, MFA, and GDPR-aligned controls.

## Storage
**Amazon S3** (or Firebase Storage) — meal photos, progress images, and trained model artifacts.

## Why This Stack
This combination directly supports FitFlow's core requirements from the case study:
- **Security** for sensitive health/nutrition data (PostgreSQL + access controls)
- **Real-time** social features (Firebase)
- **Fast performance** under load (Redis caching)
- **Cost-effective maintainability** for a mid-sized engineering team (shared TypeScript backend, managed services wherever possible)

See `comparison-matrix.md` for the full weighted evaluation and `adr-001.md` for the formal architecture decision record.
