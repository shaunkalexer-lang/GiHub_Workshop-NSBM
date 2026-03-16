# Task Manager CLI

A simple command-line task manager built with Python.  
Used as a hands-on project during the **From Code to Collaboration** Git & GitHub workshop.

---

## Workshop Activity — Fork, Build, and Submit a Pull Request

This is a **fork-based** collaboration exercise. You will not push directly to this repository.  
Instead, you will make your own copy (fork), make changes, and submit a Pull Request — exactly how real open source contribution and team collaboration works.

### Step 1 — Fork this repository

1. Click the **Fork** button in the top-right corner of this page on GitHub
2. Leave all settings as default and click **Create fork**
3. You now have your own copy at `https://github.com/YOUR-USERNAME/task-manager`

### Step 2 — Clone your fork

```bash
gh repo clone YOUR-USERNAME/task-manager
cd task-manager
```

Or with standard Git:

```bash
git clone https://github.com/YOUR-USERNAME/task-manager.git
cd task-manager
```

### Step 3 — Run the app

```bash
python main.py
```

Try a few commands to make sure everything works:

```
Enter command: add Buy groceries
Enter command: list
Enter command: done 1
Enter command: quit
```

### Step 4 — Create a feature branch

Never work directly on `main`. Create a branch named after what you are changing:

```bash
git checkout -b feature/your-name-changes
```

For example:

```bash
git checkout -b feature/nikila-welcome-message
```

### Step 5 — Make your changes

Open `main.py` in your editor and update the `WELCOME_MESSAGE` variable:

```python
# Before
WELCOME_MESSAGE = "Welcome to Task Manager CLI!"

# After — personalise it
WELCOME_MESSAGE = "Welcome to Task Manager CLI! — Built by Your Name"
```

You can also update the confirmation text in `add_task()` inside `tasks.py`.

### Step 6 — Commit your changes

```bash
git status
git add .
git commit -m "feat: personalise welcome message"
```

Use a clear, descriptive commit message. The `type: description` format is industry standard:

| Prefix   | When to use                     |
| -------- | ------------------------------- |
| `feat:`  | A new feature or visible change |
| `fix:`   | A bug fix                       |
| `docs:`  | Documentation only changes      |
| `chore:` | Maintenance, config, or tooling |

### Step 7 — Push your branch to your fork

```bash
git push origin feature/your-name-changes
```

### Step 8 — Open a Pull Request

1. Go to **your fork** on GitHub
2. Click the **Compare & pull request** button that appears at the top
3. Confirm the base repository points to the **instructor's repo** and the base branch is `main`
4. Fill in the PR title and description using the checklist provided
5. Click **Create pull request**

The automated Semgrep code scan will run immediately. Your PR must pass the scan before it can be reviewed and merged.

---

## Project Structure

```
task-manager/
├── .github/
│   ├── workflows/
│   │   └── semgrep.yml          # Code scan — runs automatically on every PR
│   ├── CODEOWNERS               # Defines who must approve PRs
│   └── pull_request_template.md # PR checklist shown when opening a PR
├── main.py                      # Entry point — run this file
├── tasks.py                     # Core task logic (add, list, done, remove)
├── storage.py                   # Saves and loads tasks from a JSON file
├── requirements.txt             # No external packages needed
└── README.md                    # This file
```

---

## Commands

| Command           | What it does        |
| ----------------- | ------------------- |
| `list`            | Show all tasks      |
| `add <task name>` | Add a new task      |
| `done <id>`       | Mark a task as done |
| `remove <id>`     | Remove a task       |
| `help`            | Show all commands   |
| `quit`            | Exit the app        |

---

## Requirements

- Python 3.7 or higher
- No external packages — uses Python standard library only

---

## Contributing

This repository uses a **fork and pull request** workflow.  
Direct pushes to `main` are disabled.  
All changes must go through a Pull Request, pass the automated code scan, and receive an approval before merging.
