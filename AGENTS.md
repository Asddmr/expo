# Agents in Expo Repository

## What are Agents? (Ajanlar Nedir?)

Agents in the Expo repository refer to automated systems and tools that help with development, testing, and deployment workflows. This document explains the different types of agents used in this project.

## Types of Agents

### 1. GitHub Actions Runners (CI/CD Agents)

GitHub Actions runners are agents that execute automated workflows for continuous integration and continuous deployment (CI/CD). The Expo repository uses several types of runners:

#### Runner Types:
- **Ubuntu 24.04 runners** - Primary Linux environment for most tests and builds
- **macOS 15 runners** - Used for iOS-specific builds and tests
- **Windows 2022 runners** - Used for Windows-specific testing

#### What they do:
- Run automated tests when code is pushed
- Build applications for different platforms (Android, iOS, web)
- Check code quality and style
- Generate documentation
- Deploy preview versions

### 2. Custom GitHub Actions

The repository includes custom actions in `.github/actions/` that act as specialized agents:

- **cleanup-linux-disk-space** - Manages disk space on Linux runners
- **eas-build** - Handles Expo Application Services builds
- **expo-caches** - Manages caching for faster builds
- **expo-git-decrypt** - Handles encrypted repository secrets
- **use-android-emulator** - Sets up Android emulators for testing

### 3. Automated Testing Agents

Testing agents run automatically to ensure code quality:

- **Unit Test Runners** - Execute unit tests for individual packages
- **E2E Test Runners** - Run end-to-end tests in `bare-expo` and `test-suite`
- **Android Instrumentation Tests** - Test Android-specific functionality
- **iOS Unit Tests** - Test iOS-specific functionality

### 4. Code Quality Agents

These agents help maintain code quality:

- **Linters** - Check code style and best practices
- **Type Checkers** - Verify TypeScript types
- **Documentation Generators** - Automatically generate API documentation

### 5. Issue and PR Management Agents

Automated agents that help manage the repository:

- **Issue Triage Bot** - Automatically categorizes and labels issues
- **Stale Issue Bot** - Manages inactive issues
- **Code Review Bot** - Assists with code review processes
- **Commentator Bot** - Provides automated feedback on PRs

## How Agents Help Development

1. **Faster Feedback** - Agents run tests automatically, giving quick feedback on code changes
2. **Consistency** - Ensure all code meets quality standards
3. **Time Savings** - Automate repetitive tasks like building and testing
4. **Error Prevention** - Catch bugs and issues before they reach production
5. **Documentation** - Keep documentation up to date automatically

## Contributing and Agents

When you contribute to Expo:

1. **Push your code** - Agents automatically start testing
2. **Review CI results** - Check if agents found any issues
3. **Fix problems** - Address any failures reported by agents
4. **Merge** - Once agents approve, your code can be merged

## Viewing Agent Activity

You can see agent activity in:
- GitHub Actions tab on pull requests
- Status checks on commits
- Workflow runs in the repository's Actions tab

## Learn More

- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Contributing Guide](./CONTRIBUTING.md)
- [Expo CI/CD Workflows](.github/workflows/)

---

*This document explains the automated agents and systems used in the Expo repository to help with development, testing, and deployment.*
