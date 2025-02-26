# Markdown Quality Assurance Guide

## Overview
To maintain high-quality documentation in this repository, we use **Vale** and **markdownlint-cli** to ensure consistency, clarity, and adherence to style guidelines. All contributors must follow these guidelines before submitting any markdown files to the repository.

## Setup Instructions
### 1. Install Dependencies
Before running the quality checks, ensure you are inside the **DevContainer**:
- If using **GitHub Codespaces**, the DevContainer starts automatically.
- If using **VS Code**, click the **blue button** in the bottom-left corner and select **"Reopen in Container"**.

### 2. Running Quality Checks
Inside the DevContainer terminal, navigate to the repository root and run the following commands:

#### **Vale (Grammar and Style Checking)**
```sh
vale .
```
- Ensures markdown files follow the **Google Developer Documentation Style Guide**.
- Uses the **write-good** supplementary style for additional readability improvements.
- Configured via `.vale.ini` in the repository root.

#### **markdownlint-cli (Markdown Formatting Check)**
```sh
markdownlint .
```
- Checks for common markdown syntax issues.
- Configured via `.markdownlint.json` to disable line length restrictions (`MD013`).

## Guidelines for Contributors
### **1. Run Linting and Grammar Checks Before Committing**
Always run `vale .` and `markdownlint .` before committing markdown files to ensure compliance.

### **2. Fix Issues Before Pushing**
- Vale will highlight grammar and style issues; update your markdown to fix these problems.
- Markdownlint will flag syntax or formatting inconsistencies; adjust formatting accordingly.

### **3. Review Pull Requests for Compliance**
Before approving a pull request, verify that the markdown files pass all linting checks by running:
```sh
vale . && markdownlint .
```

### **4. Ignoring Specific Rules (If Necessary)**
- For Vale, specific files can be ignored by modifying `.vale.ini`.
- For markdownlint, additional rules can be disabled by editing `.markdownlint.json`.

## Conclusion
By following these guidelines, we ensure that all markdown documentation is clear, consistent, and professional. If you encounter any issues, refer to the documentation for [Vale](https://vale.sh) and [markdownlint](https://github.com/DavidAnson/markdownlint-cli) for troubleshooting.
