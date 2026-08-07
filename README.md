# Reporting Issues — Coding Project Manager

> **Repo:** [05Narwhal/coding-project-manager](https://github.com/05Narwhal/coding-project-manager)  
> **Current version:** 26.1.21-beta
> **Platform:** Windows (Tauri v2 desktop app)

---

## Known Limitations in 26.1.20-beta

These are expected in this build — please don't open issues for them.

- **Sync is one-way.** CPM pushes to the cloud and never reads back. Changes made in the app appear on the website; changes made on the website do not come back down, and two machines running CPM do not sync with each other yet.
- **The website is read-only.** Web editing is a later project. Two-way sync lands first.
- **Licensing is switched off.** No subscription is required, nothing locks and nothing expires in this build. A licence prompt appearing anywhere *is* worth reporting.
- **Live collaboration is pre-release only.** It works in alpha and beta builds and is hidden in stable ones, pending more real-world network testing.

---

## Before You Open an Issue

1. **Search first.** Check [open issues](https://github.com/05Narwhal/coding-project-manager/issues) to see if it's already reported.
2. **Update.** Make sure you're on the latest release — the bug may already be fixed.
3. **Reproduce.** Confirm the problem happens consistently, not just once.

---

## Bug Reports

Open a **Bug report** issue and include:

### Required

| Field | What to provide |
|---|---|
| **App version** | Shown in Settings → About (e.g. `26.0.60-alpha`) |
| **OS / Windows version** | e.g. Windows 11 Pro 23H2 |
| **Steps to reproduce** | Numbered, minimal steps that trigger the bug |
| **Expected behavior** | What you expected to happen |
| **Actual behavior** | What actually happened |

### Helpful extras

- **Screenshots or screen recordings** — especially for UI glitches
- **Backend logs** — open DevTools (`Ctrl+Shift+I`) → Console tab and paste any red errors
- **Rust panic output** — if the app crashes, paste the terminal output if you launched via `npm run tauri dev`
- **Affected data** — note if the bug involves a specific project, task, or script type

### Template

```
**Version:** 26.0.60-alpha
**OS:** Windows 11 Pro 23H2

**Steps to reproduce:**
1. 
2. 
3. 

**Expected:** 

**Actual:** 

**Logs / screenshots:**
```

---

## Feature Requests

Open a **Feature request** issue and include:

- **What problem does this solve?** Describe the workflow gap.
- **Proposed solution.** How you'd expect the feature to work.
- **Alternatives considered.** Any workarounds you've tried.

Keep requests focused — one feature per issue.

---

## Issue Labels

| Label | Meaning |
|---|---|
| `bug` | Confirmed defect in existing behavior |
| `feature` | New functionality request |
| `ui` | Visual or layout issue |
| `backend` | Rust/IPC/persistence layer |
| `performance` | Slowness or high resource use |
| `crash` | App exits unexpectedly |
| `data-loss` | Issue that causes loss of projects, tasks, or settings |
| `alpha` | Known rough edge in the current alpha build |

---

## Out of Scope

These won't be accepted as issues:

- Support for macOS or Linux (Windows only for now)
- Requests to change the core dark-theme aesthetic
- Bugs in data migrated from a much older version — export and re-import instead

---

## Security Issues

**Do not open a public issue for security vulnerabilities.** Email directly: [julianaljaz.loy@gmail.com](mailto:julianaljaz.loy@gmail.com)

---

## Contributing

Pull requests are welcome for small fixes. For anything larger, open a feature request first so the approach can be agreed on before you write code.
