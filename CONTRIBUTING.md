# Contributing Guide

First of all, thank you for your interest in contributing to a **Broetec** project! 🎉

This document provides the technical guidelines to set up your development environment, run tests, and submit your improvements. Since we standardize our automation via `Makefile`, the commands below should work across all our Python projects.

---

## 🚀 Initial Setup

### 1. Fork and Clone
1. **Fork** this repository to your own GitHub account.
2. Clone your fork locally:
  ```bash
  git clone [https://github.com/YOUR_USERNAME/](https://github.com/YOUR_USERNAME/)<PROJECT_NAME>.git
  cd <PROJECT_NAME>
  ```

### 2. Development Environment

We use [uv](https://github.com/astral-sh/uv) for Python version and dependency management.

  * **Install everything (Venv + Dependencies):**
    ```bash
    make install
    ```
  * **Configure Git Hooks (Linter/Commits):**
    This ensures your code follows our standards before every commit.
    ```bash
    make pre-commit-install
    ```

-----

## 🛠 Development Cycle

To maintain code quality, please use the `Makefile` shortcuts. You can see all available commands by simply typing `make`.

### Code Quality

  * **Format and auto-fix issues:** `make format`
  * **Validate linting rules:** `make lint`

### Testing and Coverage

  * **Run tests locally:** `make test`
  * **Run tests via Docker:** `make docker-test`
  * **Validate Minimum Coverage (CI Check):**
    ```bash
    make test-coverage-ci
    ```
    > **Note:** The CI pipeline will fail if the code coverage is below the threshold defined in the Makefile (default: 90%).

-----

## 📦 Submission Process (Workflow)

1.  **Create a Branch:** Use semantic prefixes (e.g., `feat/`, `fix/`, `docs/`).
    ```bash
    git checkout -b feat/your-feature-name
    ```
2.  **Develop:** Implement your changes and add corresponding tests.
3.  **Validate:** Run `make format` and `make test` to ensure everything is correct.
4.  **Commits:** Follow the [Conventional Commits](https://www.conventionalcommits.org/) standard (e.g., `feat: add open-search validation`).
5.  **Pull Request:** Open a PR to the `main` branch. Clearly describe your changes and link any related Issues. Please fill out our standardized template: [**Pull Request Template**](https://github.com/Broetec/.github/blob/main/.github/pull_request_template.md)
  > **Important:** Your PR will not be merged if the code coverage is below the **90%** threshold or if any tests fail.

-----

## ⚖️ Community Standards

By participating in this project, you agree to abide by our [**Code of Conduct**](https://github.com/Broetec/.github/blob/main/CODE_OF_CONDUCT.md)

-----

## 📬 Contact

If you need help or have questions:

1.  **Technical issues/Questions:** Please [**open an issue**](https://github.com/Broetec/.github/tree/main/.github/ISSUE_TEMPLATE) using the appropriate template.
2.  **Sensitive Matters:** For reporting Code of Conduct violations or security vulnerabilities, please use the contact email provided in the [Code of Conduct](https://github.com/Broetec/.github/blob/main/CODE_OF_CONDUCT.md).
