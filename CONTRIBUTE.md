# Contribution Guide

Thank you for your interest in contributing to our project. This guide outlines the process for effective contribution.

## Opening an Issue

1. **Verify latest version** before opening an issue
2. **Check for duplicates** in existing issues
3. **Complete the issue template** with all required information
4. **Use proper formatting** for code blocks and logs
5. **Provide clear reproduction steps** when applicable

## Branch Naming

```
<type>-<description>
```

**Types:** `feature/`, `bugfix/`, `hotfix/`, `refactor/`, `docs/`, `test/`, `chore/`

**Examples:**
- `feature/user-authentication`
- `bugfix/login-error-handling`

## Commit Messages

```
<type>(<scope>): <short summary>
```

**Examples:**
- `feat(auth): Add login functionality`
- `fix(payment): Resolve transaction timeout`

## Pull Request Naming

```
Issue #<issue-number>: <Description of changes>
```

**Example:**
- `Issue #14631: Update escaping to non-escaping in JavadocTokenTypes.java`

## Pull Request Process

1. **Assign the issue to yourself**
2. **Create a properly named branch**
3. **Ensure tests pass locally** (`mvn clean verify`)
4. **Submit PR following the template**
5. **Reference the issue** in the PR description
8. **Respond to all reviewer comments**
9. **Rebase on latest master** when updating (Run **`git rebase main`** before pushing changes)

### How to Rebase Your Branch
If you are new to open-source contributions, follow these steps to properly rebase your branch:

1. Ensure you are on your feature branch:
   ```sh
   git checkout <your-branch>
   ```
2. Fetch the latest changes from the main branch:
   ```sh
   git fetch origin main
   ```
3. Rebase your branch on top of the latest main branch:
   ```sh
   git rebase origin/main
   ```
4. If there are conflicts, resolve them and continue the rebase:
   ```sh
   git add <resolved-files>
   git rebase --continue
   ```
5. Push your changes forcefully to update the PR:
   ```sh
   git push origin <your-branch> --force
   ```

## How to Amend a Commit
If you need to modify the latest commit (e.g., fix a typo or add missing changes), you can use `git commit --amend`:

1. Make the necessary changes in your files.
2. Add the changes to the staging area:
   ```sh
   git add <modified-files>
   ```
3. Amend the last commit:
   ```sh
   git commit --amend
   ```
   This will open your default text editor, allowing you to modify the commit message if needed.
4. Push the amended commit forcefully:
   ```sh
   git push origin <your-branch> --force
   ```

## Pull Request Example

```
Title: Issue #14631: Updated escaping to non-escaping in JavadocTokenTypes.java

Description:
This PR addresses issue #14631 by updating the escaping behavior in JavadocTokenTypes.java

Changes:
- Modified escapeJavadocTokenTypes method to handle new AST format
- Updated unit tests to verify non-escaping behavior
- Added documentation for the new approach

Verification:
- All tests passing locally
- Ran diff report showing no negative regressions
```

## Best Practices

1. Use descriptive names for branches and PRs
2. Include issue numbers for traceability
3. Keep PRs focused on a single concern
4. Maintain consistent code style
5. Do not close and recreate PRs

Remember that all contributors must adhere to our Code of Conduct. We appreciate your contributions.
A full-stack clone of the Tazkarti ticket booking platform, enabling users to browse events, reserve seats, and purchase tickets. Built with Spring Boot using a microservices architecture

