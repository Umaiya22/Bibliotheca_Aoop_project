# Bibliotheca — An Interactive Digital Library

A full-stack library experience that blends book discovery and reading with interactive challenges, game mechanics, and an AI-powered librarian.

> Built as an academic team project. This repository contains the React client and Spring Boot service.

## What it does

- **Explore a digital library:** browse a collection of books and open individual book views.
- **AI librarian:** ask questions through a conversational librarian experience powered by the Google Gemini API.
- **Interactive challenges:** access themed mini-games and puzzle-style interactions connected to the library experience.
- **Progress and rewards:** game-economy context, daily rewards, and activity-related UI components.
- **Account experience:** registration, login, profile, and library dashboard screens.
- **Full-stack architecture:** React client communicates with a Spring Boot REST API backed by H2.

## Technology

| Layer | Technologies |
|---|---|
| Frontend | React 19, Vite 7, React Router, JavaScript, CSS |
| Backend | Java 17, Spring Boot 3.5.9, Spring Web, Spring Data JPA |
| Database | H2 |
| AI integration | Google Gemini API |
| Build tools | npm, Maven |

## Repository structure

```text
.
├── client/                 # React + Vite application
│   ├── public/books/       # Book/PDF assets
│   └── src/
│       ├── components/     # Reusable UI and game components
│       ├── context/        # Shared application state
│       ├── hooks/          # Reusable hooks
│       ├── pages/          # Application screens
│       └── services/       # Client-side service modules
├── springboot/demo/        # Spring Boot backend
│   └── src/main/
│       ├── java/           # Controllers, services, models, repositories
│       └── resources/      # Application configuration
└── *.md                   # Project guides and implementation notes
```

## Run locally

### Requirements

- Node.js and npm
- Java 17
- Maven (or the included Maven wrapper)
- A Google Gemini API key for AI chat functionality

### 1. Start the backend

```bash
cd springboot/demo
```

Set the Gemini key as an environment variable before starting the application.

**Windows PowerShell**
```powershell
$env:GEMINI_API_KEY="your_api_key_here"
./mvnw.cmd spring-boot:run
```

**macOS / Linux**
```bash
export GEMINI_API_KEY="your_api_key_here"
./mvnw spring-boot:run
```

### 2. Start the frontend

In a second terminal:

```bash
cd client
npm install
npm run dev
```

Open the local URL printed by Vite (commonly `http://localhost:5173`).

### Useful client commands

```bash
npm run dev       # Start development server
npm run build     # Create production build
npm run lint      # Run ESLint
npm run preview   # Preview production build
```

## Configuration and security

- **Never commit API keys, passwords, database files, or local environment files.**
- Configure the Gemini key through the `GEMINI_API_KEY` environment variable.
- Keep real credentials out of screenshots, documentation, commit messages, and issue reports.
- If a credential has ever been committed, revoke/rotate it with its provider. Removing it from the latest file does not erase it from Git history.

## Notes

This is an evolving academic project. Setup details and individual feature guides are available in the Markdown documentation in the repository. Some features may require local configuration or external API access.

## Maintainers

Developed collaboratively as an academic project. See the repository's contributor history for individual contributions.
