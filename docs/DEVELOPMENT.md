# Development Guide

## Setting Up Development Environment

### 1. Clone the Repository
```bash
git clone https://github.com/emmanuelkkipkirui-pixel/Vitalbet.git
cd Vitalbet
git checkout develop
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Database Setup

#### Create PostgreSQL Database
```bash
creatdb vitalbet
```

#### Run Migrations
```bash
cd backend
npm run migrate
```

### 4. Environment Configuration
```bash
cp .env.example .env.local
# Edit .env.local with your configuration
```

### 5. Start Development Servers
```bash
npm run dev
```

This will start:
- Frontend on http://localhost:3000
- Backend on http://localhost:5000

## Project Structure

### Frontend (/frontend)
- **src/components** - Reusable React components
- **src/pages** - Page components
- **src/services** - API service calls
- **src/hooks** - Custom React hooks
- **src/context** - Context API for state management
- **src/styles** - Tailwind CSS and global styles

### Backend (/backend)
- **src/routes** - Express route handlers
- **src/controllers** - Business logic
- **src/models** - Database models
- **src/middleware** - Express middleware
- **src/services** - Business services
- **src/utils** - Utility functions
- **migrations** - Database migrations

## Git Workflow

1. Create a feature branch from `develop`:
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. Make your changes and commit:
   ```bash
   git add .
   git commit -m "feat: describe your changes"
   ```

3. Push to GitHub:
   ```bash
   git push origin feature/your-feature-name
   ```

4. Create a Pull Request to `develop` branch

## Commit Message Convention

Use conventional commit format:
- `feat:` - New feature
- `fix:` - Bug fix
- `docs:` - Documentation
- `style:` - Code style changes
- `refactor:` - Code refactoring
- `test:` - Test updates
- `chore:` - Maintenance

Example: `feat: add user authentication`

## Testing

### Run All Tests
```bash
npm test
```

### Run Specific Test Suite
```bash
npm test -- --testPathPattern=auth
```

### Coverage
```bash
npm test -- --coverage
```

## Code Quality

### Linting
```bash
npm run lint
```

### Fix Linting Issues
```bash
npm run lint -- --fix
```

## Debugging

### Backend Debugging
```bash
node --inspect-brk=localhost:9229 backend/src/index.js
```

Then open Chrome DevTools at `chrome://inspect`

## Useful Commands

- `npm run build` - Build for production
- `npm run test` - Run tests
- `npm run lint` - Check code quality
- `npm run dev` - Start development servers

## Resources

- [Express.js Documentation](https://expressjs.com/)
- [React Documentation](https://react.dev/)
- [PostgreSQL Documentation](https://www.postgresql.org/docs/)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
