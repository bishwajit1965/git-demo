# Git Demo

A hands-on Git and GitHub learning repository used to build **practical, professional Git skills** through real workflows, experiments, mistakes, recovery, and collaboration scenarios.

This repository is intentionally used as a working laboratory rather than a collection of theoretical examples.

## Purpose

The goal of this repository is to develop the Git skills expected from a professional full-stack developer, including:

* Repository and history management
* Branching and merging
* Feature development workflows
* GitHub collaboration
* Pull requests
* Undoing and recovering changes
* Rebase and stash
* Cherry-pick and patches
* Tags and releases
* `.gitignore` and `.gitattributes`
* Git LFS
* Commit signing with GPG
* Git hooks
* Advanced remote workflows
* Recovery and troubleshooting
* Git with CI/CD
* Professional team workflows

The syllabus is being completed progressively. **This repository is a learning project and is intentionally not considered finished yet.**

## Repository Goals

This repository is intended to achieve more than basic familiarity with Git commands.

### 1. Build Professional Git Competence

Develop the ability to use Git confidently in real software-development environments rather than only in isolated tutorials.

### 2. Understand Git Internals Through Practice

Build a practical mental model of:

* Commits
* Branches
* References
* HEAD
* Index/staging area
* Working tree
* Remote repositories
* History rewriting
* Object relationships

The objective is to understand **why Git behaves the way it does**, not simply memorize commands.

### 3. Develop Safe Recovery Skills

Learn how to investigate and recover from common Git problems, including:

* Accidental changes
* Wrong commits
* Merge conflicts
* Rebase problems
* Stash mistakes
* Incorrect branch operations
* Remote synchronization problems
* Lost or misplaced work

### 4. Practice Real Collaboration Workflows

Develop practical experience with:

* GitHub
* Forks
* Pull requests
* Remote branches
* Collaboration
* Review-oriented workflows
* Team-oriented Git practices

### 5. Build a Professional Git Workflow

Develop a repeatable workflow that can be carried into real full-stack projects:

```text id="7r4m2k"
Create
  ↓
Work
  ↓
Stage
  ↓
Commit
  ↓
Branch
  ↓
Integrate
  ↓
Review
  ↓
Push
  ↓
Release
  ↓
Maintain
```

### 6. Create Evidence of Practical Ability

This repository serves as a record of hands-on Git practice.

The objective is not merely to say:

> "I know Git."

It is to have a repository that demonstrates experience with real Git operations, workflows, recovery, collaboration, releases, and professional practices.

## Expected Outcomes

By completing the repository's syllabus, the expected outcome is the ability to:

* Use Git confidently in daily development.
* Understand and manage Git history.
* Create and maintain branches effectively.
* Merge and resolve conflicts.
* Rebase when appropriate.
* Temporarily store and recover work with stash.
* Move specific changes using cherry-pick.
* Create and manage patches.
* Manage releases with tags and GitHub Releases.
* Configure repositories using `.gitignore` and `.gitattributes`.
* Handle large binary files with Git LFS.
* Sign and verify commits using GPG.
* Work effectively with GitHub remotes.
* Participate in fork and pull-request workflows.
* Diagnose common Git problems.
* Recover work safely when things go wrong.
* Understand Git workflows used in professional teams.
* Integrate Git into CI/CD workflows.
* Apply these skills confidently to real full-stack projects.

### Final Outcome

The final goal is **professional Git readiness**:

> **To be able to enter an existing software project, work safely within its Git workflow, collaborate with other developers, manage changes and history, recover from mistakes, and deliver code through a professional Git/GitHub workflow.**

This repository is therefore treated as a **practical Git laboratory and evidence of capability**, not simply a tutorial exercise.

## Learning Approach

The repository follows a practical cycle:

```text id="om1c03"
Learn
  ↓
Execute
  ↓
Experiment
  ↓
Break
  ↓
Diagnose
  ↓
Recover
  ↓
Repeat
  ↓
Move On
```

The emphasis is on understanding **why Git behaves the way it does**, rather than memorizing commands.

## Current Git Syllabus

The complete roadmap is maintained in:

**[`GITSYLLABUS.md`](./GITSYLLABUS.md)**

The syllabus currently covers:

1. Git Fundamentals
2. Git History
3. Git Branching
4. Merge
5. Git Workflow
6. GitHub & Remote Repositories
7. GitHub Authentication
8. Forking & Collaboration
9. Pull Requests
10. Undo & Modification
11. Rebase
12. Stash
13. Cherry-pick & Patch
14. Tags & Releases
15. `.gitignore`
16. `.gitattributes`
17. Git LFS
18. Signing
19. Git Hooks
20. Submodules
21. Advanced Remote Git
22. Recovery & Troubleshooting
23. Git + CI/CD
24. Professional Team Simulation

The checkmarks in `GITSYLLABUS.md` indicate concepts that have already been practiced.

## What Has Already Been Practiced

Among the completed areas are:

* Git repository fundamentals
* Staging and commits
* Git history
* Branching
* Merge conflicts
* Practical Git workflow
* GitHub remotes
* HTTPS authentication
* Forking and contribution workflow
* Pull requests
* Undo and modification
* Rebase
* Stash
* Cherry-pick and patches
* Tags and GitHub Releases
* `.gitignore`
* `.gitattributes`
* Git LFS
* GPG commit signing

### Commit Signing

This repository also contains hands-on GPG signing practice.

The signing workflow was completed end-to-end:

```text id="6a1f0a"
GPG key pair
    ↓
Git configured for signing
    ↓
Signed commit
    ↓
Local signature verification
    ↓
Public GPG key added to GitHub
    ↓
GitHub displays "Verified"
```

This demonstrates commit authenticity verification, not code quality or security certification.

## Repository Structure

The repository intentionally remains simple because its primary purpose is learning Git itself.

```text id="m6h5oy"
git-demo/
│
├── GITSYLLABUS.md
├── README.md
├── practice.txt
├── signing-practice.txt
├── practice.zip
├── lfs-demo/
└── .gitattributes
```

Some files and directories are temporary practice artifacts created during individual Git exercises.

## Important Git Concepts

### `.gitignore`

Controls which **untracked** files Git should normally ignore.

```text id="ivqh90"
.gitignore
    ↓
What should Git leave alone?
```

It does not automatically remove files that are already tracked.

### `.gitattributes`

Controls how Git treats tracked files.

```text id="xynipw"
.gitattributes
    ↓
How should Git treat these files?
```

It can control line endings, text/binary behavior, LFS rules, and other Git attributes.

### Git LFS

Used for large binary files that are better handled outside Git's normal object storage.

```text id="ekmsek"
Git repository
    ↓
LFS pointer

Large binary
    ↓
Git LFS storage
```

### GPG Signing

Used to cryptographically sign commits.

```text id="tat1x1"
Private key
    ↓
Signs commit

Public key
    ↓
Verifies signature

GitHub
    ↓
Verified
```

## Philosophy

This repository is not intended to demonstrate how many Git commands can be memorized.

The objective is to develop the ability to answer questions such as:

* What happened?
* Why did Git do that?
* What state is the repository in?
* What is the safest way forward?
* Which Git operation is appropriate here?
* How do I recover without destroying useful history?
* How would this work in a real team?

A developer who can diagnose and recover from Git problems is more valuable than someone who simply remembers a list of commands.

## Status

**Learning in progress.**

The Git syllabus is deliberately being completed step by step. Additional advanced topics remain and will be practiced later.

---

Built as a practical Git learning laboratory for professional full-stack development.
