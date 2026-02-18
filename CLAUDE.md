# Development Guidelines

## Language

All development must be in English. Even if the user speaks French, all commits, documentation, code, and communication must be in English.

## Safety Rules

### Never Commit Dangerous Changes to Main

Never commit or push anything dangerous to the main branch, including:

- Destructive commands (git reset --hard, git clean -f, etc.)
- Removing safety checks
- Bypassing pre-commit hooks with --no-verify unless explicitly instructed
- Force pushes to main/master

### Always Verify Before Acting

Never assume that something doesn't exist in the project. Always analyze the codebase to verify:

- Check if files already exist before creating new ones
- Verify if a feature is already implemented
- Search for existing solutions before implementing new ones
- Confirm that the changes haven't already been made

When in doubt, use Grep, Glob, or Task tools to explore the codebase.

### Critical Thinking

Do not always agree with the user. Speak with reality and facts:

- Question assumptions that seem incorrect
- Point out potential issues or risks
- Suggest better alternatives when applicable
- Challenge decisions that might not be optimal

### Stay Updated

When things seem outdated or unclear, look them up on the web. This includes:

- Checking if dependencies are outdated
- Verifying that documentation is still accurate
- Researching best practices
- Confirming that tools/frameworks are still supported

---

## Git Commit Convention

All commits MUST include both co-authors:

- `martty-code <nesalia.inc@gmail.com>`
- `Claude Sonnet <noreply@anthropic.com>`

### Commit Message Format

```bash
git commit -m "$(cat <<'EOF'
Your commit message here

Co-Authored-By: martty-code <nesalia.inc@gmail.com>
Co-Authored-By: Claude Sonnet <noreply@anthropic.com>
EOF
)"
```

### Example

```bash
git commit -m "$(cat <<'EOF'
feat: add employee search functionality

Implement search bar with real-time filtering for employee list

Co-Authored-By: martty-code <nesalia.inc@gmail.com>
Co-Authored-By: Claude Sonnet <noreply@anthropic.com>
EOF
)"
```
