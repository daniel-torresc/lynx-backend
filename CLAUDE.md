## Technology Stack

- **Container-based development**: Docker and docker compose
- **Git Platform**: GitHub
- **Package manager**: uv

## Common Commands

```bash
# Add new project dependency
uv add <package-name>==<version>

# Add new development dependency 
uv add --dev <package-name>==<version>

# Remove project dependency
uv remove <package-name>

# Install dependencies
uv sync

# Rebuild after source changes
uv sync --reinstall-package <package-name>

# Run all tests (unit + integration + e2e)
uv run pytest

# Unit tests only (no container required)
uv run pytest -m "not integration and not e2e"

# Just the integration tests
uv run pytest -m integration

# Just the e2e tests
uv run pytest -m e2e

# Run tests verbose
uv run pytest -v

# Run specific test file/directory
uv run pytest <path-to-test-file-directory>

# Run tests with coverage
uv run pytest --cov=<package-name>

# Lint + autofix
uv run ruff check --fix src/ tests/

# Format
uv run ruff format .

# Type check
uv run ty check
```