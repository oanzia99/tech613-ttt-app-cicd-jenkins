# tech613-ttt-app-cicd-jenkins

> **Course:** Sparta Global – Tech613 DevOps  
> **Author:** Oan Zia  
> **Repository:** [oanzia99/tech613-ttt-app-cicd-jenkins](https://github.com/oanzia99/tech613-ttt-app-cicd-jenkins)  
> **Application:** Sparta Tic Tac Toe Node.js Application (Version 1.2.0)  
> **Purpose:** Automated Continuous Integration & Continuous Delivery (CI/CD) Pipeline with Jenkins  

---

## Purpose of this Repository

This repository hosts the **Sparta Tic Tac Toe Node.js application (Version 1.2.0)** configured to power an automated **Continuous Integration & Continuous Delivery (CI/CD)** pipeline using **Jenkins**, GitHub Webhooks, and automated quality testing gates.

When code changes are pushed to the development branch (`dev`), Jenkins automatically executes test suites (`node --test`), validates code integrity, and merges approved changes into the `main` deployment branch.

---

## Application Details (Version 1.2.0)

The uncompressed application source code resides directly in the root [`app/`](./app/) directory:

* **Name:** `sparta-app-v2`
* **Version:** `1.2.0`
* **Runtime:** Node.js (v20+ LTS)
* **Testing Framework:** Node.js native test runner (`node --test`)
* **Key Features in v1.2:**
  * Interactive Tic Tac Toe web game with client/server stateful modes
  * MongoDB integration for persistent scoreboards and game history
  * Prometheus observability metrics endpoint (`GET /metrics`)
  * Structured JSON observability logging (`pino`) with correlation IDs
  * Automatic fallback handling for database disconnections

---

## Developer Workflow & Testing

```bash
# 1. Switch to the dev branch
git checkout dev

# 2. Navigate to the app directory and install dependencies
cd app
npm install

# 3. Run automated tests locally
npm test

# 4. Start the application locally
npm start
```

---

## Repository Structure

```text
tech613-ttt-app-cicd-jenkins/
├── .gitignore               # Ignores node_modules, logs, and environment files
├── README.md                # Purpose of repository and usage guide (this file)
└── app/                     # Uncompressed Sparta Tic Tac Toe Node.js application (v1.2.0)
    ├── package.json         # Package metadata, dependencies, and test scripts (v1.2.0)
    ├── package-lock.json    # Exact dependency tree lockfile
    ├── index.js             # Application entry point
    ├── server.js            # Express server implementation & routes
    ├── app.js               # Game client-side logic & UI handlers
    ├── logger.js            # Pino structured JSON logger
    ├── metrics.js           # Prometheus metrics instrumentation
    ├── styles.css           # UI styling
    ├── public/              # Static frontend assets
    ├── seeds/               # Database seed scripts
    └── test/                # Automated unit and integration test suites
```

---

*Maintained by **Oan Zia** | Sparta Global Tech613 DevOps*
