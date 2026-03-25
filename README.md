# Introduction to Git, GitHub, Jest, GitHub Classroom, and GitHub Codespaces

## What is Git?

Git is a version control system that tracks changes in code and files. It allows multiple developers to collaborate on a project efficiently and helps manage code history, branches, and merges.

### Key Features of Git
- **Version Control**: Tracks changes in files, allowing you to revert to previous versions if needed. Provides a clear history of who made changes, what changes were made, and when.
- **Branching and Merging**: Branches allow you to work on new features or bug fixes without affecting the main codebase. Merging integrates changes from different branches, enabling collaborative development.
- **Commit and Push**: A commit saves your changes locally with a message describing what was done. Push sends your commits to a remote repository, like GitHub, for others to access.

## What is GitHub?

GitHub is a web-based platform that hosts Git repositories. It provides tools for version control, collaboration, and project management, allowing developers to share code, contribute to open-source projects, and work together on private or public repositories.

### Core Features of GitHub
- **Repositories**: Central location for all your project files and history.
- **Pull Requests**: A way to propose changes to a project; allows for code review and discussion before merging.
- **Issues and Project Boards**: Tools for tracking bugs, feature requests, and project tasks.

## What is GitHub Codespaces?

GitHub Codespaces is a cloud-based development environment that runs directly in your browser. It gives you a full VS Code editor with all the tools you need — no local installation required.

### Why Use Codespaces?
- **No setup required**: Everything is pre-configured — Node.js, npm, extensions, and dependencies are ready to go.
- **Works anywhere**: All you need is a web browser. Works on Chromebooks, school computers, tablets, etc.
- **Consistent environment**: Every student gets the exact same setup, eliminating "it works on my machine" issues.
- **Fast start**: Click a button and you're coding in under a minute.

### How to Open a Codespace
1. Go to the assignment repository on GitHub
2. Click the green **"Code"** button at the top
3. Select the **"Codespaces"** tab
4. Click **"Create codespace on main"**
5. Wait for the environment to load (this may take a few minutes the first time)

## What is JavaScript?

JavaScript is the programming language of the web. It runs directly in the browser and is used to make web pages interactive — handling button clicks, updating content, validating forms, and much more.

### Key Concepts for These Assignments
- **Variables**: Use `let` for values that change and `const` for values that don't.
- **Functions**: Reusable blocks of code that perform a specific task.
- **DOM Manipulation**: Use `document.getElementById()` or `document.querySelector()` to read and change elements on the page.
- **Event Listeners**: Use `addEventListener()` to respond to user actions like clicks and form submissions.
- **prompt() and alert()**: Built-in browser functions for simple input and output.

## What is Jest?

Jest is a popular testing framework for JavaScript. It is used in these assignments to automatically check that your code works correctly.

### Key Features of Jest
- **Test Functions**:
  - `test('description', () => { ... })`: Defines a single test case.
  - `describe('group', () => { ... })`: Groups related tests together.
- **Assertions**:
  - `expect(value).toBe(expected)`: Checks if two values are exactly equal.
  - `expect(value).toContain(item)`: Checks if an array or string contains something.
  - `expect(fn).toThrow()`: Checks if a function throws an error.
- **DOM Testing**: Jest can use `jsdom` to simulate a browser environment, letting tests interact with your HTML and JavaScript just like a real browser would.

## What is GitHub Classroom?

GitHub Classroom is a tool designed to help educators manage coding assignments using GitHub.

### How It Works
1. Your instructor posts an assignment link in Google Classroom
2. Click the link to accept the assignment
3. GitHub Classroom creates a **personal copy** of the repository just for you
4. You write your code and push (save) it to GitHub
5. **Autograding** runs automatically when you push — tests check your code and assign points
6. Check the **Actions** tab on GitHub to see your score

### Checking Your Score
1. Go to your assignment repository on GitHub
2. Click the **Actions** tab at the top
3. Click on the most recent workflow run
4. Each test shows as a separate step with its point value
5. Green checkmarks = passing, red X = failing

## Project Structure

Every JavaScript assignment follows this structure:

```
assignment-repo/
├── index.html          ← Your HTML file (structure and elements)
├── script.js           ← Your JavaScript file (logic and behavior)
├── style.css           ← Optional CSS file (styling)
├── .devcontainer/      ← Codespaces configuration (don't modify)
│   └── devcontainer.json
├── .github/
│   └── workflows/
│       └── classroom.yml  ← Autograding workflow (don't modify)
└── README.md           ← Assignment instructions
```

### Files You Edit
- **`script.js`** — This is where you write your JavaScript code. Most of your work goes here.
- **`index.html`** — Some assignments provide starter HTML; others ask you to build it. Read the README to know what's expected.

### Files You Should NOT Edit
- **`.github/workflows/classroom.yml`** — This runs the autograding tests. Modifying it may break your score.
- **`.devcontainer/devcontainer.json`** — This configures your Codespaces environment.

## Running Your Code

### In Codespaces / VS Code
1. Open `index.html` in the editor
2. Right-click the file and select **"Open with Live Server"** (if the Live Server extension is installed), or:
3. Open the terminal (`Ctrl+`` `) and run:
   ```bash
   npx live-server
   ```
4. A browser preview will open showing your page
5. Edit `script.js`, save, and the page refreshes automatically

### Opening the Browser Console
The browser console shows `console.log()` output and error messages:
- **Chrome/Edge**: Press `F12` or `Ctrl+Shift+J` (Windows) / `Cmd+Option+J` (Mac)
- **In Codespaces**: Use the Simple Browser preview, then open DevTools in your actual browser tab

## GitHub Desktop (Alternative to Codespaces)

If you prefer to work locally instead of using Codespaces:

1. Download and install [GitHub Desktop](https://desktop.github.com/)
2. Open GitHub Desktop and sign in with your GitHub account
3. Click **File** > **Clone Repository**
4. Select the **URL** tab and paste your assignment repository URL
5. Choose a local path and click **Clone**
6. Open the project in VS Code

### Local Requirements
- A modern web browser (Chrome, Edge, or Firefox)
- VS Code with the Live Server extension
- Node.js 18+ ([Download](https://nodejs.org/)) — only needed if you want to run tests locally

## Benefits of These Tools in Computer Science Classes

- **Industry-standard tools**: Git, GitHub, and JavaScript are used by professional software developers worldwide.
- **Collaboration skills**: Learn how to manage code contributions from multiple people.
- **Automated testing**: Get instant feedback on your code through autograded tests.
- **Cloud development**: Codespaces lets you code from anywhere without installing anything.
- **Real-world skills**: JavaScript is the most widely used programming language on the web.

## Next Steps

Navigate to the [Workflow Repo](https://github.com/cs-plus-plus/JS-Workflow) for a step-by-step guide on accepting assignments, writing code, and submitting your work.
