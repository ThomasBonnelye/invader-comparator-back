# Invader Comparator Backend

Backend API for the Invader Comparator application, built with Express, TypeScript, and MongoDB.

## Tech Stack

- Node.js with TypeScript
- Express for the API
- MongoDB with Mongoose
- Passport.js for Google OAuth authentication
- Docker for containerization

## Getting Started

### Prerequisites

- Docker and Docker Compose
- A MongoDB instance (local or cloud)
- Google OAuth credentials

### Environment Setup

Copy the example environment file and fill in your values:

```bash
cp .env.example .env
```

Required environment variables:
- `MONGODB_URI` - Your MongoDB connection string
- `SESSION_SECRET` - A random string for session encryption
- `GOOGLE_CLIENT_ID` - Your Google OAuth client ID
- `GOOGLE_CLIENT_SECRET` - Your Google OAuth client secret
- `FRONTEND_URL` - URL of your frontend application
- `PORT` - Server port (default: 3001)

### Running with Docker

Build and start the container:

```bash
docker compose up --build
```

The API will be available at `http://localhost:3001`

### Local Development

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Build for production:

```bash
npm run build
npm start
```

## Project Structure

```
src/
├── config/          # Configuration files (Passport, etc.)
├── models/          # Mongoose models
├── routes/          # API routes
└── server.ts        # Application entry point
```

## API Routes

- `GET /` - Health check
- `/api/auth/*` - Authentication endpoints (Google OAuth)
- `/api/uids/*` - UIDs management endpoints

## Notes

This project uses ES modules (`"type": "module"` in package.json). The TypeScript configuration is set up for modern Node.js with ESM support.
