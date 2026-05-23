# Ticket Reservation Business Logic Bug

<p align="center">
  <img src="https://img.shields.io/badge/Bug_Report-Cybersecurity-0078D4?style=for-the-badge" alt="Bug Report">
  <img src="https://img.shields.io/badge/CTF_Lab-Realistic_Simulation-22C55E?style=for-the-badge" alt="Realistic CTF Simulation">
  <img src="https://img.shields.io/badge/Severity-High-DC2626?style=for-the-badge" alt="High">
</p>

---

## Overview

Reserve tickets without paying, advance time, and show that other buyers are still blocked.

This repository is a **sanitized educational case study**. It does not target a real company or live system. The CTF lab is a mock vulnerable app where the flag unlocks only after reproducing the simulated bug.

## Play the CTF Simulation

Run locally:

```bash
python -m http.server 8000
```

Open:

```text
http://localhost:8000/labs/ctf-game/
```

GitHub Pages:

```text
https://mialmashahreh22.github.io/ticket-reservation-business-logic-bug/labs/ctf-game/
```

## What You Must Do

Demonstrate an unpaid hold that lasts too long.

## Report

Read the full report:

```text
report/BUG-REPORT.md
```

## Repository Structure

```text
ticket-reservation-business-logic-bug/
|-- README.md
|-- report/
|   `-- BUG-REPORT.md
|-- docs/
|   `-- remediation.md
|-- labs/
|   `-- ctf-game/
|       |-- index.html
|       |-- styles.css
|       |-- app.js
|       |-- manifest.webmanifest
|       |-- service-worker.js
|       `-- assets/
|           `-- ctf-icon.svg
`-- resources/
    `-- references.md
```

## Safety

Use this project only for learning, local labs, and responsible disclosure practice. Do not test destructive actions, IDORs, token exposure, or business-logic abuse against systems you do not own or have permission to test.
