# Reporting Issues — Coding Project Manager

> **Repo:** [05Narwhal/coding-project-manager](https://github.com/05Narwhal/coding-project-manager)  
> **Current version:** 26.1.31-beta (beta channel; last stable: 26.1.23-stable)
> **Platform:** Windows (Tauri v2 desktop app)

---

## Known Limitations in 26.1.30-beta

These are expected in this build — please don't open issues for them.

- **Source control needs GitHub connected first.** Everything under Properties → Source control (Changes, diffs, History, Worktrees, branches, merges, pull requests, releases, session snapshots) is available in every build, but until you connect GitHub in Settings → GitHub (CPM shows a code you enter on github.com) the branch, pull-request and release features stay unavailable.
- **Note attachments don't sync through the cloud yet.** Images and files in notes are stored on the PC that added them (25 MB per file). Syncing them needs Cloud Storage to be switched on for CPM's cloud project, which is done separately; until then a note opened on another device shows a "Not on this device" placeholder. Deleting a note does not delete its stored files.
- **Discord status only exists in builds that carry a Discord application ID.** If Settings → Editor & Projects has no "Discord status" section, this build doesn't have one. When present it is off by default.
- **Grammar suggestions are English-oriented and will sometimes flag correct text.** Use *Ignore once* / *Ignore rule*, or turn them off under Settings → Editor & Projects → Notes.
- **Sync is two-way for notes and tasks only.** Notes and tasks you change on the website come back down to the app, and a note or task deleted on either side is deleted on the other. Project statistics and your Home layout only ever go up. Signing in on a new machine pulls your notes and tasks, but not your tracked time, scripts, settings or project links — the backup manager is the way to move those.
- **The website edits notes and tasks; projects are read-only there.** Projects, time and statistics are shown but cannot be edited on the web.
- **Licensing is switched off.** No subscription is required, nothing locks and nothing expires in this build. A licence prompt appearing anywhere *is* worth reporting.
- **Live collaboration is in every build, but has had less real-world network testing than the rest of the app.** Everyone in a session must be on the same CPM version (a join from any other build is refused, with both version numbers in the message), and hosting may need a firewall rule — the session panel says whether the port is blocked and has a button to allow it (Windows will ask for administrator permission).
- **Blank window when creating a Cargo project could not be reproduced** on a current build. If you still see it on 26.1.30-beta, please open an issue with the exact steps and the log from the app data folder's `logs/`.

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
| **App version** | Shown in Settings → About (e.g. `26.1.30-beta`) |
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
**Version:** 26.1.30-beta
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
