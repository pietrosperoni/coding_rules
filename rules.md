# Project Rules

## 0. Multi-Repository Awareness
- Each distinct component should exist in its own repository
- Respect repository boundaries; only modify files within the target repository
- When working within a parent folder containing multiple repositories, be explicit about which repository you're modifying
- Cross-repository changes must be implemented separately in each affected repository

## 1. Technology Consistency
- Use consistent technology choices across repositories when they interact
- Share common configuration files and environment definitions when possible
- Maintain version compatibility between interacting components
- Document API contracts between repositories clearly

## 2. Code Quality Standards
- Follow PEP 8 style guide for all Python code
- Maximum line length: 88 characters
- Add docstrings to all public functions, classes, and modules
- Use type hints for function parameters and return values
- Keep files under 300 lines; split larger files into logical components
- Avoid duplication across repositories; create shared libraries if necessary
- Commit messages: present-tense, ≤ 72 characters summary

## 3. Error Handling
- Use consistent error handling patterns across repositories
- Log errors with appropriate context for troubleshooting
- Define clear error boundaries between components
- Handle cross-component failures gracefully

## 4. Testing Strategy
- Write tests for core functionality in each repository
- Test component interactions where repositories interface
- Target 80% code coverage minimum (100% for authentication and data persistence)
- Keep tests deterministic and repeatable
- Test integrated functionality across repository boundaries
- Mock external dependencies, including other repositories
- When fixing bugs, first write a test that reproduces the issue

## 5. Environment Management
- Use a single shared environment definition when possible
- Clearly separate development, testing, and production configurations
- Keep production code in `src/` and test code in `tests/` consistently
- Maintain separate dependency lists for production vs. development
- Ensure test code never runs in production environments

## 6. Documentation
- Document cross-repository dependencies and interactions
- Maintain API documentation at repository boundaries
- Keep README files updated in each repository
- Document setup procedures considering the multi-repository context

## 7. AI-Assisted Development Guidelines
- Make narrow, specific requests when using AI tools
- Always specify which repository is being modified
- Review generated code carefully, especially cross-repository interactions
- Never allow AI to modify configuration files (`.env`, `environment.yml`, etc.)
- Check for existing implementations before adding new code
- Ensure AI-generated code follows existing patterns in the target repository

## 8. Security Practices
- Never store sensitive information in code or source control
- Validate all inputs at repository boundaries
- Use secure random generators for tokens and IDs
- Apply consistent security practices across all repositories
- Treat inter-repository communication as potentially untrusted

## 9. Safety Measures
- Run syntax validation before each commit
- Test components individually and in integration
- Verify that components still work together after changes
- Use CI/CD to validate cross-repository compatibility