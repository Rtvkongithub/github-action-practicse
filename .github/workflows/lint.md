# Lint in CI/CD

## What is Lint?

Lint is the process of analyzing source code to detect:

* Syntax errors
* Coding style issues
* Unused variables or imports
* Potential bugs
* Bad coding practices

It helps improve code quality before the code is built or deployed.

## Why Use Lint?

* Finds errors early
* Maintains consistent coding style
* Improves code readability
* Reduces bugs
* Saves debugging time

## Lint in GitHub Actions

A lint job is usually executed after the code is checked out and before the build stage.

Example workflow:

```yaml
jobs:
  lint:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - name: Run Lint
        run: echo "Running lint checks"
```

## Common Lint Tools

| Language   | Lint Tool      |
| ---------- | -------------- |
| JavaScript | ESLint         |
| Python     | Pylint, Flake8 |
| Java       | Checkstyle     |
| Go         | golangci-lint  |
| Docker     | Hadolint       |
| YAML       | yamllint       |

## CI/CD Flow

```
Code
  ↓
Lint
  ↓
Build
  ↓
Test
  ↓
Deploy
```

If the lint step fails, the workflow stops and the code is not built or deployed.

## Summary

* Lint checks code quality.
* It catches errors before building the application.
* It enforces coding standards.
* Lint is commonly the first validation step in a CI/CD pipeline.
