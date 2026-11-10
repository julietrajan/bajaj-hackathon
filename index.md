---
layout: default
title: Smart EMI Agent Hackathon
description: Bajaj Finserv × GitHub Copilot Hackathon — build, collaborate and ship with GitHub and GitHub Copilot
---

# 🏦 Smart EMI Agent Hackathon

**Bajaj Finserv × GitHub Copilot** · 2-day team hackathon

> Build a working app from scratch with **GitHub Copilot**, run it the way real engineering teams do on **GitHub**, and ship **v1.0** in two days.

| | |
|---|---|
| 📅 **Dates** | Day 1: Tue, 15 Dec 2026 · Day 2: Wed, 16 Dec 2026 |
| 🕘 **Office hours** | Wed, 9 Dec 2026 · Mon, 14 Dec 2026 |
| 👥 **Teams** | 3–5 members |
| 📦 **Submission** | Your team's private GitHub repository |
| 🏆 **Leaderboard** | [Jump to leaderboard](#-leaderboard) |

---

## 📌 Contents

1. [The problem](#-the-problem)
2. [What you will build](#-what-you-will-build)
3. [Ground rules](#-ground-rules)
4. [Before you start](#-before-you-start)
5. [The 8 challenges](#-the-8-challenges)
6. [Scoring](#-scoring)
7. [Judging criteria](#-judging-criteria)
8. [Leaderboard](#-leaderboard)
9. [Submission checklist](#-submission-checklist)
10. [Help and resources](#-help-and-resources)

---

## 🧩 The problem

Many customers hold more than one loan at a time: a personal loan, a consumer durable EMI and a two-wheeler loan. The questions they ask most are simple:

- *"What do I owe this month?"*
- *"What happens if I prepay ₹50,000?"*
- *"When is my next due date?"*

Today, answering these questions often means a call to customer service or a branch visit.

**Your challenge:** build a **Smart EMI Agent** that lets a customer answer these questions in seconds.

---

## 🛠️ What you will build

A small web app where a customer can:

| # | Feature | What it does |
|---|---|---|
| 1 | **Loan dashboard** | Shows every loan with EMI, outstanding balance and next due date |
| 2 | **What-if simulator** | Prepay a lump sum or change tenure and see the new EMI and interest saved |
| 3 | **Due-date alerts** | Highlights dues in the next 7 days and anything overdue |
| 4 | **Ask a question** | Answers plain-language questions about the customer's loans |

**How you build it matters as much as what you build.** Every team works in a private GitHub repo, follows a proper GitHub workflow, and uses GitHub Copilot throughout: instructions, skills, agents and MCP.

---

## 📜 Ground rules

- 🔒 **Made-up data only.** No real customer data, no production systems, no internal APIs.
- 🔑 **No secrets in code.** Use GitHub secrets or environment variables where needed.
- 🧰 **Any tech stack is allowed.** Choose what your team is comfortable with.
- 🌿 **Everything goes through pull requests.** No direct pushes to `main` after Challenge 1.
- ⏱️ **Code freeze:** all work must be merged in your private repo by the end of Day 2.
- 🤝 **Add the organisers** as collaborators on your repo so judges can review it.

---

## ✅ Before you start

Make sure every team member has:

- [ ] A GitHub account in the hackathon organisation
- [ ] A GitHub Copilot licence that is assigned and working
- [ ] VS Code (latest version) with the GitHub Copilot and GitHub Copilot Chat extensions
- [ ] Copilot **agent mode** and **MCP** enabled in VS Code
- [ ] Git installed and authenticated (`git config user.name` / `user.email`)
- [ ] Access to the team's private repository

> 💡 Hit a blocker? Bring it to an office hour **before** the hackathon. Don't lose Day 1 to setup.

---

## 🚩 The 8 challenges

| Day | Challenge | Focus |
|---|---|---|
| Day 1 | [1. Set up the repo and plan the work](#challenge-1--set-up-the-repo-and-plan-the-work) | GitHub basics |
| Day 1 | [2. Give Copilot your team's context](#challenge-2--give-copilot-your-teams-context) | Copilot instructions |
| Day 1 | [3. Build the loan dashboard and EMI calculator](#challenge-3--build-the-loan-dashboard-and-emi-calculator) | Branching, PRs, agent mode |
| Day 1 | [4. Automate quality with GitHub Actions](#challenge-4--automate-quality-with-github-actions) | Actions, CI, security |
| Day 2 | [5. Delegate a feature to the Copilot coding agent](#challenge-5--delegate-a-feature-to-the-copilot-coding-agent) | Coding agent |
| Day 2 | [6. Capture team know-how as a skill and a custom agent](#challenge-6--capture-team-know-how-as-a-skill-and-a-custom-agent) | Skills, custom agents |
| Day 2 | [7. Connect Copilot to tools with MCP](#challenge-7--connect-copilot-to-tools-with-mcp) | MCP |
| Day 2 | [8. Ship v1.0](#challenge-8--ship-v10) | Releases, deployment |

---

### Challenge 1 — Set up the repo and plan the work

**Concepts:** repositories · Issues · labels · milestones · GitHub Projects · branch protection

**Your tasks**

1. Create your team's **private** repository with a `README.md`, `.gitignore` and licence.
2. Turn the four app features into **Issues**. Add labels (`feature`, `bug`, `docs`) and a milestone called **v1.0**.
3. Create a **GitHub Projects** board with columns *To do / In progress / Done* and add your Issues.
4. Protect `main`: no direct pushes, and every change needs a pull request with at least **1 approval**.

**✅ Done when**

- [ ] The private repo exists and `main` is protected
- [ ] At least **6 Issues** are linked to the **v1.0** milestone
- [ ] The Project board shows your Issues across *To do / In progress / Done*

---

### Challenge 2 — Give Copilot your team's context

**Concepts:** repository custom instructions · path-specific instructions

**Your tasks**

1. Add `.github/copilot-instructions.md` covering:
   - your tech stack and coding standards
   - "use made-up data only"
   - currency formatting in ₹ with Indian number grouping (₹1,50,000)
   - rounding rules for money
2. Add at least one **path-specific instruction** file in `.github/instructions/`, for example `tests.instructions.md`: *"use framework X and cover edge cases such as zero tenure"*.
3. Merge both files through a **pull request**, not a direct push.

**✅ Done when**

- [ ] Both instruction files are on `main`, merged through a reviewed PR
- [ ] Your team can show one Copilot response that follows the instructions (for example, ₹ formatting without being asked)

---

### Challenge 3 — Build the loan dashboard and EMI calculator

**Concepts:** branching · commits · pull requests · code review · linking Issues · Copilot agent mode

**Your tasks**

1. Create a **feature branch**.
2. Use **Copilot agent mode** to:
   - generate a made-up dataset of **10–20 customers** and their loans
   - build the **loan dashboard**
   - build the **EMI calculator** with an amortisation schedule
3. Write **unit tests** for the EMI formula.
4. Open a PR that includes `Closes #<issue-number>`. A teammate reviews it and leaves at least one comment, then the team merges it.

**✅ Done when**

- [ ] The dashboard runs locally and shows EMI, outstanding balance and next due date for each loan
- [ ] The EMI unit tests pass
- [ ] The PR is merged and its Issue closed automatically

---

### Challenge 4 — Automate quality with GitHub Actions

**Concepts:** Actions · workflows · status checks · Dependabot · secret scanning

**Your tasks**

1. Create a workflow in `.github/workflows/` that **installs, lints and tests** the app on every pull request. Copilot can help you write it.
2. Make that workflow a **required status check** on `main`.
3. Turn on **Dependabot alerts** and **secret scanning**.
4. Break a test on purpose, then use Copilot to **explain the failure** and fix it.

**✅ Done when**

- [ ] The workflow file is in `.github/workflows/`
- [ ] At least one PR shows a ❌ check that later turned ✅
- [ ] A workflow status badge is in the README
- [ ] The check is required before a PR can merge

---

### Challenge 5 — Delegate a feature to the Copilot coding agent

**Concepts:** Copilot coding agent · writing well-scoped Issues · reviewing AI-authored PRs

**Your tasks**

1. Write a clear Issue for the **what-if simulator** (prepayment and tenure change). Include acceptance criteria and the tests you expect.
2. **Assign the Issue to Copilot.**
3. Review the pull request Copilot opens. Leave comments so Copilot iterates **at least once**.
4. Merge only after CI passes.

**✅ Done when**

- [ ] A merged PR authored by the Copilot coding agent exists
- [ ] The PR shows at least one round of review feedback and Copilot's follow-up commit
- [ ] The simulator shows the new EMI and the interest saved

---

### Challenge 6 — Capture team know-how as a skill and a custom agent

**Concepts:** agent skills · custom agents

**Your tasks**

1. Create an **agent skill** at `.github/skills/emi-rules/SKILL.md`. Capture your rules for EMI, prepayment, rounding and due-date calculation. Add a reference script or examples if helpful.
2. Create a **custom agent** in `.github/agents/`, for example:
   - a **Test Writer** agent that writes tests the way your team does, or
   - a **Data Privacy Reviewer** agent that flags anything that looks like real personal data
3. Use the skill and the agent to build the **due-date alerts** feature: show dues in the next 7 days and highlight overdue ones.

**✅ Done when**

- [ ] The skill and custom agent files are committed
- [ ] The due-date alerts feature is merged
- [ ] The PR description explains how the skill or agent was used

---

### Challenge 7 — Connect Copilot to tools with MCP

**Concepts:** Model Context Protocol (MCP) · GitHub MCP server · custom MCP server

**Your tasks**

1. Configure the **GitHub MCP server** in VS Code. From Copilot Chat, create or update Issues and check PR status without leaving the editor.
2. Build a small **MCP server** over your made-up loan data, with tools such as:
   - `get_loans(customer_id)`
   - `get_upcoming_dues(days)`
3. Use it to answer plain-language questions such as *"Which customers have dues in the next 7 days?"* This delivers the **Ask a question** feature.

**✅ Done when**

- [ ] The MCP configuration (for example `.vscode/mcp.json`) and the MCP server code are in the repo
- [ ] Your team can show Copilot Chat answering a loan question using your MCP tool
- [ ] At least one Issue was created through the GitHub MCP server

---

### Challenge 8 — Ship v1.0

**Concepts:** tags · GitHub Releases · release notes · deployment workflow · documentation

**Your tasks**

1. Add a **deployment workflow**, for example to GitHub Pages or as a build artifact.
2. Tag **`v1.0.0`** and publish a **GitHub Release** with auto-generated release notes.
3. Finish the README: what the app does, how to run it, the architecture, and **how your team used Copilot**.
4. Close the **v1.0** milestone.

**✅ Done when**

- [ ] Release **v1.0.0** is published
- [ ] There is a working demo link or downloadable build
- [ ] The v1.0 milestone is 100% closed
- [ ] Your team gives a **5-minute demo** to the judges

---

## 🧮 Scoring

Challenge points are tracked on the leaderboard as you go. Each "Done when" result is checked against your repo: files, merged PRs, tags and releases.

| Challenge | Points |
|---|---:|
| 1. Repo and planning | 10 |
| 2. Custom instructions | 10 |
| 3. Dashboard and EMI calculator | 15 |
| 4. Actions and quality | 10 |
| 5. Copilot coding agent | 15 |
| 6. Skill and custom agent | 15 |
| 7. MCP | 15 |
| 8. Release v1.0 | 10 |
| **Total** | **100** |

---

## ⚖️ Judging criteria

Finalists are judged on the demo and the repo.

| Criterion | Weight | What judges look for |
|---|---:|---|
| Business value | 25% | Does it solve the customer's problem clearly? |
| Use of GitHub Copilot | 25% | Instructions, skills, agents and MCP used with purpose |
| Working app and code quality | 20% | Runs, tested, readable |
| GitHub practices | 20% | Issues, PRs, reviews, Actions, release |
| Demo and documentation | 10% | Clear 5-minute demo and a useful README |

---

## 🏆 Leaderboard

*Last updated: [Add date and time]*

| Rank | Team | C1 | C2 | C3 | C4 | C5 | C6 | C7 | C8 | Points |
|---:|---|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|---:|
| 1 | [Team name] | ✅ | ✅ | ✅ | ⏳ | ⬜ | ⬜ | ⬜ | ⬜ | 35 |
| 2 | [Team name] | ✅ | ✅ | ⏳ | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ | 20 |
| 3 | [Team name] | ✅ | ⏳ | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ | 10 |

✅ Done · ⏳ In progress · ⬜ Not started

> Sample rows above are illustrative. Organisers update this table at each checkpoint.

---

## 📤 Submission checklist

Before code freeze, make sure your repo has:

- [ ] A protected `main` branch, with all work merged through PRs
- [ ] `.github/copilot-instructions.md` and at least one file in `.github/instructions/`
- [ ] At least one workflow in `.github/workflows/` with passing checks
- [ ] A merged PR authored by the Copilot coding agent
- [ ] `.github/skills/emi-rules/SKILL.md` and a custom agent in `.github/agents/`
- [ ] MCP configuration and MCP server code
- [ ] Release **v1.0.0** with release notes
- [ ] A complete README, including a "How we used Copilot" section
- [ ] Organisers added as collaborators

---

## 🙋 Help and resources

**Office hours**

| Session | Date | Focus |
|---|---|---|
| Office hour 1 | Wed, 9 Dec 2026 | Setup check, licences, repo access, Q&A on the challenges |
| Office hour 2 | Mon, 14 Dec 2026 | Final readiness, team formation, MCP and coding agent dry run |

**Documentation**

- [GitHub Docs](https://docs.github.com)
- [GitHub Copilot documentation](https://docs.github.com/copilot)
- [GitHub Actions documentation](https://docs.github.com/actions)
- [Model Context Protocol](https://modelcontextprotocol.io)

**During the hackathon:** post questions in [Add Teams channel or GitHub Discussions link]. Mentors will be available throughout both days.

---

<sub>Smart EMI agent Hackathon · Bajaj Finserv × Microsoft · All data used in this hackathon is fictional.</sub>
