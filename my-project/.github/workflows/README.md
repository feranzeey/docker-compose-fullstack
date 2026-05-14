# CI/CD with GitHub Actions
This project demonstrates a simple CI/CD pipeline using GitHub Actions to automatically run a Python application whenever code is pushed to the repository.

# Project Structure
```bash
.
├── .github
│   └── workflows
│       └── ci.yml
├── hello.py
└── README.md
```
# Step 1 — Create Workflow Folder
Run:

```bash
mkdir -p .github/workflows
```
# Step 2 — Create CI Workflow File

Create:

```bash
.github/workflows/ci.yml
```

Open the file in VS Code:

```bash
code .github/workflows/ci.yml
```
# Step 3 — Add GitHub Actions Workflow
Add this inside `ci.yml`:

```yaml
name: DevOps CI

on:
  push:

jobs:
  test:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v4

      - uses: actions/setup-python@v5
        with:
          python-version: "3.9"

      - run: python hello.py
```

Save the file.

# Step 4 — Push to GitHub
Run:

```bash
git add .
git commit -m "Added CI pipeline"
git push
```
# What This Pipeline Does
This GitHub Actions workflow:

- Runs automatically on every push
- Sets up Python 3.10
- Executes `hello.py`
- Helps automate testing and CI/CD processes

# Expected Output

```bash
Hello, DevOps!
```
# Technologies Used
- GitHub Actions
- Python
- Git
- GitHub

# Author
Dada Feranmi