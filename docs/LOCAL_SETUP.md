# Local setup and security notes

## Prerequisites

- Node.js and npm
- Java 17
- Maven (or the included Maven wrapper)
- A Google Gemini API key for the AI librarian

## Backend

From `springboot/demo`, set the key in your shell before running Spring Boot.

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

The application reads the key through the `gemini.api.key` property, which resolves from `GEMINI_API_KEY`.

## Frontend

From the repository root:

```bash
cd client
npm install
npm run dev
```

For a production build, run `npm run build`.

## Security

- Do not commit real API keys, `.env` files, local databases, logs, or build output.
- The `.gitignore` file excludes common local secrets, H2 database files, and generated build artifacts.
- If a key was committed previously, revoke it with Google AI Studio / Google Cloud and create a replacement. Changing the latest configuration does not remove a credential from Git history.
