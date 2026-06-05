# Security Policy

## Scope

Silent is a static, client-side-only web application. It has no backend, no database, no user accounts, and no network communication beyond serving the HTML file itself.

## Reporting a Vulnerability

If you discover a security issue (e.g. a way the app could be misused or could harm users), please report it by opening a [GitHub Issue](../../issues) with the label `security`.

For sensitive disclosures, contact the repository owner directly via GitHub.

## What is out of scope

- Vulnerabilities in the user's browser or operating system
- Microphone permission prompts (these are controlled by the browser, not this app)
- GitHub Pages infrastructure

## Security design

| Property | Status |
|----------|--------|
| No external scripts or stylesheets loaded | ✅ |
| No user data transmitted or stored | ✅ |
| No cookies or localStorage | ✅ |
| DOM manipulation via `textContent` only (no `innerHTML`) | ✅ |
| No `eval()` or dynamic code execution | ✅ |
| Microphone access requires explicit user consent | ✅ |
| HTTPS required by browser for microphone API | ✅ |
