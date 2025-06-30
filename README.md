# PyGitGuard 🛡️

![GitHub release](https://img.shields.io/github/release/Milko2409/pygitguard.svg) ![Python](https://img.shields.io/badge/python-3.6%2B-blue.svg) ![License](https://img.shields.io/badge/license-MIT-green.svg)

Welcome to **PyGitGuard**, a powerful Git security scanner designed to help developers prevent accidental commits of sensitive data. With the rise of data breaches, protecting your codebase has never been more critical. PyGitGuard scans for various types of sensitive information, ensuring your projects remain secure.

## Table of Contents

1. [Features](#features)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Configuration](#configuration)
5. [Examples](#examples)
6. [Contributing](#contributing)
7. [License](#license)
8. [Support](#support)

## Features

- **Sensitive Data Detection**: Scans for passwords, API keys, and other sensitive information.
- **Pre-commit Hook**: Integrates seamlessly with Git to prevent sensitive data from being committed.
- **Customizable Rules**: Define what constitutes sensitive data for your projects.
- **Easy Integration**: Works well with existing Python workflows.
- **Comprehensive Reporting**: Provides detailed reports on detected issues.

## Installation

To install PyGitGuard, follow these steps:

1. Ensure you have Python 3.6 or higher installed on your machine.
2. Clone the repository:

   ```bash
   git clone https://github.com/Milko2409/pygitguard.git
   cd pygitguard
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. For the latest release, download and execute the file from the [Releases section](https://github.com/Milko2409/pygitguard/releases).

## Usage

Once installed, you can use PyGitGuard in your projects. Here’s how:

1. Navigate to your project directory.
2. Run PyGitGuard:

   ```bash
   pygitguard
   ```

3. Review the output for any detected sensitive data.

You can also set up a pre-commit hook to automate the scanning process. This ensures that every commit is checked for sensitive data before it is finalized.

## Configuration

PyGitGuard allows you to customize its behavior. You can define specific patterns or keywords that you want to scan for. This is done by editing the configuration file, typically located at `.pygitguard.yml`.

### Example Configuration

```yaml
patterns:
  - "password"
  - "secret"
  - "api_key"
```

This configuration will instruct PyGitGuard to look for the specified patterns in your files.

## Examples

Here are some examples of how to use PyGitGuard effectively:

### Example 1: Basic Scan

Run the scanner in your project directory:

```bash
pygitguard
```

Output might look like:

```
Detected sensitive data in file: config.py
Pattern: password
```

### Example 2: Pre-commit Hook

To set up a pre-commit hook, add the following to your `.git/hooks/pre-commit` file:

```bash
#!/bin/sh
pygitguard
```

Make the hook executable:

```bash
chmod +x .git/hooks/pre-commit
```

Now, every time you attempt to commit, PyGitGuard will run automatically.

## Contributing

We welcome contributions to PyGitGuard! If you want to help improve the project, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or fix.
3. Make your changes.
4. Submit a pull request with a clear description of your changes.

Please ensure your code follows the existing style and includes tests where applicable.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Support

For support, please visit the [Releases section](https://github.com/Milko2409/pygitguard/releases) for the latest updates and documentation.

---

By using PyGitGuard, you take a significant step towards securing your codebase. Regularly scan your projects and integrate this tool into your development workflow to minimize the risk of exposing sensitive data.