# CLAUDE.md - AI Assistant Guide for claude-code

This file provides context and guidelines for AI assistants working with this repository.

## Project Overview

**Repository:** claude-code
**Status:** Initial setup phase
**Purpose:** [To be defined as the project develops]

## Quick Reference

### Essential Commands

```bash
# Development
npm install          # Install dependencies
npm run dev          # Start development server
npm run build        # Build for production
npm test             # Run test suite
npm run lint         # Run linter
npm run format       # Format code
```

### Project Structure (Planned)

```
claude-code/
├── src/                  # Source code
│   ├── components/       # UI components (if applicable)
│   ├── lib/             # Core library code
│   ├── utils/           # Utility functions
│   └── types/           # TypeScript type definitions
├── tests/               # Test files
├── docs/                # Documentation
├── scripts/             # Build and automation scripts
├── .github/             # GitHub workflows and templates
├── package.json         # Dependencies and scripts
├── tsconfig.json        # TypeScript configuration
└── CLAUDE.md           # This file
```

## Development Guidelines

### Code Style and Conventions

1. **Language:** TypeScript (preferred) or JavaScript
2. **Formatting:** Use Prettier with default settings
3. **Linting:** ESLint with recommended rules
4. **Naming Conventions:**
   - Files: kebab-case (`my-component.ts`)
   - Classes: PascalCase (`MyComponent`)
   - Functions/Variables: camelCase (`myFunction`)
   - Constants: SCREAMING_SNAKE_CASE (`MAX_RETRIES`)
   - Types/Interfaces: PascalCase with descriptive names

### Git Workflow

1. **Branch Naming:**
   - Features: `feature/description`
   - Bug fixes: `fix/description`
   - Claude branches: `claude/session-id`

2. **Commit Messages:**
   - Use conventional commits format
   - Present tense, imperative mood
   - Examples:
     - `feat: add user authentication`
     - `fix: resolve null pointer in parser`
     - `docs: update API documentation`
     - `refactor: simplify error handling`

3. **Pull Requests:**
   - Include clear description of changes
   - Reference related issues
   - Ensure all tests pass before merging

### Testing Strategy

- Write unit tests for all new functionality
- Aim for high test coverage (>80%)
- Use descriptive test names that explain the expected behavior
- Include edge cases and error conditions

### Documentation

- Document public APIs with JSDoc/TSDoc comments
- Keep README.md up to date
- Update this CLAUDE.md file as the project evolves
- Add inline comments for complex logic only

## AI Assistant Instructions

### When Working on This Codebase

1. **Before Making Changes:**
   - Read relevant existing code to understand patterns
   - Check for existing utilities before creating new ones
   - Review test files to understand expected behavior

2. **Code Quality:**
   - Follow existing code style and patterns
   - Write type-safe code (avoid `any` types)
   - Handle errors appropriately
   - Consider edge cases

3. **Security Considerations:**
   - Never commit sensitive data (API keys, passwords)
   - Validate all user inputs
   - Be cautious with file system operations
   - Avoid command injection vulnerabilities

4. **Performance:**
   - Consider time and space complexity
   - Avoid unnecessary computations
   - Use appropriate data structures

### Common Tasks

#### Adding a New Feature
1. Create feature branch
2. Write tests first (TDD approach)
3. Implement the feature
4. Update documentation
5. Ensure all tests pass
6. Create pull request

#### Fixing a Bug
1. Reproduce the issue
2. Write a failing test
3. Fix the bug
4. Verify the fix doesn't break existing functionality
5. Update tests if needed

#### Refactoring
1. Ensure comprehensive test coverage exists
2. Make incremental changes
3. Run tests after each change
4. Maintain backward compatibility when possible

## Environment Setup

### Prerequisites

- Node.js >= 18.x
- npm >= 9.x
- Git

### Initial Setup

```bash
# Clone the repository
git clone <repository-url>
cd claude-code

# Install dependencies
npm install

# Set up environment variables (if needed)
cp .env.example .env

# Run tests to verify setup
npm test
```

## Architecture Decisions

> Document important architectural decisions here as the project evolves.

### ADR-001: [Title]
- **Date:** [Date]
- **Status:** [Proposed/Accepted/Deprecated]
- **Context:** [Why this decision was needed]
- **Decision:** [What was decided]
- **Consequences:** [What are the implications]

## Known Issues and TODOs

- [ ] Set up CI/CD pipeline
- [ ] Configure linting and formatting
- [ ] Add comprehensive test coverage
- [ ] Set up documentation generation
- [ ] Define project architecture

## Resources

- [Project Documentation](./docs/)
- [Contributing Guidelines](./CONTRIBUTING.md)
- [Code of Conduct](./CODE_OF_CONDUCT.md)
- [License](./LICENSE)

## Version History

- **v0.0.1** - Initial repository setup
  - Created CLAUDE.md for AI assistant guidance
  - Established initial project structure conventions

---

*Last updated: 2025-11-17*

*This file should be updated as the project evolves to reflect current practices and structure.*
