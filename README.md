# baby-butler

# NurtureButler

## Overview

**NurtureButler** is a Flutter-powered digital assistant designed to support expectant and new parents throughout pregnancy and early baby development. Built using **Flutter** for the frontend and **Serverpod 3** as a Dart-based backend, NurtureButler acts as a proactive "butler" that tracks progress, sends timely reminders, and surfaces helpful, educational insights at every stage.

The app focuses on automation and assistance rather than passive tracking, demonstrating how Flutter and Serverpod can work together to deliver a practical, real-world digital assistant.

> ⚠️ **Disclaimer:** NurtureButler provides general educational information and reminders only. It does not provide medical advice or replace professional healthcare guidance.

---

## Features

### Pregnancy Mode

* Automatic pregnancy week calculation based on due date
* Weekly pregnancy summaries
* Baby development highlights (high-level, non-diagnostic)
* Preparation tips and reminders
* Proactive weekly notifications powered by backend scheduling

### Baby Mode

* Seamless transition after birth
* Baby milestone tracking
* Vaccination schedule reminders
* Educational explanations for each vaccination
* Growth and development checkpoints

### Butler Experience

* Proactive reminders instead of manual checking
* Clear timelines and "what’s next" insights
* Simple, calm UI focused on reducing cognitive load

---

## Tech Stack

### Frontend

* **Flutter**
* Material 3 UI
* Clean, responsive layouts
* API-driven state management

### Backend

* **Serverpod 3**
* Dart-based API endpoints
* Scheduled jobs for reminders and summaries
* PostgreSQL database (managed via Serverpod)
* Backend-driven business logic (date calculations, milestones)

---

## Architecture Overview

```
Flutter App
   │
   │ REST / Serverpod APIs
   ▼
Serverpod Backend
   ├── Authentication
   ├── Pregnancy & Baby Logic
   ├── Scheduled Jobs (Reminders)
   └── PostgreSQL Database
```

Serverpod is responsible for:

* Pregnancy week calculations
* Baby milestone logic
* Vaccination schedule timing
* Automated reminder triggers
* Data persistence

Flutter is responsible for:

* User interface
* Butler interaction screens
* Displaying summaries and insights

---

## Project Structure (High-Level)

```
nurturebutler/
├── flutter_app/
│   ├── lib/
│   └── pubspec.yaml
├── serverpod/
│   ├── lib/
│   ├── generated/
│   └── config/
└── README.md
```

---

## Getting Started

### Prerequisites

* Flutter SDK
* Dart SDK
* Docker (recommended for Serverpod)
* PostgreSQL

### Setup

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd nurturebutler
   ```

2. Set up Serverpod:

   ```bash
   cd serverpod
   serverpod generate
   docker compose up
   ```

3. Run the Flutter app:

   ```bash
   cd flutter_app
   flutter pub get
   flutter run
   ```

---

## Demo

A short demo video (≤ 3 minutes) demonstrates:

* Pregnancy tracking and weekly summaries
* Butler-style reminders
* Transition to Baby Mode
* Vaccination reminders and milestone tracking

---

## Inspiration

Pregnancy and early parenthood involve many timelines, milestones, and responsibilities that can feel overwhelming. NurtureButler was created to reduce that cognitive load by acting as a reliable digital assistant—one that proactively reminds, informs, and supports parents without requiring constant manual input.

---

## Hackathon Context

This project was built for the **Serverpod 3 Flutter Butler Hackathon**, with a focus on:

* Demonstrating Flutter + Serverpod integration
* Backend-driven automation
* Practical, real-world use cases
* Clean and understandable architecture

---

## Future Improvements

* Optional AI-powered question answering
* Cloud sync across devices
* Partner or caregiver access
* Localization and language support

---

## License

This project is provided for hackathon and educational purposes.
