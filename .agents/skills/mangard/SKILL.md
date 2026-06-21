```markdown
# mangard Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `mangard` repository, a TypeScript codebase built with the Vue framework. It covers file naming, import/export styles, commit message patterns, and testing approaches, providing clear examples and suggested commands for common workflows.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `userProfile.ts`, `dashboardView.vue`

### Import Style
- Use **relative imports** for modules.
  - Example:
    ```typescript
    import { fetchData } from './apiService'
    import { UserProfile } from '../models/userProfile'
    ```

### Export Style
- Use **named exports**.
  - Example:
    ```typescript
    // userProfile.ts
    export function getUserProfile(id: string) { ... }
    export const USER_ROLE = 'admin'
    ```

### Commit Messages
- **Freeform** style, no enforced prefixes.
- Average length: ~45 characters.
  - Example:  
    ```
    Add user authentication logic to login page
    ```

## Workflows

### Creating a New Feature
**Trigger:** When adding a new feature or module  
**Command:** `/new-feature`

1. Create a new file using camelCase naming.
2. Use relative imports to include dependencies.
3. Export functions or constants using named exports.
4. Write a freeform commit message describing the feature.

### Running Tests
**Trigger:** When verifying code correctness  
**Command:** `/run-tests`

1. Locate or create test files matching the `*.test.*` pattern.
2. Run the test suite using the project's test runner (framework unknown—refer to project documentation or package scripts).
3. Review test results and address any failures.

### Refactoring Code
**Trigger:** When improving or restructuring existing code  
**Command:** `/refactor`

1. Identify the target files (use camelCase naming for new files).
2. Update imports to use relative paths.
3. Ensure all exports remain named.
4. Update or add tests as needed.
5. Commit changes with a concise, descriptive message.

## Testing Patterns

- Test files follow the `*.test.*` naming pattern.
  - Example: `userProfile.test.ts`
- The specific testing framework is not detected; refer to project documentation for details.
- Place tests alongside the code they verify or in a dedicated `tests` directory as per project structure.

## Commands
| Command       | Purpose                                 |
|---------------|-----------------------------------------|
| /new-feature  | Scaffold and commit a new feature/module|
| /run-tests    | Run the test suite                      |
| /refactor     | Refactor code following conventions     |
```
