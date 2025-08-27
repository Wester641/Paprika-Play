# Playwright Test Project 🚀

This project uses [Playwright](https://playwright.dev/) for automated testing.  
This README is designed for new contributors to quickly get started.

---

## 📦 Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <project-folder>
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

---

## ▶️ Running Tests Locally

### Run all tests
```bash
npx playwright test
```

### Run a specific test
```bash
npx playwright test tests/example.spec.ts
```

### Run with UI Test Explorer
```bash
npx playwright test --ui
```

### Open Playwright report after test run
```bash
npx playwright show-report
```

---

## ⚙️ Configuration

Main config file: **`playwright.config.ts`**  
- Defines browsers, timeouts, retries, and more.  
- You can adjust it based on your local setup.

---

## 🧩 Project Structure

```
├── .github/workflows/playwright.yml   # GitHub Actions CI pipeline
├── playwright.config.ts               # Playwright configuration
├── tests/                             # Main test files
├── tests-examples/                    # Example tests
├── prompts/                           # Prompts and templates
└── mcp.json                           # MCP configuration
```

---

## 🔄 CI/CD

This repo includes a GitHub Actions workflow:  
**`.github/workflows/playwright.yml`**

- Runs tests automatically on each push/PR.  
- Reports are available in GitHub Actions → Jobs.

---

## 🛠️ Useful Commands

- Install Playwright browsers and drivers:
  ```bash
  npx playwright install
  ```

- Lint the project:
  ```bash
  npm run lint
  ```

---

## ❓ FAQ

**Q:** Playwright browsers are not installing.  
**A:** Try:
```bash
npx playwright install --with-deps
```

**Q:** How do I run only one test?  
**A:** Add `.only` to the test:
```ts
it.only('should work', async ({ page }) => { ... });
```

---

👨‍💻 Happy testing!
