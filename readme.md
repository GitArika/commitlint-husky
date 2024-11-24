
# Commitlint with Husky 🚀

A robust configuration for enforcing **conventional commits** using **Husky** and **Commitlint**, ensuring consistent and descriptive commit messages for your projects.

## 🔍 Overview

This repository demonstrates how to integrate **Commitlint** with **Husky** in your project to automate the validation of commit messages. By adopting this setup, you can:

- Enforce commit message standards like [Conventional Commits](https://www.conventionalcommits.org/).
- Maintain a clean, understandable commit history.
- Improve collaboration and project traceability.

---

## ✨ Features

- **Seamless Integration:** Configures Husky to automatically run Commitlint on every commit.
- **Customizable Rules:** Easily adapt Commitlint rules to match your project's conventions.
- **Plug-and-Play:** A preconfigured example you can clone or use as a reference.

---

## 🛠️ Getting Started

Follow these steps to set up Commitlint with Husky in your project.

### 1. Clone the Repository

```bash
git clone https://github.com/GitArika/commitlint-husky.git
cd commitlint-husky
```

### 2. Install Dependencies

Run the following command to install required dependencies:

```bash
npm install
```

### 3. Commitlint and Husky Configuration

The repository includes pre-configured settings for Commitlint and Husky:

- **Commitlint Rules:** Defined in `.commitlintrc.js`. Modify the rules as needed to enforce your custom commit message conventions.
- **Husky Hooks:** Configured in `.husky/commit-msg` to automatically validate commit messages before they are committed.

### 4. Test the Setup

Try making a commit to test the validation:

```bash
git commit -m "invalid message"
```

Commitlint will reject non-conforming messages, ensuring compliance with your rules.

---

## 🔧 Configuration Details

### Commitlint Rules (`.commitlintrc.js`)

The default rules enforce [Conventional Commits](https://www.conventionalcommits.org/):

```javascript
module.exports = {
  extends: ['@commitlint/config-conventional'],
};
```

Feel free to extend or override these rules to match your team's standards.

### Husky Hook (`.husky/commit-msg`)

The hook ensures Commitlint runs on every commit:

```bash
#!/bin/sh
. "$(dirname "$0")/_/husky.sh"

npx --no-install commitlint --edit "$1"
```

---

## 🤝 Contributions

Contributions are welcome! If you'd like to enhance this repository or suggest improvements, follow these steps:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/improve-docs
   ```
3. Push your changes and create a pull request.

---

## 📧 Contact

For questions, suggestions, or collaboration opportunities, feel free to reach out:

- **Email:** [ariel.se@icloud.com](mailto:ariel.se@icloud.com)
- **GitHub:** [GitArika](https://github.com/GitArika)

---

## 📜 License

This repository is licensed under the MIT License. Use it freely in your projects.

---
