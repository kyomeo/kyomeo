<h1 align="center">Mikołaj Gruszka - Manual QA Tester</h1>
<h3 align="center">I test what ships, and I write down what I find</h3>

<p align="center">
  <img src="https://img.shields.io/badge/Manual_QA-Web-2E7D32?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Bug_Reporting-GitHub_Issues-181717?style=for-the-badge&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Root_Cause-Analysis-B45309?style=for-the-badge" />
  <img src="https://img.shields.io/badge/DevTools-Chrome-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white" />
</p>

I test two commercial web products as a manual tester. I run test scenarios from the browser against
staging and production, report every run as one structured comment under its ticket, and file what I
find as reproducible bug reports.

**36 issues filed, 19 already resolved. 10 of them public and clickable below. One merged pull request.**

---

## What I work on

### 🧝 lotro-translator.pl (public repository)

[koniecdev/LotroKoniecDev](https://github.com/koniecdev/LotroKoniecDev) is a platform that brings
Polish translations to *The Lord of the Rings Online*. I test the web application: account flows,
the translator editor, import/export, and the game-version admin area.

**10 issues filed, all closed. Four of them changed a rule the project still follows. One pull
request, merged.** Everything is public, so every claim on this page can be checked by opening it.

### 🐱 uratujkota.pl (private repository)

A cat adoption platform. I joined as a part-time manual tester in August 2026 and cover the sign-up
and account flows, the listing forms, the user profile area and data-protection features. The
repository is private, so nothing here is linkable; the findings below are described with the
product owner's consent.

**26 issues filed, 9 already fixed. Five QA tickets executed, on staging and on the live site.**
Three findings I would open with:

- **A cat's age was entered in years and stored as months.** Typing `3` created a cat born three
  months ago. The form accepted it, the record looked fine, and the data was quietly wrong.
- **The listing form saved without a required field and picked a value on its own.** The record came
  out looking complete while holding something nobody had chosen.
- **After sign-up through an external identity provider, the application-side profile was never
  created.** The consent record stayed empty and the GDPR data export came back with nothing in it.
  I traced it back to its cause: nothing sent a new account to the onboarding form, and that form is
  what creates the profile. Filing the cause as its own report closed both tickets.

---

## Selected work

### Merged pull request: the source-of-truth hierarchy

**[PR #727 "Wiki is the source of truth, above specs, ADRs and code"](https://github.com/koniecdev/LotroKoniecDev/pull/727)**

I kept hitting cases where the project's documentation, its architecture decisions and the running
product disagreed with each other, and nothing said which one wins. I proposed the rule that settles
it, and it was merged into the project's own instructions. It now governs how conflicts between
documentation and code are resolved across the whole repository.

### Reports that changed the project's rules

| Issue | What it was | What it changed |
|---|---|---|
| [#742](https://github.com/koniecdev/LotroKoniecDev/issues/742) | Test steps carried no ids, yet bug titles and tickets already cited them | Became a project rule: every test step now carries a stable id that is never reused or renumbered |
| [#726](https://github.com/koniecdev/LotroKoniecDev/issues/726) | Five things in the tester documentation that cost time when writing a ticket from it alone | One point **superseded a sentence in an accepted Architecture Decision Record** (ADR-0003) |
| [#736](https://github.com/koniecdev/LotroKoniecDev/issues/736) | Every user-visible date was rendered in UTC instead of local Polish time | Became a project rule and changed how dates are printed across pages, e-mails and file names |
| [#671](https://github.com/koniecdev/LotroKoniecDev/issues/671) | Users could not change their own e-mail address, a gap in GDPR right to rectification | Turned into its own specification and architecture decision record |

<!-- MIEJSCE ZAREZERWOWANE: tu wejdzie para "bug, test regresyjny, PR".
     Nie kasuj tej linijki, dopóki jej nie wypełnisz. -->

---

## How I work

I do not just tick checkboxes. I document a run so that someone else can repeat it.

- **Every run is one comment under its ticket.** Test id, status, environment, what actually
  happened, evidence, linked bug. Screenshots go straight into the comment, so a result and its
  proof never live in separate places. Pass rate is calculated from executed steps only, so blocked
  and not-run steps never inflate it.
  - **I work with an AI assistant, and nothing it writes goes out unread.** I dictate a run in plain
  language and it assembles the report; evidence goes straight into the comment. Figures are checked
  against the repository before anything is posted, and the pass or fail verdict stays mine. A report
  that reads well and counts wrong is worse than no report at all.
- **Statuses mean different things.** `FAILED` is a result: information obtained. `BLOCKED` is the
  absence of a result, and it keeps a run open until the missing precondition is delivered.
- **Evidence is mandatory where it matters.** Any step that consumes its own preconditions, such as
  an import, a deletion or a status change, gets a screenshot even when it passes. Tomorrow there is
  no way to show what it looked like before.
- **I look for the cause, not only the symptom.** Four unrelated broken screens on one product came
  down to a single missing redirect after sign-up. Reporting that cause closed the tickets that
  described the symptoms.
- **Severity and priority are two different questions.** How badly it hurts the user is my call and
  I rate it on every report. How soon it gets fixed belongs to the product owner.
- **One bug is one report.** Reproducible, with steps, environment, expected vs actual, and evidence.
- **I write test scenarios, not only execute them.** Example:
  [#725, game version number rules, list order and status-based delete](https://github.com/koniecdev/LotroKoniecDev/issues/725).

---

## Where I am now

I work as a Customer Support Specialist and I am moving into QA. Support is where I learned to take
a complaint written by a frustrated person and turn it into something specific enough to act on,
which is most of what a bug report is.

---

## Tools

`GitHub Issues` · `Claude Code (AI-assisted testing)` · `Google Sheets` · `Excel` · `Confluence` · `Markdown` · `Git (reading)`

---

## Contact

<p align="left">
  <a href="https://www.linkedin.com/in/mikolajgruszkaqa/"><img src="https://img.shields.io/badge/LinkedIn-Miko%C5%82aj_Gruszka-0A66C2?style=flat-square&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:mikolajgruszkaqa@gmail.com"><img src="https://img.shields.io/badge/Email-mikolajgruszkaqa@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white" /></a>
  <a href="https://github.com/kyomeo"><img src="https://img.shields.io/badge/GitHub-kyomeo-181717?style=flat-square&logo=github&logoColor=white" /></a>
</p>
