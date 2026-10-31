# SynthHumLab Ray-Ban Tracker 👓

[![Project Code Linting](https://github.com/cerodriguez46)](https://github.com/cerodriguez46/RayBanSample)

An advanced iOS application built using SwiftUI that interfaces securely with **Ray-Ban Meta Smart Glasses** utilizing the official Meta Wearables Device Access Toolkit (DAT).

---

## 🚀 Features
* **Secure Architecture:** Decoupled local credential configurations using `.xcconfig` templates to keep developer tokens off public repositories.
* **Automated Linting:** Lightweight GitHub Actions pipeline to validate code workspace integrity on every push.
* **App Store Ready:** Pre-built `docs/` architecture linked directly to a public GitHub Pages deployment for required Privacy Policies and Terms of Service.

---

## 🛠️ Local Prerequisites
To download, compile, and run this project with physical smart glasses, you must have:
* **Mac Hardware:** Running macOS Sonoma (or newer) with Xcode 15.4+ installed.
* **Apple Developer Account:** Required for native background Bluetooth & external accessory code signing.
* **Meta Wearables Developer Profile:** Registered via the [Meta Wearables Developer Center](https://meta.com).
* **Developer Mode Enabled:** Open the **Meta AI** companion app on your phone, navigate to your device settings, and tap the application version string 5 to 7 times until the Developer Options menu unlocks.

---

## 📦 Getting Started & Installation

### 1. Clone the Repository
```bash
git clone https://github.com
cd YOUR_REPOSITORY_NAME
```

### 2. Configure Your Secret Developer Tokens
Because this repository is public, your specific Meta credentials are blocked via the `.gitignore` rules. You **must** create your own local configuration card before hitting compile:

1. Open the project workspace in Xcode.
2. In the root directory, create a new configuration file named exactly: `DeveloperKeys.xcconfig`
3. Paste your custom sandbox tokens from your Meta Wearables dashboard into it:
   ```text
   META_APP_ID = YOUR_META_APP_ID_HERE
   META_CLIENT_TOKEN = YOUR_META_CLIENT_TOKEN_HERE
   ```

### 3. Open and Build the App
1. Connect your **physical iOS device** via a USB cable (The iOS Simulator does not support the low-level Bluetooth accessory pipeline required by the glasses).
2. Ensure **Developer Mode** is turned on under *Settings > Privacy & Security* on your iPhone.
3. Select your physical device target in the top toolbar of Xcode.
4. Press `⌘ + R` to compile, resolve Swift Package dependencies, and deploy live!

---

## How We Work: Contributors and Maintainers

Everyone on this project — coders and non-coders alike — follows the same
basic pipeline: **issue → branch → pull request → review → merge.** What
differs is your part in it.

### For Contributors

Your job: take one issue from "to-do" to "merged."

1. **Pick an issue** from the Issues tab. New here? Filter by
   `good first issue` — those are written for beginners. **Assign
   yourself** so nobody else starts the same work.
2. **Ask first if anything is unclear** — post your question in the issue
   itself. Asking early is the norm here, not a weakness.
3. **Get the project on your computer (once).** Clone the project repo:
   `git clone <repo address>` — or use GitHub Desktop (File → Clone
   Repository). You only clone once.
4. **Start every work session from an up-to-date `main`.** Switch to
   `main` and pull down everyone's latest merged work:
   `git switch main` then `git pull`.
5. **Branch off `main`** — never work directly on it. Name your branch by
   type, issue number, and a short name, e.g. `feature/12-photo-capture`,
   `fix/9-stream-crash`, or `docs/14-setup-guide`. (GitHub can create the
   branch for you from inside the issue.)
6. **Make your change**, small and focused on just that issue. Commit as
   you go with one-sentence messages: `git commit -m "Add photo capture"`.
   Contributions don't have to be code — reference analyses, rubric
   scores, documentation, and data entries all follow these same steps.
7. **Make sure it builds and passes locally before you push.** API work:
   run the app and `pytest`. App work: build in Xcode (⌘B) and run tests
   (⌘U). If it doesn't run on your machine, don't push it yet.
8. **Push your branch** to the project repo:
   `git push -u origin feature/12-photo-capture`. (Because you're a member
   of the project organization, you push branches to the project's own
   repo — no fork or personal copy needed.)
9. **Open the pull request.** Pushing and the PR are two separate steps:
   the push uploads your branch; the PR asks for it to be merged. After
   pushing, click GitHub's "Compare & pull request" button, fill in the
   template, and write `Closes #<issue number>` so the issue closes
   automatically when you're merged. Not finished yet? Open a **draft PR**
   — that's encouraged.
10. **Respond to the review.** A reviewer may approve, comment, or request
    changes. Requested changes are normal, not a rejection: push fixes to
    the same branch and the PR updates itself. Ask in the PR if a comment
    is unclear.
11. **You're done when the maintainer merges.** Your name stays in the
    project's history. Delete your branch afterward, and next session
    start again at step 4.

Stuck at any point? Post in your issue what you tried and what happened —
a screenshot helps. "I'm stuck" is a valid update.

### For Maintainers

Your job: keep the machine running — issues flowing, people unblocked,
`main` healthy.

1. **Write and curate issues.** The backlog is your main tool. Every real
   task exists as an issue that says *what* to do, *why*, and how we'll
   know it's done ("Done when…"). Keep a healthy pool of
   `good first issue` tasks for beginners and no-code contributors.
2. **Triage promptly.** Give new issues and pull requests a first look
   within a few days: add labels, assign or invite someone to claim them,
   and answer the first questions. Silence is what kills contributions.
3. **Route reviews.** Review pull requests yourself, or route them — code
   PRs to a technical reviewer, documentation and evaluation-data PRs to
   a content reviewer. Every PR needs one approving review from someone
   other than its author.
4. **Check before merging.** The PR does what its issue asked, the
   automatic checks (CI) are green, no secrets are committed, and nothing
   out of scope snuck in. Squash-merge, and confirm the linked issue
   closed.
5. **Unstick people.** A contributor who goes quiet for a week usually
   needs help, not pressure. Check in on their issue and offer a hand or
   a smaller slice of the task.
6. **Housekeeping.** Keep branch protection on `main` (pull request +
   passing checks + one approval required for every merge). Manage
   organization permissions as people join. Post the short weekly status
   update — what shipped, what's next, what's blocked — in the pinned
   status issue.
7. **Releases.** Tag releases from `main` with a changelog entry, so the
   project's progress is visible to anyone — including future funders —
   without reading the code.

---
## Product Roadmap
Set main branch to only be modified with pull requests
Update license agreement
Update privacy policy
Expand pipeline 
Break down Git and Github for newcomers in sub guides for contributing 
Create structs for each of the sensors to access
Fill out index doc page for basics of accessing the sensors and lifecyle of meta ray bans
Update app logo
Add description of base files as they are laid out for MVVM architecture


## 🔒 Data & Privacy Policy
This application processes all camera, microphone, and sensor telemetry data stream assets **locally and in real-time** on the host iOS device. No hardware telemetry or media streams are stored, shared, or transmitted to external third-party cloud architectures. 

For full legal terms, view our public live tracking configurations:
* [Live Privacy Policy](https://YOUR_GITHUB_USERNAME.github.io/YOUR_REPOSITORY_NAME/privacy)
* [Live Terms of Use](https://YOUR_GITHUB_USERNAME.github.io/YOUR_REPOSITORY_NAME/terms)

## 📄 License
This repository is licensed under the terms of the [MIT License](LICENSE).

