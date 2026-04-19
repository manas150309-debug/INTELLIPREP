# IntelliPrep (API + Web Technology Project)

IntelliPrep is a simple web technology quiz app that demonstrates how to build and consume an API using **only core Node.js** on the backend and vanilla HTML/CSS/JavaScript on the frontend.

## Why this version

The previous implementation required `express`, but dependency installation can fail in restricted environments. This revision is zero-dependency so it runs with just Node installed.

## Features

- Zero-dependency Node HTTP API server
- Topic list endpoint
- Question retrieval endpoint by topic
- Answer evaluation endpoint with per-question review
- Static frontend powered by `fetch()`
- Basic status/error messages in the UI

## Project Structure

- `server.js` — Node HTTP server + API routes + static file handling
- `public/index.html` — app UI
- `public/styles.css` — styling
- `public/app.js` — client-side API calls and quiz flow

## Run locally

```bash
npm start
```

Then open: `http://localhost:3000`

## API Endpoints

- `GET /api/topics` — list available topics
- `GET /api/questions?topic=javascript` — get questions for a topic
- `POST /api/evaluate` — submit answers and receive score plus detailed review

### Example request for `/api/evaluate`

```json
{
  "topic": "javascript",
  "responses": [
    "Application Programming Interface",
    "JSON.parse()"
  ]
}
```
