# CLAUDE.md - AI Assistant Guide for claude-code

This file provides context and guidelines for AI assistants working with this repository.

## Project Overview

**Repository:** claude-code
**Status:** Initial setup phase - awaiting project initialization
**Purpose:** To be defined as the project develops
**Created:** 2025-11-17

## Current State

> **Important:** This repository is in its initial setup phase. No source code, package configuration, or build tooling has been implemented yet.

### Actual Project Structure

```
claude-code/
├── .git/                    # Git repository
├── .github/
│   └── workflows/
│       └── blank.yml        # Placeholder CI workflow (needs implementation)
└── CLAUDE.md                # This file - AI assistant guidelines
```

### What Exists
- **CLAUDE.md** - This documentation file with development guidelines
- **GitHub Actions workflow** - Basic template at `.github/workflows/blank.yml` (placeholder only)

### What Does NOT Exist Yet
- No `package.json` or `node_modules/`
- No `src/` directory or source code
- No `tests/` directory or test files
- No `tsconfig.json` or build configuration
- No linting/formatting configuration
- No `README.md`, `LICENSE`, or other standard docs
- No `.env.example` or environment configuration

## Getting Started (For New Development)

Since this is a fresh repository, the first steps should be:

```bash
# 1. Initialize Node.js project
npm init -y

# 2. Install core dependencies (adjust based on project needs)
npm install typescript --save-dev
npm install @types/node --save-dev

# 3. Create TypeScript configuration
npx tsc --init

# 4. Set up project structure
mkdir -p src tests docs scripts

# 5. Install linting and formatting
npm install eslint prettier --save-dev
npm install @typescript-eslint/parser @typescript-eslint/eslint-plugin --save-dev
```

## Development Guidelines

### Code Style and Conventions (To Be Followed Once Development Begins)

1. **Language:** TypeScript (preferred) or JavaScript
2. **Formatting:** Prettier with default settings
3. **Linting:** ESLint with recommended TypeScript rules
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
   - Documentation: `docs/description`
   - Claude AI branches: `claude/session-id`

2. **Commit Messages:**
   - Use conventional commits format
   - Present tense, imperative mood
   - Examples:
     - `feat: add user authentication`
     - `fix: resolve null pointer in parser`
     - `docs: update API documentation`
     - `refactor: simplify error handling`
     - `test: add unit tests for parser`
     - `chore: update dependencies`

3. **Pull Requests:**
   - Include clear description of changes
   - Reference related issues when applicable
   - Ensure all tests pass before merging

### Testing Strategy (To Be Implemented)

- Write unit tests for all new functionality
- Aim for high test coverage (>80%)
- Use descriptive test names that explain expected behavior
- Include edge cases and error conditions
- Recommended frameworks: Jest or Vitest

### Documentation Standards

- Document public APIs with JSDoc/TSDoc comments
- Keep README.md up to date
- Update this CLAUDE.md file as the project evolves
- Add inline comments for complex logic only (code should be self-documenting)

## AI Assistant Instructions

### When Working on This Codebase

1. **Before Making Changes:**
   - Read relevant existing code to understand patterns
   - Check for existing utilities before creating new ones
   - Review test files to understand expected behavior
   - Check this CLAUDE.md for current conventions

2. **Code Quality:**
   - Follow existing code style and patterns
   - Write type-safe code (avoid `any` types in TypeScript)
   - Handle errors appropriately with proper error messages
   - Consider edge cases and input validation

3. **Security Considerations:**
   - Never commit sensitive data (API keys, passwords, tokens)
   - Validate all user inputs
   - Be cautious with file system operations
   - Avoid command injection vulnerabilities
   - Sanitize data before database queries

4. **Performance:**
   - Consider time and space complexity
   - Avoid unnecessary computations
   - Use appropriate data structures
   - Be mindful of memory usage

### Common Tasks

#### Setting Up the Project (Current Priority)
1. Initialize `package.json` with appropriate metadata
2. Configure TypeScript with `tsconfig.json`
3. Set up linting and formatting tools
4. Create initial project structure (`src/`, `tests/`, etc.)
5. Configure CI/CD pipeline properly
6. Add essential documentation (README.md, LICENSE)

