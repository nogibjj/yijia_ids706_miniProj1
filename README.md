# yijia_ids706_miniProj1

## Python Template

This project demonstrates how to create a standard Python project scaffolding, dockerize the project, and set up a CI/CD process.

![CI/CD](https://github.com/<username>/<repository>/actions/workflows/<workflow-file>.yaml/badge.svg)

## File Structure

- **`.devcontainer/`**: Contains the development container configuration (`devcontainer.json` and often a Dockerfile) to ensure consistency, portability, and isolation for the development environment.
- **`Makefile`**: Provides commands for setup, testing, linting, and other tasks, making it easier to use command-line entries and integrate with CI/CD workflows.
- **`.github/workflows/`**: Contains CI/CD workflows for GitHub, which trigger actions like setup, linting, and testing when code is pushed to the repository.

## Setup

### 1. Clone the Repository

```bash
git clone <repository-url>
```

### 2. Open the repository in Visual Studio Code
- Reopen in container to use the .devcontainer configuration.
- Rebuild the container if necessary, ensuring Docker is running on your computer.

### 3. Install dependencies
Run the following command to install all required dependencies:

```bash
make install
```

## Usage
- make install: Installs dependencies specified in requirements.txt.
- make format: Formats Python files using Black.
- make lint: Lints Python files using Pylint, ignoring specific patterns.
- make test: Runs tests using pytest and generates a coverage report.
- make clean: Removes pytest cache.

## CI/CD Setup
- Location: .github/workflows/
- Description: Contains GitHub Actions workflows for CI/CD, which automatically run setup, lint, and test actions on pushes to the GitHub repository.