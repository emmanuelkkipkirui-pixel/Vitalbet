# Vitalbet Setup Guide

## Prerequisites

- Node.js 18+
- Docker & Docker Compose
- PostgreSQL 15+
- Git

## Installation Steps

### 1. Clone the Repository

```bash
git clone https://github.com/emmanuelkkipkirui-pixel/Vitalbet.git
cd Vitalbet
```

### 2. Setup Environment Variables

```bash
cp .env.example .env
# Edit .env with your configuration
```

### 3. Install Dependencies

**Backend:**
```bash
cd backend
npm install
```

**Frontend:**
```bash
cd ../frontend
npm install
```

### 4. Run with Docker Compose

```bash
cd ..
docker-compose up -d
```

This will start:
- PostgreSQL on localhost:5432
- Backend API on localhost:5000
- Frontend on localhost:3000

### 5. Database Setup

```bash
cd backend
npm run migrate
npm run seed
```

## Development

### Backend Development

```bash
cd backend
npm run dev
```

### Frontend Development

```bash
cd frontend
npm run dev
```

## Testing

### Run All Tests

```bash
# Backend
cd backend
npm test

# Frontend
cd ../frontend
npm test
```

### Run with Coverage

```bash
npm test:coverage
```

## Building for Production

### Backend Build

```bash
cd backend
npm run build
```

### Frontend Build

```bash
cd ../frontend
npm run build
```

## Docker Deployment

```bash
docker-compose -f docker-compose.yml up -d
```

## Troubleshooting

### Port Already in Use

```bash
# Kill process on specific port
lsof -ti:5000 | xargs kill -9  # Backend
lsof -ti:3000 | xargs kill -9  # Frontend
```

### Database Connection Issues

Ensure PostgreSQL is running and connection string is correct in .env

### Docker Issues

```bash
# Clean up Docker resources
docker-compose down -v
docker system prune -a
```
