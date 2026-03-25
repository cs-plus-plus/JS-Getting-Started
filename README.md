# CS++ JavaScript — Getting Started

> **Welcome to CS++!** This guide covers everything you need to know before starting your first JavaScript assignment. Read through it once, try the practice examples, and you'll be ready to go.

---

## Table of Contents

1. [What is Git?](#what-is-git)
2. [What is GitHub?](#what-is-github)
3. [What is GitHub Codespaces?](#what-is-github-codespaces)
4. [What is GitHub Classroom?](#what-is-github-classroom)
5. [JavaScript Fundamentals](#javascript-fundamentals)
6. [What is Jest?](#what-is-jest)
7. [Project Structure](#project-structure)
8. [Try It Yourself — Practice Examples](#try-it-yourself--practice-examples)
9. [Tips for Success](#tips-for-success)
10. [FAQ](#faq)
11. [Next Steps](#next-steps)

---

## What is Git?

Git is a **version control system** — it tracks every change you make to your code, so you can always go back to a previous version if something breaks. Think of it like an "undo history" for your entire project.

### Key Concepts

| Term | What It Does |
|------|-------------|
| **Repository (repo)** | A folder that Git is tracking. All your project files live here. |
| **Commit** | A snapshot of your code at a specific moment. Always include a short message describing what you changed. |
| **Push** | Sends your commits from your computer (or Codespace) to GitHub so others can see them. |
| **Clone** | Downloads a copy of a repository from GitHub to your computer. |
| **Branch** | A separate version of your code. We'll mostly use the default `main` branch. |

> 💡 **Tip:** Think of commits like saving a video game — you can always load an earlier save if you mess up.

---

## What is GitHub?

GitHub is a website that stores your Git repositories online. It's where you'll find your assignments, push your code, and see your autograded scores.

### What You'll Use GitHub For
- **Viewing assignment repositories** — each assignment is its own repo
- **Checking your score** — the Actions tab shows your autograded results
- **Pushing your code** — your commits go from Codespaces to GitHub

---

## What is GitHub Codespaces?

GitHub Codespaces is a **cloud-based code editor** that runs directly in your web browser. It's like VS Code, but you don't need to install anything — it just works.

### Why Codespaces?
- ✅ **No installation required** — works on Chromebooks, school computers, tablets, anything with a browser
- ✅ **Pre-configured** — Node.js, extensions, and everything you need is already set up
- ✅ **Same for everyone** — no more "it works on my machine" problems
- ✅ **Start in seconds** — click a button and you're coding

### How to Open a Codespace
1. Go to your assignment repository on GitHub
2. Click the green **"Code"** button
3. Select the **"Codespaces"** tab
4. Click **"Create codespace on main"**
5. Wait for it to load (first time may take 1–2 minutes)

> 💡 **Tip:** Your Codespace saves automatically. You can close the browser tab and come back later — your code will still be there.

---

## What is GitHub Classroom?

GitHub Classroom is the tool your teacher uses to hand out coding assignments. When you accept an assignment, it creates a **personal copy** of the repository just for you.

### How It Works
1. Your teacher shares an **assignment link** (usually in Google Classroom)
2. Click the link and click **"Accept this assignment"**
3. GitHub Classroom creates your personal copy of the repo
4. Open it in Codespaces, write your code, and push
5. **Autograding runs automatically** — tests check your code and assign points
6. Check the **Actions** tab to see your score

### Checking Your Score
1. Go to your repository on GitHub
2. Click the **Actions** tab at the top
3. Click the most recent workflow run
4. Each test shows as a step — ✅ green = passed, ❌ red = failed
5. Your total score is the sum of all passing tests

> 💡 **Tip:** You can push as many times as you want! Each push triggers autograding, so keep improving until all tests pass.

---

## JavaScript Fundamentals

Here's a quick reference for the JavaScript concepts you'll use in these assignments. Don't worry about memorizing everything — come back to this section whenever you need a refresher.

### Variables

Use `let` for values that change, and `const` for values that don't:

```javascript
let score = 0;          // can change later
score = score + 10;     // now score is 10

const maxScore = 100;   // cannot be changed
// maxScore = 200;      // ❌ Error! const can't be reassigned
```

> ⚠️ **Avoid `var`** — it's older JavaScript and behaves differently. Always use `let` or `const`.

### Data Types

| Type | Example | Description |
|------|---------|-------------|
| **Number** | `42`, `3.14` | Any number (integer or decimal) |
| **String** | `"hello"`, `'world'` | Text wrapped in quotes |
| **Boolean** | `true`, `false` | Yes/no values |
| **null** | `null` | Intentionally empty |
| **undefined** | `undefined` | Variable declared but not assigned |

### Operators

```javascript
// Arithmetic
let sum = 5 + 3;       // 8
let diff = 9 - 2;      // 7
let product = 4 * 2;   // 8
let quotient = 9 / 3;  // 3
let remainder = 10 % 3; // 1
let power = 2 ** 3;    // 8

// Comparison (use === not ==)
5 === 5     // true
5 === "5"   // false (different types)
5 !== 3     // true
10 > 5      // true
3 <= 3      // true
```

> ⚠️ **Always use `===` (strict equality)**, not `==`. The triple equals checks both value AND type.

### Strings

```javascript
let name = "Alice";
let greeting = "Hello, " + name + "!";    // "Hello, Alice!"
let length = name.length;                  // 5
let upper = name.toUpperCase();            // "ALICE"
let lower = name.toLowerCase();            // "alice"

// Template literals (backticks) — easier for combining strings and variables
let msg = `Hello, ${name}! Your name has ${name.length} letters.`;
```

### Conditionals (if / else if / else)

```javascript
let age = 16;

if (age < 13) {
    console.log("Child");
} else if (age < 18) {
    console.log("Teen");     // This runs because 16 < 18
} else {
    console.log("Adult");
}
```

### Functions

Functions are reusable blocks of code:

```javascript
// Defining a function
function greet(name) {
    return "Hello, " + name + "!";
}

// Calling a function
let message = greet("Alice");  // "Hello, Alice!"
console.log(message);
```

### prompt() and alert()

Some assignments use `prompt()` for input and `alert()` for output:

```javascript
// Ask the user for input
let name = prompt("What is your name?");

// Show a message
alert("Hello, " + name + "!");
```

> 💡 **Tip:** The autograder mocks `prompt()` and `alert()` to test your code automatically. Write your code using these functions normally — the tests handle the rest.

### DOM Manipulation

The DOM (Document Object Model) lets your JavaScript interact with HTML elements:

```javascript
// Get an element by its ID
let heading = document.getElementById("myHeading");

// Change the text inside an element
heading.textContent = "New Title";

// Change the HTML inside an element
heading.innerHTML = "<em>Italic Title</em>";

// Read a value from an input field
let input = document.getElementById("myInput");
let value = input.value;
```

### Event Listeners

Make things happen when users interact with your page:

```javascript
// Get the button element
let btn = document.getElementById("myBtn");

// Run a function when the button is clicked
btn.addEventListener("click", function() {
    alert("Button was clicked!");
});
```

> ⚠️ **Important:** Many assignments require `addEventListener` — do NOT use `onclick` attributes in HTML. The tests check for this.

### console.log()

Your best friend for debugging:

```javascript
let x = 42;
console.log("The value of x is:", x);    // prints to the browser console
console.log(typeof x);                    // "number"
```

To see console output: press **F12** (or **Ctrl+Shift+J**) to open the browser's Developer Tools.

### Arrays

```javascript
let colors = ["red", "green", "blue"];
console.log(colors[0]);        // "red" (first element)
console.log(colors.length);    // 3

colors.push("yellow");         // add to the end
console.log(colors);           // ["red", "green", "blue", "yellow"]

// Loop through an array
for (let i = 0; i < colors.length; i++) {
    console.log(colors[i]);
}
```

### Loops

```javascript
// For loop — use when you know how many times to loop
for (let i = 1; i <= 5; i++) {
    console.log("Count: " + i);
}

// While loop — use when you don't know how many times
let guess = 0;
while (guess !== 7) {
    guess = Math.floor(Math.random() * 10) + 1;
}
console.log("Found 7!");
```

### Useful Math Functions

```javascript
Math.PI              // 3.14159...
Math.floor(4.7)      // 4 (rounds down)
Math.ceil(4.2)       // 5 (rounds up)
Math.round(4.5)      // 5 (rounds to nearest)
Math.random()        // random decimal between 0 and 1
Math.sqrt(16)        // 4

// Random integer between 1 and max
let max = 10;
let random = Math.floor(Math.random() * max) + 1;

// Format a number to 2 decimal places
let pi = Math.PI;
let formatted = pi.toFixed(2);  // "3.14" (returns a string!)
```

### parseInt() and parseFloat()

Convert strings to numbers:

```javascript
let str = "42";
let num = parseInt(str);       // 42 (integer)

let decimal = "3.14";
let float = parseFloat(decimal); // 3.14

// Check if a value is not a number
isNaN("hello")   // true
isNaN("42")      // false
isNaN(42)        // false
```

---

## What is Jest?

Jest is the **testing framework** used to automatically check your code. When you push to GitHub, Jest runs your code and checks if it produces the correct output.

### How Tests Work
- Each assignment has tests defined in the GitHub Actions workflow (`.github/workflows/classroom.yml`)
- Tests simulate user input (mocking `prompt()`) and check output (`alert()`, `textContent`, etc.)
- Each test is worth a specific number of points
- You don't need to write tests — just write code that makes them pass

### What Autograding Looks Like

When you push your code, GitHub runs the tests automatically. In the Actions tab, you'll see something like:

```
✅ Required elements exist             10/10
✅ myFunc() persistent counter          15/15
❌ getRandomNum() range or 0             0/15
✅ myAdder() correct sum                15/15
                                Total: 40/55
```

---

## Project Structure

Every JavaScript assignment follows this layout:

```
your-assignment/
├── index.html              ← Your HTML file (structure and elements)
├── script.js               ← Your JavaScript file (this is where most of your code goes)
├── style.css               ← Optional CSS (styling — not always needed)
├── .devcontainer/           ← Codespaces config (DO NOT MODIFY)
│   └── devcontainer.json
├── .github/
│   └── workflows/
│       └── classroom.yml   ← Autograding tests (DO NOT MODIFY)
└── README.md               ← Assignment instructions (READ THIS FIRST)
```

### ✅ Files You Edit
- **`script.js`** — This is where you write your JavaScript. Most of your work goes here.
- **`index.html`** — Some assignments have starter HTML; others ask you to add elements.

### ❌ Files You Should NOT Edit
- **`.github/workflows/classroom.yml`** — Modifying this will break autograding.
- **`.devcontainer/devcontainer.json`** — This configures your Codespaces environment.

---

## Try It Yourself — Practice Examples

Want to experiment without breaking your assignment? Create a **practice file** in your Codespace:

### Step 1: Create a practice file

In your Codespace, right-click in the file explorer and select **"New File"**. Name it `practice.js`.

### Step 2: Try these examples

Copy and paste any of these into `practice.js` and run them in the terminal with `node practice.js`:

**Example 1 — Variables and math:**
```javascript
// practice.js — Variables and Math
let fahrenheit = 212;
let celsius = (fahrenheit - 32) * 5 / 9;
console.log("Temperature in Celsius: " + celsius.toFixed(2));

let radius = 5;
let area = Math.PI * radius * radius;
console.log("Area of the circle: " + area.toFixed(2));
```

**Example 2 — Conditionals:**
```javascript
// practice.js — If/Else
let age = 16;

if (age <= 12) {
    console.log("Child: $7");
} else if (age <= 17) {
    console.log("Teen: $12");
} else if (age <= 64) {
    console.log("Adult: $20");
} else {
    console.log("Senior: $12");
}
```

**Example 3 — Loops and arrays:**
```javascript
// practice.js — Loops and Arrays
let numbers = [];
for (let i = 1; i <= 10; i++) {
    numbers.push(i);
}
console.log("Numbers:", numbers);

let sum = 0;
for (let i = 0; i < numbers.length; i++) {
    sum += numbers[i];
}
console.log("Sum:", sum);
console.log("Average:", (sum / numbers.length).toFixed(2));
```

**Example 4 — Functions:**
```javascript
// practice.js — Functions
function add(a, b) {
    return a + b;
}

function distance(x1, y1, x2, y2) {
    return Math.sqrt((x2 - x1) ** 2 + (y2 - y1) ** 2);
}

console.log("3 + 5 =", add(3, 5));
console.log("Distance:", distance(0, 0, 3, 4).toFixed(2));
```

### Step 3: Run your practice file

Open the terminal in Codespaces (`Ctrl+`` `) and type:

```bash
node practice.js
```

> 💡 **Tip:** The `practice.js` file won't affect your assignment tests — only `script.js` and `index.html` are graded. Practice files are a safe sandbox for experimenting.

---

## Tips for Success

1. **Read the README first** — Every assignment has a README with detailed instructions. Read it before you start coding.
2. **Check element IDs** — The autograder looks for specific IDs (like `#myDate`, `#feedback`). Typos will cause tests to fail.
3. **Use `console.log()` to debug** — Print variables to the console to see what's happening. Press F12 to open Developer Tools.
4. **Save before pushing** — Make sure you save your files (`Cmd+S` / `Ctrl+S`) before committing.
5. **Push often** — Don't wait until you're "done." Push after each feature so you can see your progress.
6. **Read the test names** — The Actions tab shows what each test checks. Use the test names as a checklist.
7. **Start with what you know** — Get the easy tests passing first, then tackle the harder ones.
8. **Use `practice.js` to experiment** — Don't be afraid to try things in a separate file first.

---

## FAQ

**Q: Do I need to install anything on my computer?**
No! Everything runs in GitHub Codespaces, which works in your web browser. No downloads or installations needed.

**Q: Can I use my own computer/IDE instead of Codespaces?**
Yes. You'll need a web browser, a text editor (VS Code is recommended), and Node.js 18+. See the [Workflow Guide](https://github.com/cs-plus-plus/JS-Workflow) for details on using GitHub Desktop.

**Q: I pushed my code but don't see a score. What happened?**
Go to the **Actions** tab in your GitHub repository. If the workflow is still running, wait a minute. If it failed, click on it to see the error details.

**Q: Can I push more than once?**
Yes! Push as many times as you want. Each push triggers autograding. Your most recent push is always the one that counts.

**Q: What if I break something?**
Git tracks every change. You can always go back to a previous version. If you're stuck, ask your teacher or contact kevin@csplusplus.com.

**Q: Why is my test failing even though my code looks right?**
Common reasons:
- **Typo in an element ID** — the test looks for exact IDs like `#myDate`, not `#mydate` or `#my-date`
- **Wrong text format** — if the test expects `"Temperature in Celsius: 100.00"`, even a missing space will fail
- **Using `==` instead of `===`** — always use strict equality
- **Forgetting `.toFixed(2)`** — some tests expect exactly 2 decimal places

**Q: What's the difference between `textContent` and `innerHTML`?**
- `textContent` sets plain text only (safer, preferred in most assignments)
- `innerHTML` can include HTML tags like `<strong>` or `<em>`

**Q: Can I use AI tools to help me?**
Check with your teacher. These assignments are designed to help you learn — the more you write yourself, the more you'll understand.

---

## Next Steps

You're ready to start coding! Head to the **[Assignment Workflow Guide](https://github.com/cs-plus-plus/JS-Workflow)** for step-by-step instructions on accepting assignments, writing code, committing, and checking your score.

📋 **View all assignments and scoring breakdowns at [csplusplus.com/js-tests](https://csplusplus.com/js-tests)**

---

*CS++ — AP Computer Science Principles — [csplusplus.com](https://csplusplus.com) — kevin@csplusplus.com*
