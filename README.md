---

# Python Automation with GitHub Actions

This project demonstrates the use of GitHub Actions to automate the execution of a Python script at regular intervals. The script appends random values along with the current date and time (when the code was executed) to a text file named `useless_info.txt`, and commits the changes to the repository.

---

## Table of Contents
1. [Overview](#overview)
2. [Features](#features)
3. [Getting Started](#getting-started)
4. [Workflow Details](#workflow-details)
5. [Contributing](#contributing)
7. [License](#license)

---

## Overview

This repository contains a GitHub Actions workflow that automates the execution of a Python script whenever possible. Scheduled workflows can run as frequently as every 5 minutes, but actual execution timing may vary depending on GitHub's servers.

### Script Functions:
- Checks if a file named `useless_info.txt` exists; if it doesn’t, the script creates it.
- Appends a random value to the file.
- Appends the current date and time to the file.
- Commits the changes to the repository using GitHub Actions.

**Note**: If using a **self-hosted GitHub Actions runner**, you will need to install dependencies manually on the runner (see [Self-Hosted Runner Setup](#self-hosted-runner-setup)).

---

## Features

- **Automated Execution**: Runs the Python script at regular intervals using GitHub Actions.
- **Data Logging**: Logs random values along with timestamps to a text file, showcasing file handling and automation.
- **Continuous Integration**: Automatically commits and pushes changes, demonstrating CI capabilities with GitHub Actions.

---

## Getting Started

### Installation

1. **Fork the Repository**  
   Click the 'Fork' button at the top right corner of this repository to create a copy under your GitHub account.

2. **Clone the Repository**  
   Clone the forked repository to your local machine:
   ```bash
   git clone https://github.com/your-username/PythonAutomation2.git
   ```

3. **Navigate to the Project Directory**  
   ```bash
   cd PythonAutomation2
   ```

4. **Install Dependencies**  
   - **For GitHub's Hosted Actions**: Dependencies are automatically installed as part of the workflow, so you don't need to install them locally.
   - **For Self-Hosted GitHub Actions Runners**: You will need to manually install the required Python packages on your self-hosted runner:
   ```bash
   pip install -r requirements.txt
   ```
   **Note**: The `requests` package in `requirements.txt` is **not used** in the actual code but is included for demonstration purposes. You can remove it from `requirements.txt` if it is not needed for your setup.

---

## Workflow Details

The GitHub Actions workflow is defined in `.github/workflows/main.yml` and is scheduled to run whenever possible. Scheduled workflows can run as frequently as every 5 minutes, but actual execution timing may vary depending on GitHub's servers. The workflow executes the following steps:

1. **Set Up Python Environment**  
   Initializes a Python environment with the specified version.

2. **Install Dependencies**  
   Installs the Python packages listed in `requirements.txt`.

3. **Run Python Script**  
   Executes `main.py` to check for or create the text file, append data, and log timestamps.

4. **Commit and Push Changes**  
   Commits any changes made to `useless_info.txt` and pushes them to the repository.

For more details, refer to the `main.yml` file in the `.github/workflows` directory.

---

## Contributing

Contributions are welcome! To contribute, please follow these steps:

1. **Fork the Repository**  
   Create a fork of this repository.

2. **Create a Feature Branch**  
   Create a new branch for your feature or bug fix:
   ```bash
   git checkout -b feature-name
   ```

3. **Commit Your Changes**  
   Make your changes and commit them with clear, descriptive messages:
   ```bash
   git commit -m "Description of your changes"
   ```

4. **Push to Your Branch**  
   Push your changes to your forked repository:
   ```bash
   git push origin feature-name
   ```

5. **Create a Pull Request**  
   Open a pull request to this repository, detailing the changes you made.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
