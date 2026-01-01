# Contributing Guide

Thank you for your interest in contributing to this project! This guide will help you understand our development process and how to submit contributions.

## Table of Contents

- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Code Standards](#code-standards)
- [Commit Guidelines](#commit-guidelines)
- [Pull Request Process](#pull-request-process)
- [Code Review](#code-review)
- [Branching Strategy](#branching-strategy)

## Getting Started

1. **Fork the repository** (for external contributors)
   - Click the "Fork" button at the top right of the repository page

2. **Clone your fork**
   ```bash
   git clone https://github.com/YOUR-USERNAME/template.git
   cd template
   ```

3. **Add the upstream remote**
   ```bash
   git remote add upstream https://github.com/eng618/template.git
   ```

4. **Keep your fork synchronized**
   ```bash
   git fetch upstream
   git checkout develop
   git merge upstream/develop
   ```

## Development Workflow

We follow a Git Flow-inspired workflow. Please read our [Branching Strategy](BRANCHING.md) for detailed information.

### Quick Workflow Summary

1. Create a feature branch from `develop`
2. Make your changes
3. Test your changes
4. Commit with clear messages
5. Push to your fork
6. Create a Pull Request to `develop`
7. Address review feedback
8. Celebrate when your PR is merged! 🎉

## Code Standards

### General Guidelines

- Write clear, readable, and maintainable code
- Follow the existing code style and conventions in the repository
- Add comments for complex logic or non-obvious decisions
- Keep functions and methods focused and single-purpose
- Write self-documenting code with meaningful variable and function names

### Documentation

- Update documentation when changing functionality
- Add docstrings/comments for public APIs and complex functions
- Include examples in documentation when helpful
- Keep README files up to date

### Testing

- Write tests for new features and bug fixes
- Ensure all tests pass before submitting a PR
- Maintain or improve code coverage
- Include both positive and negative test cases

## Commit Guidelines

We recommend following [Conventional Commits](https://www.conventionalcommits.org/) format:

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Commit Types

- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Code style changes (formatting, missing semi-colons, etc.)
- `refactor`: Code refactoring without changing functionality
- `perf`: Performance improvements
- `test`: Adding or updating tests
- `chore`: Maintenance tasks, dependency updates, etc.
- `ci`: CI/CD configuration changes

### Examples

```bash
feat(api): add user authentication endpoint

fix(parser): handle edge case with empty input

docs(readme): update installation instructions

chore(deps): update dependencies to latest versions
```

## Pull Request Process

### Before Submitting

1. **Update your branch**
   ```bash
   git checkout develop
   git pull upstream develop
   git checkout your-feature-branch
   git rebase develop
   ```

2. **Run tests**
   - Ensure all tests pass
   - Add new tests if needed

3. **Review your changes**
   - Double-check that you're only changing what's necessary
   - Remove debugging code, console logs, or commented-out code
   - Ensure no sensitive information is included

### Submitting a Pull Request

1. **Push your branch**
   ```bash
   git push origin your-feature-branch
   ```

2. **Create the PR**
   - Go to the repository on GitHub
   - Click "New Pull Request"
   - Select `develop` as the base branch (unless it's a hotfix)
   - Select your feature branch as the compare branch
   - Fill out the PR template with all relevant information

3. **PR Title**
   - Use a clear, descriptive title
   - Follow the conventional commit format if possible
   - Example: `feat: add user authentication system`

4. **PR Description**
   - Explain what changes were made and why
   - Link to related issues (e.g., "Closes #123")
   - Include screenshots for UI changes
   - List any breaking changes
   - Describe how to test the changes

### PR Checklist

- [ ] My code follows the project's code style
- [ ] I have performed a self-review of my code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings or errors
- [ ] I have added tests that prove my fix is effective or that my feature works
- [ ] New and existing unit tests pass locally with my changes
- [ ] Any dependent changes have been merged and published

## Code Review

### For Contributors

- Be responsive to feedback and questions
- Be open to suggestions and willing to make changes
- Ask for clarification if feedback is unclear
- Update your PR based on review comments
- Mark conversations as resolved after addressing them

### Review Process

1. **Automated Checks**
   - CI pipelines must pass
   - Code coverage should be maintained or improved
   - Linting and formatting checks must pass

2. **Peer Review**
   - At least one reviewer must approve the PR
   - Reviewers will check code quality, logic, and adherence to standards
   - Address all review comments before merging

3. **Final Approval**
   - Once approved and all checks pass, a maintainer will merge the PR
   - The feature branch will be deleted after merging

## Branching Strategy

We use a two-branch strategy with `main` and `develop` as primary branches.

- **`main`**: Production-ready code, always deployable
- **`develop`**: Integration branch for development

For complete details, see [BRANCHING.md](BRANCHING.md).

### Branch Naming Conventions

- Feature: `feature/description` or `feat/description`
- Bug fix: `fix/description` or `bugfix/description`
- Hotfix: `hotfix/description`
- Documentation: `docs/description`
- Chore: `chore/description`

### Examples

```bash
feature/user-authentication
fix/login-validation-error
hotfix/critical-security-patch
docs/update-api-documentation
chore/update-dependencies
```

## Reporting Issues

### Bug Reports

When reporting a bug, please include:

- A clear and descriptive title
- Steps to reproduce the issue
- Expected behavior
- Actual behavior
- Environment information (OS, browser, version, etc.)
- Screenshots or error messages if applicable

### Feature Requests

When requesting a feature, please include:

- A clear and descriptive title
- The problem or need the feature would address
- Proposed solution or implementation ideas
- Any alternatives you've considered
- Additional context or examples

## Security Issues

Please do not report security vulnerabilities through public GitHub issues.

Instead, please refer to our [Security Policy](../SECURITY.md) for instructions on how to report security vulnerabilities responsibly.

## Code of Conduct

### Our Pledge

We are committed to providing a welcoming and inclusive environment for everyone, regardless of:

- Age, body size, disability, ethnicity, gender identity and expression
- Level of experience, education, socio-economic status
- Nationality, personal appearance, race, religion
- Sexual identity and orientation

### Expected Behavior

- Be respectful and inclusive
- Welcome newcomers and help them get started
- Be collaborative and constructive in discussions
- Accept constructive criticism gracefully
- Focus on what is best for the community

### Unacceptable Behavior

- Harassment, trolling, or discriminatory comments
- Personal or political attacks
- Publishing others' private information without permission
- Any conduct that could be considered inappropriate in a professional setting

## Questions?

If you have questions about contributing, feel free to:

- Open an issue with the `question` label
- Reach out to the maintainers
- Check existing documentation and issues first

## License

By contributing, you agree that your contributions will be licensed under the same license as the project (see [LICENSE](../LICENSE)).

---

Thank you for contributing! Your efforts help make this project better for everyone. 🙌
