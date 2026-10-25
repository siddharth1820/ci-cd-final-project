# CI/CD Final Project

## Project Overview

This project demonstrates the implementation of a Continuous Integration and Continuous Deployment (CI/CD) pipeline using GitHub Actions and OpenShift Pipelines (Tekton).

The project includes a Python-based emotion detection application, automated code linting, unit testing, and pipeline tasks for building and deploying an application.

## Objectives

- Automate code validation using GitHub Actions.
- Check Python code quality using `flake8`.
- Execute unit tests using `nose`.
- Define pipeline tasks using Tekton.
- Demonstrate application deployment using OpenShift Pipelines.

## Technologies Used

- **Python** — application logic and testing
- **Flask** — web application framework
- **GitHub** — source code management
- **GitHub Actions** — continuous integration
- **flake8** — Python code linting
- **nose** — unit testing
- **Tekton Pipelines** — CI/CD pipeline automation
- **OpenShift** — container application platform

## Project Structure

```text
ci-cd-final-project/
├── .github/
│   └── workflows/
│       └── workflow.yml
├── .tekton/
│   └── tasks.yml
├── EmotionDetection/
│   ├── __init__.py
│   ├── emotion_detection.py
│   └── test_emotion_detection.py
├── server.py
└── README.md
```

*Note: The structure above describes the expected files. Keep it consistent with the files actually present in the repository.*

## GitHub Actions Workflow

The GitHub Actions workflow is configured to run when code is pushed, a pull request is created, or the workflow is manually triggered.

The workflow performs the following operations:

1. Checks out the repository.
2. Sets up Python.
3. Installs the required dependencies.
4. Runs `flake8` to check code quality.
5. Runs unit tests using `nose`.

## Tekton Pipeline Tasks

The Tekton configuration defines tasks for:

- Cleaning the source workspace.
- Running unit tests.
- Supporting automated pipeline execution.

Additional pipeline tasks can be configured for source retrieval, code quality checks, image building, and application deployment, depending on the OpenShift pipeline configuration.

## Expected Outcome

The project aims to demonstrate an automated CI/CD workflow in which code quality checks and unit tests are performed before the application proceeds through the deployment pipeline
