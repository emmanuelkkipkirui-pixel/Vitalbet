# Contributing to Vitalbet

We appreciate your interest in contributing to Vitalbet! This document provides guidelines and instructions for contributing.

## Code of Conduct

Please be respectful and constructive in all interactions.

## How to Contribute

### Reporting Bugs

1. Check if the bug has already been reported in Issues
2. If not, create a new issue with:
   - Clear title describing the bug
   - Detailed description of the problem
   - Steps to reproduce
   - Expected vs actual behavior
   - Screenshots if applicable
   - System information

### Suggesting Features

1. Check if the feature has been suggested
2. Create a new issue with:
   - Clear title
   - Detailed description of the feature
   - Use cases and benefits
   - Any relevant mockups or examples

### Submitting Pull Requests

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Make your changes
4. Add or update tests as needed
5. Ensure code passes linting: `npm run lint`
6. Run tests: `npm test`
7. Commit with clear messages: `git commit -m "feat: description"`
8. Push to your fork: `git push origin feature/your-feature`
9. Create a Pull Request to the `develop` branch

## Development Standards

### Code Style
- Use ESLint configuration provided
- Follow Airbnb JavaScript style guide
- Use TypeScript for type safety
- Add JSDoc comments for complex functions

### Naming Conventions
- Components: PascalCase (e.g., `UserProfile.tsx`)
- Functions: camelCase (e.g., `getUserData`)
- Constants: UPPER_SNAKE_CASE (e.g., `MAX_RETRY_COUNT`)
- Database tables: snake_case (e.g., `user_accounts`)

### Testing
- Write unit tests for new functions
- Aim for >80% code coverage
- Test error cases and edge cases
- Use descriptive test names

### Database
- Create migrations for schema changes
- Never modify existing migrations
- Name migrations: `TIMESTAMP_description.sql`
- Include rollback statements

## Review Process

1. Maintainers will review your PR
2. Address feedback and make requested changes
3. CI/CD pipeline must pass
4. Minimum of 1 approval required
5. PR will be merged to `develop` branch

## Questions?

Feel free to open a discussion or reach out to the maintainers.

Thank you for contributing! 🎉
