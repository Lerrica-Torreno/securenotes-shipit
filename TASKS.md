# SecureNotes — Make It Fast & Fair, Then Ship It

**Weeks 16–17 Laboratory · Work in Pairs**

## Part A — Make It Accessible & Fast (Week 16)

Files: `app/static/index.html` and `app/static/styles.css`

- [x] **TASK 1 — Perceivable.** Added the HTML language attribute, a descriptive page title, and alternative text for both images.
- [x] **TASK 2 — Structure & Controls.** Implemented the `<main>` landmark, corrected the heading hierarchy, and replaced the clickable `<div>` with a proper `<button>`.
- [x] **TASK 3 — Labels.** Replaced the fake labels with proper `<label>` elements associated with their respective input IDs.
- [x] **TASK 4 — Contrast.** Updated the `--ink` and `--brand` colors to meet the WCAG AA minimum contrast ratio of 4.5:1.
- [x] **TASK 5 — Performance.** Deferred JavaScript loading, added image dimensions, and enabled lazy loading for the content image.

**Test Result:** 18 tests passed.

## Part B — Ship It on a Pipeline (Week 17)

File: `.github/workflows/ci.yml`

- [x] **TASK 6 — Triggers.** Configured GitHub Actions to run on pushes and pull requests targeting `main`.
- [x] **TASK 7 — The Job.** Configured an automated test job using Ubuntu, Python 3.12, dependency installation, and Pytest.

**Test Result:** 8 pipeline tests passed.

**Full Test Suite:** 38 passed.

## Part C — Push & Peer Review

- [x] Created the GitHub repository.
- [x] Pushed the original starter project to `main`.
- [x] Created the `fast-and-fair` branch.
- [x] Committed and pushed the completed laboratory changes.
- [x] Created a pull request from `fast-and-fair` to `main`.
- [x] Verified that GitHub Actions completed successfully.
- [ ] Reviewed another pair's pull request.
- [ ] Added line-specific review comments.
- [ ] Submitted an Approve or Request Changes verdict.

**Repository:** https://github.com/Lerrica-Torreno/securenotes-shipit

**Feature Branch:** https://github.com/Lerrica-Torreno/securenotes-shipit/tree/fast-and-fair

**Our Pull Request:** [Insert actual PR link]

**Peer-Reviewed Pull Request:** [To be completed]

## Reflection

**1. Which accessibility fix would a sighted mouse user never notice but a screen-reader or keyboard user depends on? Why?**

One important accessibility fix was replacing the fake form labels with proper `<label>` elements connected to their corresponding input fields. A sighted mouse user might not notice the difference because the labels look almost the same visually. However, screen-reader users depend on these labels to understand what information they need to enter. This improvement makes the login form more accessible and easier to navigate for users who rely on assistive technologies.

**2. Your pipeline runs the Week 16 checks automatically now. How does that stop a teammate from accidentally shipping an inaccessible page six weeks from now?**

The GitHub Actions pipeline automatically runs the accessibility, performance, and security tests whenever changes are submitted through the configured workflow. If a teammate accidentally removes an important accessibility feature, such as an image's alternative text or a form label, the tests can detect the issue and cause the pipeline to fail. This allows developers to identify problems before merging changes into the main branch. By consistently checking the application, the pipeline helps maintain accessibility and prevents previously resolved issues from returning.