#### Adding a New Feature
1. Create feature branch from main
2. Write tests first (TDD approach recommended)
3. Implement the feature with proper types
4. Update documentation as needed
5. Ensure all tests pass
6. Create pull request with clear description

#### Fixing a Bug
1. Reproduce the issue
2. Write a failing test that captures the bug
3. Fix the bug
4. Verify the fix doesn't break existing functionality
5. Update tests if needed
6. Document the fix in commit message

#### Refactoring
1. Ensure comprehensive test coverage exists first
2. Make incremental, small changes
3. Run tests after each change
4. Maintain backward compatibility when possible
5. Update documentation if APIs change

## Environment Setup

### Prerequisites

- Node.js >= 18.x (LTS recommended)
- npm >= 9.x
- Git
- Code editor with TypeScript support (VS Code recommended)

### Initial Setup (Once Project Is Initialized)

```bash
# Clone the repository
git clone <repository-url>
cd claude-code

# Install dependencies
npm install

# Set up environment variables (if applicable)
cp .env.example .env
# Edit .env with your configuration

# Run tests to verify setup
npm test

# Start development
npm run dev
```

## Architecture Decisions

> Document important architectural decisions here as the project evolves.

### ADR-001: Project Initialization
- **Date:** 2025-11-17
- **Status:** Pending
- **Context:** Need to establish the foundational architecture and tooling
- **Decision:** TBD - awaiting project requirements definition
- **Consequences:** Will affect all future development choices

## CI/CD Configuration

### Current State
The GitHub Actions workflow at `.github/workflows/blank.yml` is a placeholder template that:
- Triggers on push/PR to a specific branch
- Runs on `ubuntu-latest`
- Only contains "Hello, world!" echo statements

### Recommended Next Steps for CI/CD
1. Add Node.js setup action
2. Cache npm dependencies
3. Run linting checks
4. Run test suite
5. Build the project
6. (Optional) Deploy or publish artifacts

Example workflow structure:
```yaml
- uses: actions/checkout@v4
- uses: actions/setup-node@v4
  with:
    node-version: '18'
    cache: 'npm'
- run: npm ci
- run: npm run lint
- run: npm test
- run: npm run build
```

## Priority TODOs

### High Priority (Project Setup)
- [ ] Create `package.json` with project metadata and scripts
- [ ] Set up TypeScript configuration (`tsconfig.json`)
- [ ] Create initial project directory structure
- [ ] Add ESLint configuration
- [ ] Add Prettier configuration
- [ ] Update GitHub Actions workflow with real CI steps

### Medium Priority (Documentation)
- [ ] Create `README.md` with project overview
- [ ] Add `LICENSE` file
- [ ] Create `CONTRIBUTING.md` guidelines
- [ ] Add `CODE_OF_CONDUCT.md`
- [ ] Set up `.env.example` template

### Lower Priority (As Development Progresses)
- [ ] Set up documentation generation (TypeDoc or similar)
- [ ] Configure code coverage reporting
- [ ] Add pre-commit hooks (Husky + lint-staged)
- [ ] Set up semantic versioning
- [ ] Configure automated releases

## Resources

### To Be Created
- [Project Documentation](./docs/) - Not yet created
- [Contributing Guidelines](./CONTRIBUTING.md) - Not yet created
- [Code of Conduct](./CODE_OF_CONDUCT.md) - Not yet created
- [License](./LICENSE) - Not yet created
- [README](./README.md) - Not yet created

### External Resources
- [TypeScript Documentation](https://www.typescriptlang.org/docs/)
- [ESLint Documentation](https://eslint.org/docs/)
- [Prettier Documentation](https://prettier.io/docs/)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [GitHub Actions](https://docs.github.com/en/actions)

## Version History

- **v0.0.2** - 2025-11-17
  - Updated CLAUDE.md to reflect actual repository state
  - Added accurate current structure documentation
  - Prioritized setup TODOs
  - Enhanced AI assistant instructions

- **v0.0.1** - 2025-11-17
  - Created initial CLAUDE.md template
  - Established development conventions
  - Added placeholder GitHub Actions workflow

---

*Last updated: 2025-11-17*

*This file should be updated as the project evolves to reflect current practices, structure, and state.*
