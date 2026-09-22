# 📌 FINAL GIT SYLLABUS QUESTIONNAIRE — LOCKED

## 🚀 1. Git Fundamentals ✅

- Git introduction
- Git vs GitHub
- Installation
- Configuration
- Get Started
- Repository
- Working tree
- Staging area
- Commits
- New files
- Staging
- Commit
- Status
- Diff
- Help

## 🚀 2. Git History ✅

- Log
- Show
- Commit hashes
- HEAD
- Parent commits
- Comparing commits
- History inspection
- Commit messages
- Amend

## 🚀 3. Git Branching ✅

- Branch concept
- Create branch
- Switch branch
- Rename branch
- Delete branch
- Branch listing
- Branch pointers
- Tracking branches
- Feature branches

## 🚀 4. Merge ✅

- Fast-forward merge
- Three-way merge
- Merge
- Merge conflicts
- Conflict markers
- Conflict resolution
- Abort merge
- Merge history

## 🚀 5. Git Workflow ✅

- Working with branches
- Feature workflow
- Main/development concepts
- Best practices
- Clean commits
- Team conventions

## 🚀 6.GitHub & Remote Repositories ✅

- GitHub
- Remote repositories
- remote
- origin
- Add remote
- Set remote
- Clone
- Fetch → [Fetch = get the remote changes and let me inspect them.]
- Pull → [Pull = get the remote changes and integrate them into my current branch.]
- Push
- Remote branches
- Tracking
- Branch synchronization

Footnote — GitHub & Remote Repositories

What is a remote repository?

A remote repository is a Git repository stored somewhere outside your local development environment, commonly on a platform such as GitHub.

It provides a place to store, share, synchronize, and collaborate on Git history and project files.

Mental model:

Local repository = my working copy and local history. Remote repository = the shared copy that other people and systems can access.

A typical relationship looks like:

Local Repository
      │
      │ push
      ↓
Remote Repository
      │
      │ fetch / pull
      ↓
Local Repository
What is GitHub?

GitHub is a platform for hosting Git repositories and providing collaboration features around them.

Git itself is the version-control system.

GitHub adds services such as:

Remote repository hosting.
Pull Requests.
Code review.
Issues.
Repository permissions.
Releases.
Actions and CI/CD.
Collaboration tools.

Therefore:

Git is the version-control tool; GitHub is a platform built around Git repositories.

Why use a remote repository?

A remote repository provides several important benefits.

It allows you to:

Back up your project history remotely.
Access the project from different machines.
Share code with other developers.
Collaborate through branches and Pull Requests.
Connect repositories to CI/CD systems.
Publish releases.
Maintain a public record of development work.

For professional development, GitHub also becomes an important part of a developer's technical portfolio.

Local vs remote repository

A local Git repository exists on your computer:

D:/trials/git-demo/.git

A remote repository can exist on GitHub:

github.com/username/git-demo

They are separate repositories connected through Git.

The local repository does not automatically synchronize with GitHub.

You explicitly transfer information using commands such as:

git push
git fetch
git pull
The origin remote

When a GitHub repository is connected as a remote, Git commonly names that remote:

origin

You can inspect it with:

git remote -v

Typical output:

origin  https://github.com/username/git-demo.git
origin  https://github.com/username/git-demo.git

origin is only a conventional name.

It is not a special Git keyword.

You could technically use another name, but origin is the standard convention for the primary remote.

What we practiced

Using the git-demo repository, we connected the local Git repository to GitHub and practiced the basic local-to-remote workflow.

The practice included:

Creating and using a GitHub repository.
Connecting the local repository to the remote.
Inspecting remote configuration.
Pushing local commits to GitHub.
Fetching remote information.
Pulling remote changes.
Understanding local and remote branches.
Tracking a remote branch.
Understanding how local and remote histories can diverge.
Using GitHub as the collaboration point for the repository.
Adding a remote

A local repository can be connected to GitHub with:

git remote add origin <repository-url>

For an HTTPS repository:

git remote add origin https://github.com/username/git-demo.git

Then verify:

git remote -v

This establishes the relationship:

Local repository
      │
      │ origin
      ↓
GitHub repository
Push

git push transfers local commits to the remote repository.

For example:

git push -u origin main

The first push commonly uses -u to establish an upstream tracking relationship.

After that, future pushes can often be performed simply with:

git push

Mental model:

Push = send my local commits to the remote repository.

Fetch

git fetch retrieves information from the remote repository without automatically changing your current working branch.

git fetch origin

It updates your knowledge of the remote repository.

Mental model:

Fetch = download remote information; don't automatically integrate it into my current work.

This makes fetch a relatively safe way to inspect what has changed remotely.

Pull

git pull generally performs two operations:

git fetch
   +
integration

For example:

git pull origin main

The exact integration mechanism can depend on configuration and Git version, but conceptually:

Pull = get remote changes and integrate them into the current branch.

Fetch vs pull

This distinction is important.

Fetch
git fetch

Gets remote information but leaves your current branch unchanged.

Pull
git pull

Gets remote changes and integrates them into your current branch.

Mental model:

fetch
  → "Show me what changed remotely."

pull
  → "Bring those changes into my current work."
Remote-tracking branches

When Git communicates with a remote, it maintains remote-tracking references such as:

origin/main

This is not the same thing as your local:

main

Think of them as:

main
  → my local branch

origin/main
  → my local record of the remote main branch

They can temporarily point to different commits.

Local and remote branches can diverge

Suppose:

A ── B ── C        main
      \
       D ── E      origin/main

The local and remote histories are no longer identical.

This is why understanding fetch, pull, push, merge, and rebase becomes important.

Git does not automatically assume that two different histories should simply overwrite one another.

Upstream tracking

When you run:

git push -u origin main

Git records a relationship between the local branch and the remote-tracking branch.

Conceptually:

main
  ↕
origin/main

This allows commands such as:

git push
git pull

to know which remote branch is associated with the current local branch.

GitHub as collaboration infrastructure

Once the repository is on GitHub, Git becomes part of a larger development workflow:

Local development
       ↓
Git commits
       ↓
Push
       ↓
GitHub
       ↓
Branches
       ↓
Pull Requests
       ↓
Review
       ↓
Merge
       ↓
CI/CD

This is why GitHub knowledge is important for professional development.

Knowing Git commands alone is not enough; developers also need to understand how Git is used inside a collaborative platform.

GitHub repository as a portfolio

A public GitHub repository can also provide evidence of practical development ability.

A well-maintained repository can demonstrate:

Meaningful commits.
Branching workflow.
Pull Requests.
Documentation.
Tests.
CI/CD.
Releases.
Real project structure.
Consistent development activity.

The repository therefore becomes more than storage.

It can become part of a developer's professional evidence.

Useful commands
# Inspect remotes
git remote -v

# Add a remote
git remote add origin <repository-url>

# Change a remote URL
git remote set-url origin <repository-url>

# Push a branch
git push -u origin main

# Push later changes
git push

# Fetch remote information
git fetch origin

# Pull and integrate remote changes
git pull origin main

# Inspect all branches
git branch -a
What we learned

The important lesson was understanding the relationship between:

Local repository
       ↕
     Git
       ↕
Remote repository
       ↕
     GitHub

We learned that:

git push
→ sends local commits to remote

git fetch
→ retrieves remote information

git pull
→ retrieves and integrates remote changes

And:

main
→ local branch

origin/main
→ remote-tracking reference

These concepts form the foundation for later topics such as Pull Requests, collaboration, CI/CD, and professional team workflows.

Practical professional rule

Never think of push, fetch, and pull as interchangeable. Know whether you are publishing your work, inspecting remote changes, or integrating remote changes into your local branch.

Before synchronizing repositories, understand which direction the data is moving:

push
Local → Remote

fetch
Remote → Local knowledge

pull
Remote → Local + integration
Final mental model
                 GitHub
                   │
             Remote Repository
                   │
        ┌──────────┴──────────┐
        │                     │
      fetch                  push
        ↓                     ↑
 Remote information       Local commits
        │                     │
        └──────────┬──────────┘
                   │
            Local Repository
                   │
                  pull
                   ↓
             Fetch + Integrate

Core lesson:

A remote repository is not simply a backup folder. It is the shared point where local Git development connects with collaboration, review, automation, and professional software delivery.

## 🚀 7. GitHub Authentication

- HTTPS
- SSH
- SSH keys
- Add SSH key to GitHub
- Test authentication
- Secure authentication practices

### Footnote — GitHub Authentication

**What is GitHub Authentication?**

GitHub authentication is the process Git uses to **prove that you are authorized to access a GitHub repository** when performing operations such as cloning, pulling, or pushing.

For GitHub repositories, the two common authentication approaches are:

- **HTTPS**
- **SSH**

**Mental model:**

> **Authentication = proving to GitHub that this Git operation is being performed by an authorized account.**

---

## Why is authentication important?

Git can work entirely on a local machine without authentication.

Authentication becomes important when Git communicates with a remote repository such as GitHub.

For example:

```text id="h7g8x3"
Local Repository
      │
      │ git push
      ↓
    GitHub
      │
      ↓
Authentication
      │
      ↓
Authorized?
   ↙       ↘
 Yes        No
 ↓           ↓
Push       Rejected
```

Without successful authentication, GitHub will not allow protected repository operations.

---

## HTTPS authentication

HTTPS uses a repository URL such as:

```text id="x4j6m2"
https://github.com/username/repository.git
```

When Git connects to GitHub over HTTPS, authentication is handled through GitHub's supported credential mechanisms.

GitHub no longer accepts a normal account password for Git operations over HTTPS.

Instead, HTTPS authentication can use a **Personal Access Token (PAT)** or a credential manager.

The important mental model is:

> **The HTTPS URL identifies the remote repository; credentials prove that you are authorized to access it.**

---

## What we used

For the `git-demo` repository, the remote was configured using HTTPS.

The remote can be inspected with:

```bash id="8m4y8c"
git remote -v
```

This allows you to verify where Git is sending and retrieving repository data.

A typical result looks like:

```text id="7t6p4q"
origin  https://github.com/username/git-demo.git
```

---

## HTTPS authentication workflow

The basic workflow is:

```text id="j7q2m8"
Local Git Repository
        ↓
git push
        ↓
GitHub HTTPS endpoint
        ↓
Credential authentication
        ↓
GitHub authorizes operation
        ↓
Push accepted
```

Once credentials are securely stored by the credential manager, repeated operations can often be performed without manually entering credentials every time.

---

## Personal Access Token

A **Personal Access Token (PAT)** can be used instead of a GitHub account password for HTTPS Git authentication.

A token should be treated like a password or other credential.

It should:

- Be protected.
- Have only the permissions required.
- Never be committed to a repository.
- Never be placed inside source code.
- Never be shared publicly.

If a token is exposed, it should be revoked and replaced.

---

## SSH authentication

SSH provides another common authentication mechanism.

Instead of authenticating with HTTPS credentials, SSH uses a cryptographic key pair.

The basic model is:

```text id="y0x5vw"
Private Key
     ↓
Your computer

Public Key
     ↓
GitHub
```

The private key remains on your computer.

The public key can be registered with GitHub.

GitHub can then verify that the connection is associated with the corresponding key.

---

## HTTPS vs SSH

Both approaches can provide authenticated access to GitHub repositories.

| HTTPS                                | SSH                                 |
| ------------------------------------ | ----------------------------------- |
| Uses HTTPS remote URL                | Uses SSH remote URL                 |
| Commonly uses PAT/credential manager | Uses SSH key pair                   |
| Easy to understand and configure     | Convenient once configured          |
| Works well with credential managers  | Strong cryptographic authentication |
| Credentials must be protected        | Private key must be protected       |

Neither should be treated as inherently mandatory for every developer.

The appropriate choice depends on the developer's environment and workflow.

---

## What we completed

For the Git learning syllabus, we completed the **HTTPS authentication path** and successfully used it with the `git-demo` repository.

The repository remote was configured for GitHub over HTTPS, allowing authenticated operations such as pushing changes.

We intentionally did not continue into a full SSH setup because the HTTPS workflow was sufficient for the Git developer-level syllabus.

SSH remains a useful professional skill that can be learned when a particular environment requires or benefits from it.

---

## Authentication vs authorization

These terms are related but different.

### Authentication

Answers:

> **Who are you?**

### Authorization

Answers:

> **What are you allowed to do?**

For example:

```text id="q7f4xy"
Authentication
     ↓
Identify the GitHub account
     ↓
Authorization
     ↓
Determine whether that account can push
```

Successfully authenticating does not automatically mean that every repository operation is permitted.

Repository permissions still matter.

---

## Authentication and remote repositories

Git authentication becomes relevant whenever Git communicates with a remote repository.

Examples include:

```bash id="2o6n3v"
git clone <repository-url>
git fetch
git pull
git push
```

Local operations such as:

```bash id="n8r6f1"
git status
git add .
git commit
```

normally do not require GitHub authentication because they operate on the local repository.

---

## Security principles

Authentication credentials are sensitive.

Never do this:

```text
commit PAT
paste private SSH key
store token in source code
publish credentials in README
```

Instead:

```text
Credential
    ↓
Secure credential storage
    ↓
Git operation
    ↓
GitHub
```

The repository should contain **code and configuration templates**, not private authentication credentials.

---

## What we learned

The important lesson was that Git and GitHub are separate systems.

Git provides the version-control mechanism.

GitHub provides the remote hosting and collaboration platform.

Authentication establishes a trusted connection between your local Git environment and the GitHub account/repository you are authorized to use.

```text id="x2n6qa"
Git
 ↓
Local version control

GitHub
 ↓
Remote repository + collaboration

Authentication
 ↓
Prove access to GitHub

Authorization
 ↓
Determine permitted operations
```

---

## Useful commands

```bash id="q3k8vs"
# Inspect remote repository
git remote -v

# Add an HTTPS remote
git remote add origin https://github.com/username/repository.git

# Change an existing remote
git remote set-url origin https://github.com/username/repository.git

# Push a branch
git push -u origin main

# Fetch remote changes
git fetch origin

# Pull remote changes
git pull origin main
```

---

## Practical professional rule

> **Treat GitHub credentials like production credentials: protect them, never commit them, and grant only the access that is actually required.**

For HTTPS, protect your token and credential-manager access.

For SSH, protect your private key and passphrase.

The authentication method can change, but the security principle does not.

---

## Final mental model

```text
HTTPS
  ↓
Remote URL
  ↓
Credential / PAT
  ↓
GitHub authentication
  ↓
Repository authorization
  ↓
Git operation allowed
```

or:

```text
SSH
  ↓
SSH remote URL
  ↓
Private/Public key pair
  ↓
GitHub authentication
  ↓
Repository authorization
  ↓
Git operation allowed
```

**Core lesson:**

> **Git handles version control; GitHub handles remote collaboration; authentication establishes trusted access between them.**

## 🚀 8. Forking & Collaboration / Contribution ⭐ ✅

- What is a fork?
- Fork vs clone
- Fork vs branch
- origin
- upstream
- Clone your fork
- Create feature branch
- Push to fork
- Synchronize fork
- Pull Request to upstream
- Contributing to another repository
- Open-source workflow

### Footnote — Git Forking & Collaboration / Contribution

**What is Forking?**

A **fork** is a copy of another user's or organization's repository under your own GitHub account.

Forking is especially useful when you want to contribute to a repository where you **do not have direct write access**.

**Mental model:**

> **Fork = create my own GitHub copy of someone else's repository so I can work independently and propose changes back to the original project.**

A typical open-source contribution workflow looks like:

```text
Original Repository
        │
        ↓
       Fork
        │
        ↓
Your GitHub Repository
        │
        ↓
Feature Branch
        │
        ↓
Changes + Commits
        │
        ↓
Pull Request
        │
        ↓
Original Repository
```

---

## Why use a fork?

Forking allows developers to contribute without requiring direct permission to modify the original repository.

It is commonly used for:

* Open-source contributions.
* Contributing to projects owned by another person or organization.
* Experimenting with an existing project safely.
* Developing changes independently before proposing them upstream.
* Maintaining a personal copy of a project.

Forking creates a boundary between the **original repository** and your own working copy.

---

## Fork vs Clone

These two concepts are related but different.

### Fork

A fork is created on the **GitHub platform**.

```text
Original GitHub Repository
          ↓
       GitHub Fork
          ↓
Your GitHub Repository
```

### Clone

A clone copies a repository from a remote location to your **local computer**.

```bash
git clone <repository-url>
```

So:

> **Fork = GitHub-side copy**

> **Clone = local working copy**

A common contribution workflow uses both:

```text
Original repository
        ↓
       Fork
        ↓
Your GitHub repository
        ↓
      Clone
        ↓
Your computer
```

---

## Fork vs Branch

A branch and a fork solve different problems.

### Branch

A branch is another line of development **inside the same repository**.

```text
Repository
   ├── main
   ├── feature
   └── bugfix
```

### Fork

A fork creates another repository under a different GitHub account.

```text
User A's repository
        │
        ↓
User B's fork
```

Therefore:

> **Branch = separation inside a repository**

> **Fork = separation between repositories/accounts**

---

## What we practiced

Using GitHub and the `git-demo` learning workflow, we explored the contribution model behind forks and collaboration.

The practice established the relationship between:

* Original repository.
* Forked repository.
* Local clone.
* Branches.
* Commits.
* Remote repositories.
* Pull Requests.
* Contribution to the upstream project.

The objective was to understand how a developer can contribute to a project **without directly owning or modifying its main repository**.

---

## The contributor workflow

A typical contribution begins by forking the repository on GitHub.

After the fork exists, clone your fork locally:

```bash
git clone <your-fork-url>
```

Move into the repository:

```bash
cd <repository>
```

Then create a feature branch:

```bash
git switch -c feature-name
```

Make the required changes and commit them:

```bash
git add .
git commit -m "Implement feature"
```

Push the branch to your fork:

```bash
git push -u origin feature-name
```

Then create a Pull Request from your fork to the original repository.

---

## Origin and upstream

Fork-based workflows often use two remote names:

```text
origin
  ↓
Your fork

upstream
  ↓
Original repository
```

For example:

```bash
git remote -v
```

might show:

```text
origin    → your GitHub fork
upstream  → original project
```

This distinction is important because your fork and the original project can continue to develop independently.

---

## Keeping your fork synchronized

The original repository may receive changes while you are working on your fork.

You can retrieve those changes from the upstream repository:

```bash
git fetch upstream
```

Then integrate the appropriate upstream changes into your local branch using the workflow chosen by the project.

For example:

```bash
git merge upstream/main
```

or, where appropriate:

```bash
git rebase upstream/main
```

The exact synchronization strategy depends on the project's contribution guidelines.

---

## Collaboration model

The complete relationship can be visualized as:

```text
                 Original Repository
                         │
                      upstream
                         │
                         ↓
                    Your Local
                         ↑
                      origin
                         │
                         ↓
                    Your Fork
                         │
                         ↓
                  Feature Branch
                         │
                         ↓
                    Pull Request
                         │
                         ↓
                 Original Repository
```

This is one of the most important GitHub collaboration patterns for open-source development.

---

## Contribution is more than code

A professional contribution may involve:

* Understanding the project's existing code.
* Reading contribution guidelines.
* Creating a focused branch.
* Making a small, relevant change.
* Writing clear commits.
* Testing the change.
* Explaining the change in the Pull Request.
* Responding to review comments.
* Updating the branch when necessary.

The objective is not simply to make code work.

The contribution must fit the **existing project and its workflow**.

---

## Good contribution practice

A good contribution should generally be:

* Focused.
* Understandable.
* Tested.
* Consistent with the existing project.
* Easy to review.
* Limited to the required change.

Avoid mixing unrelated changes into the same Pull Request.

For example, if you are fixing a validation bug, avoid simultaneously redesigning unrelated UI components.

This keeps review and integration much easier.

---

## Forking and Pull Requests

Forking and Pull Requests are closely connected.

The typical open-source contribution path is:

```text
Fork
  ↓
Clone
  ↓
Branch
  ↓
Change
  ↓
Commit
  ↓
Push
  ↓
Pull Request
  ↓
Review
  ↓
Merge
```

The fork provides the workspace.

The branch isolates the work.

The Pull Request provides the contribution mechanism.

---

## What we learned

The important lesson was understanding how Git and GitHub scale from **individual development to collaboration with people whose repositories you do not control**.

```text
Git
 ↓
Local development

GitHub
 ↓
Remote collaboration

Fork
 ↓
Independent repository copy

Branch
 ↓
Isolated work

Pull Request
 ↓
Proposed contribution

Review + Merge
 ↓
Integration
```

---

## Useful commands

```bash
# Clone your fork
git clone <your-fork-url>

# Inspect remotes
git remote -v

# Add the original repository
git remote add upstream <original-repository-url>

# Fetch changes from the original repository
git fetch upstream

# Create a feature branch
git switch -c feature-name

# Push your branch to your fork
git push -u origin feature-name
```

---

## Practical professional rule

> **When contributing to someone else's repository, keep your work isolated, focused, tested, and easy to review.**

Do not assume that the original project's workflow is the same as yours.

Before contributing, check:

```text
README
CONTRIBUTING.md
Issue / task description
Branching rules
Testing requirements
Pull Request guidelines
```

Following the project's existing conventions is itself part of being a good contributor.

---

## Final mental model

```text
Fork
  → My GitHub copy

Clone
  → My local copy

Branch
  → My isolated line of work

Commit
  → My recorded change

Push
  → Publish my branch

Pull Request
  → Propose my contribution

Review
  → Project maintainers evaluate it

Merge
  → Contribution becomes part of the original project
```

**Core lesson:**

> **Forking gives you a safe place to work; branches organize the work; commits record it; Pull Requests communicate it; review and merge turn the contribution into part of the original project.**

## 🚀 9. Pull Requests ✅

- Create PR
- PR branches
- Review
- Review comments
- Requested changes
- Update PR
- Merge PR
- Delete feature branch
- Keep local repository synchronized

### Footnote — Git Pull Requests

**What is a Pull Request?**

A **Pull Request (PR)** is a request to merge changes from one branch into another branch, usually after the changes have been pushed to a remote repository such as GitHub.

A PR is not a Git command. It is a **collaboration and review mechanism provided by platforms such as GitHub**.

**Mental model:**

> **Pull Request = “I have completed a change on my branch; please review it before we merge it into the target branch.”**

A typical workflow looks like:

```text
main
  │
  └── feature branch
          │
          ├── commit
          ├── commit
          └── commit
                │
                ↓
             push
                │
                ↓
        Pull Request on GitHub
                │
          review / discussion
                │
                ↓
              merge
                │
                ↓
              main
```

---

## Why use Pull Requests?

Pull Requests provide a controlled way to introduce changes into a shared branch.

They are commonly used to:

* Review code before merging.
* Discuss implementation decisions.
* Detect problems before they reach the main branch.
* Run automated tests and CI checks.
* Keep feature work separate from stable code.
* Maintain a record of what changed and why.
* Allow multiple developers to collaborate safely.

A PR therefore represents more than just code merging.

It is part of a **professional development workflow**.

---

## Pull Request vs Git Merge

`git merge` is a Git operation that combines histories.

A Pull Request is a **workflow around that operation**.

For example:

```text
Git:

git merge feature
```

This performs the actual integration locally.

A Pull Request on GitHub allows the integration to happen through a review process:

```text
Feature branch
      ↓
Push to GitHub
      ↓
Pull Request
      ↓
Review
      ↓
Checks
      ↓
Approval
      ↓
Merge
```

The PR therefore provides the collaboration layer around Git's branching and merging capabilities.

---

## What we practiced

Using the `git-demo` repository and GitHub, we practiced the basic Pull Request workflow.

The practice included:

* Working on a separate branch.
* Making commits on that branch.
* Pushing the branch to GitHub.
* Creating a Pull Request.
* Selecting the target branch.
* Reviewing the proposed changes.
* Understanding the difference between the source branch and target branch.
* Merging the Pull Request.
* Understanding what happens to the branches after merging.
* Removing or keeping branches according to the workflow.

The goal was to experience a real GitHub collaboration process rather than treating Pull Requests as only a GitHub button.

---

## Source branch and target branch

Every Pull Request has two important sides.

### Source branch

The branch containing the changes being proposed.

Example:

```text
feature/login
```

### Target branch

The branch that will receive those changes.

Example:

```text
main
```

So a PR can be understood as:

```text
feature/login
      │
      │ Pull Request
      ↓
     main
```

The direction matters.

The feature branch is proposing changes **into** the target branch.

---

## Pull Request review

A reviewer can inspect the proposed changes before they are merged.

They can:

* Read the changed files.
* Inspect individual lines.
* Leave comments.
* Ask for changes.
* Discuss implementation choices.
* Approve the Pull Request.

This creates an important separation:

> **Writing code and approving code do not have to be performed by the same person.**

That becomes especially important in team environments.

---

## Pull Request checks

Modern GitHub repositories can connect automated checks to Pull Requests.

For example:

```text
Pull Request
     ↓
CI workflow
     ↓
Install dependencies
     ↓
Run tests
     ↓
Build
     ↓
Result
```

A team can therefore require successful automated checks before allowing a PR to merge.

This connects Pull Requests directly with **CI/CD**.

---

## Pull Request discussion

A Pull Request also provides a permanent place to explain a change.

A useful PR description should normally answer questions such as:

```text
What changed?

Why was it changed?

How was it implemented?

How was it tested?

Are there any limitations or follow-up tasks?
```

This makes the PR useful later as part of the project's technical history.

---

## Pull Request conflicts

A Pull Request may show a merge conflict when the source and target branches contain incompatible changes.

The conflict is not a special type of Git problem.

It is the same underlying Git merge problem that can occur locally.

A developer may resolve it locally, commit the resolution, and push the updated branch.

The Pull Request then updates automatically.

Mental model:

```text
PR conflict
    ↓
Git cannot automatically combine changes
    ↓
Resolve conflict
    ↓
Commit resolution
    ↓
Push
    ↓
PR updates
```

---

## Pull Requests and branches

A Pull Request does not replace branches.

Branches provide isolation:

```text
main
 │
 ├── feature-A
 ├── feature-B
 └── bugfix-C
```

Pull Requests provide a controlled mechanism for bringing those changes back into an appropriate target branch.

Therefore:

> **Branch = isolated line of development**

> **Pull Request = proposed integration of that work**

---

## Pull Request and Forks

Pull Requests can also be created from a fork.

A common open-source workflow is:

```text
Original repository
       ↓
      Fork
       ↓
Your repository
       ↓
Feature branch
       ↓
Pull Request
       ↓
Original repository
```

This allows contributors to propose changes to repositories where they do not have direct write access.

This connects the Pull Request concept with the earlier **Forking & Collaboration** section.

---

## What we learned

The most important lesson was that a Pull Request is not simply a request to “pull code.”

It is a structured collaboration workflow that combines:

```text
Branching
   +
Commits
   +
Remote repository
   +
Code review
   +
Automated checks
   +
Discussion
   +
Merge
```

This makes Pull Requests one of the central workflows of professional Git-based development.

---

## Useful workflow

A typical feature workflow can be summarized as:

```bash
git switch -c feature-name

# make changes

git add .
git commit -m "Implement feature"

git push -u origin feature-name
```

Then create the Pull Request on GitHub:

```text
feature-name
     ↓
Pull Request
     ↓
main
```

After review and successful checks, the branch can be merged.

---

## Practical professional rule

> **Do not treat a Pull Request as merely a place to click “Merge.” Treat it as a communication, review, testing, and integration point.**

A good PR should make it easy for another developer to understand:

**what changed, why it changed, and whether it is safe to merge.**

---

## Final mental model

```text
Branch
  ↓
Isolate work

Commit
  ↓
Record progress

Push
  ↓
Publish branch

Pull Request
  ↓
Request review + integration

Review / Checks
  ↓
Validate the change

Merge
  ↓
Integrate into target branch
```

**Core lesson:**

> **A Pull Request is the professional bridge between individual development work and shared project integration.**

## 🚀 10. Undo & Modification

- restore → [restore → discard my file change]

- Unstage → [restore --staged → unstage my change]

- Amend → [fix my latest commit]

- revert → [undo an existing commit with a new commit]

- reset → [git reset = Move the branch/HEAD backward, optionally changing what is staged or kept in the working tree.]

- Soft reset → [--soft moves HEAD backward but keeps the undone commit's changes staged.]

- Mixed reset → [Mixed reset = move HEAD backward and unstage the changes.]

- Hard reset → [Hard reset doesn't know which changes you care about. It resets the working tree to the target commit.]

- Reset vs revert

- Local vs shared history

- Safe/unsafe situations

|=======================================================
|
| COMMAND       HEAD     Staging     Working Tree
|
|=======================================================
| --soft        moves      KEEP          KEEP
| --mixed       moves      CLEAR         KEEP
| --hard        MOVE       CLEAR          RESET/DISCARD
|
|-------------------------------------------------------

### Footnote — Git Undo & Modification

**What is Git Undo & Modification?**

Git provides several ways to **correct, discard, reverse, or modify changes** depending on where those changes currently exist.

The important skill is not memorizing undo commands. It is understanding **what you want to undo and where that change currently lives**.

**Mental model:**

> **Before undoing anything, identify whether the change is in the working directory, staging area, local history, or shared history. Then choose the least destructive operation that solves the problem.**

---

## Why is undo and modification important?

Mistakes are normal in real development.

You may:

= Modify the wrong file.
= Stage something accidentally.
= Want to remove a file from staging but keep the changes.
= Make a mistake in the latest commit.
= Need to reverse an existing commit.
= Need to move local history backward.
= Need to recover from an incorrect operation.

Professional Git usage means being able to correct these situations **without unnecessarily losing useful work**.

---

## The Git state model

Think about Git as several layers:

```text
Working Directory
       ↓
Staging Area
       ↓
Local Commit History
       ↓
Remote Repository
```

The farther a change has travelled, the more carefully it should generally be modified or undone.

---

## Discard working-directory changes

If a file has been modified but the changes have **not been staged**, Git can restore it to the state of the last commit:

```bash
git restore <file>
```

Example:

```bash
git restore practice.txt
```

This discards the current uncommitted changes in that file.

Because this operation can permanently remove those working-tree changes, it should only be used when the changes are no longer needed.

---

## Unstage a file

If a file has been staged but should not be included in the next commit:

```bash
git restore --staged <file>
```

This removes the file from the staging area but **keeps the changes in the working directory**.

Mental model:

```text
Staged change
      ↓
git restore --staged
      ↓
Unstaged change
```

The work remains; only its staging state changes.

---

## Modify the latest commit

If the latest commit contains a small mistake, it can be modified instead of creating another unnecessary commit.

```bash
git commit --amend
```

For example, after adding something that should have been included in the previous commit:

```bash
git add <file>
git commit --amend
```

The commit message can also be changed:

```bash
git commit --amend -m "Correct commit message"
```

Amending replaces the previous commit with a new commit.

Therefore, its commit identity changes.

---

## Revert a committed change

If a committed change needs to be undone while preserving the existing history, use:

```bash
git revert <commit>
```

Git creates a **new commit** that reverses the effect of the selected commit.

For example:

```text
A ── B ── C
```

If `B` is reverted:

```text
A ── B ── C ── Revert-B
```

The original commit remains in the history.

This makes `git revert` particularly useful for changes that have already been shared with others.

---

## Reset

`git reset` is used to move the current branch reference backward and can also change the staging and working-tree state depending on the option used.

Common forms are:

```bash
git reset --soft
git reset --mixed
git reset --hard
```

Conceptually:

```text
--soft
→ move HEAD, keep changes staged

--mixed
→ move HEAD, keep changes unstaged

--hard
→ move HEAD and discard tracked working-tree/staging changes
```

`--hard` is therefore particularly dangerous when valuable local changes exist.

---

## Reset vs revert

This distinction is one of the most important parts of Git undo operations.

| Situation                         | Typical operation      |
| --------------------------------- | ---------------------- |
| Discard local file changes        | `git restore`          |
| Unstage a file                    | `git restore --staged` |
| Correct the latest commit         | `git commit --amend`   |
| Move local history backward       | `git reset`            |
| Reverse a committed/shared change | `git revert`           |

The correct command depends on **what state the change is currently in**.

---

## What we practiced

Using the `git-demo` repository, we developed the ability to:

- Understand Git's different change states.
- Distinguish working-directory changes from staged changes.
- Correct staging mistakes.
- Understand how committed changes can be modified or reversed.
- Distinguish `reset` from `revert`.
- Recognize destructive operations.
- Treat Git history as a recovery mechanism.
- Choose an undo operation based on the actual state of the repository.

The main objective was to understand **why different undo commands exist**, rather than simply memorizing their syntax.

---

## Always inspect before undoing

Before performing an undo operation, first check the repository:

```bash
git status
```

When history is relevant:

```bash
git log --oneline
```

These commands help answer:

> **Where is my change right now?**

Only after answering that question should you choose the undo operation.

---

## The golden rule of Git undo

> **Never choose an undo command before identifying where the change currently exists.**

Think through the sequence:

```text
Working directory?
       ↓
Staged?
       ↓
Committed?
       ↓
Already pushed/shared?
```

Then choose the least destructive operation appropriate to the situation.

---

## Local history vs shared history

Git gives you considerable freedom when working on your own local history.

Once commits have been pushed and other developers may depend on them, history changes become more sensitive.

A practical distinction is:

```text
Local / unpublished
→ history can often be rewritten

Shared / published
→ prefer preserving history when possible
```

This is why `reset`, `amend`, and other history-changing operations require more care after work has been shared.

---

## Useful commands

```bash
# Inspect repository state
git status

# Inspect commit history
git log --oneline

# Discard working-directory changes
git restore <file>

# Unstage a file
git restore --staged <file>

# Modify the latest commit
git commit --amend

# Move local history backward
git reset <option>

# Reverse an existing commit
git revert <commit>
```

---

## What we learned

The most important lesson was that **Git does not have one universal undo command**.

Different commands solve different problems:

```text
git restore
  → discard working-tree changes

git restore --staged
  → remove changes from staging

git commit --amend
  → correct the latest commit

git reset
  → move local history/state

git revert
  → create a new commit that reverses an existing commit
```

These operations should not be treated as interchangeable.

---

## Mental model

> **Git undo is really about controlling the state and history of your changes.**

```text
Working change
      ↓
git restore
      ↓
Discard

Staged change
      ↓
git restore --staged
      ↓
Unstage

Latest commit
      ↓
git commit --amend
      ↓
Correct

Local history
      ↓
git reset
      ↓
Move/rewrite

Shared commit
      ↓
git revert
      ↓
Reverse safely
```

**Practical rule:**

> **Use the least destructive Git operation that solves the problem, and always inspect the repository state before undoing anything.**

## 🚀 11. Rebase ✅

- What rebase is
- Rebase vs merge
- Basic rebase
- Rebase workflow
- Rebase conflicts
- Continue
- Abort
- Interactive rebase
- Squashing
- Reordering/editing commits
- When to use/not use rebase

### Footnote — Git Rebase

**What is `git rebase`?**
`git rebase` moves or **replays a series of commits onto a different base commit**.

Its primary purpose is to create a cleaner, more linear project history by changing where a branch's commits are based.

**Mental model:**

> **Rebase = take my commits, temporarily lift them away, move the branch to a new base, then replay those commits on top.**

Suppose the history is:

```text id="h7k3vp"
A ── B ── C        main
      \
       D ── E      feature
```

If `main` has moved forward and we rebase `feature` onto `main`:

```text id="m4q8zn"
A ── B ── C ── D' ── E'    feature
```

The changes from `D` and `E` are replayed after `C`.

The resulting commits `D'` and `E'` are **new commits with new commit identities**.

---

## Why use rebase?

Rebase can be useful when:

* Updating a feature branch with the latest `main`.
* Keeping project history linear.
* Preparing a branch before opening a pull request.
* Cleaning up local commits before sharing them.
* Avoiding unnecessary merge commits in appropriate workflows.

Rebase is primarily a **history-rewriting operation**.

---

## Rebase vs merge

Both can integrate changes, but they do it differently.

### Merge

```text id="n2v7cx"
A ── B ── C ───── M
      \           /
       D ── E ───
```

Merge combines the histories and may create a merge commit.

### Rebase

```text id="q8m4wp"
A ── B ── C ── D' ── E'
```

Rebase replays the feature commits on the new base and produces a linear history.

Neither operation is universally "better."

The correct choice depends on the team's workflow and whether rewriting history is appropriate.

---

## What we practiced

We practiced rebase using the `git-demo` repository and created separate commits on branches so that the effect of rebasing could be observed.

The practice included:

- Moving a branch onto a newer base.
- Observing that rebased commits receive new hashes.
- Working with rebase conflicts.
- Continuing a rebase after resolving conflicts.
- Aborting a rebase safely.
- Understanding what happens to branch history during a rebase.
- Using interactive rebase to inspect and reorder local commits.
- Protecting important syllabus work before history-changing operations.

---

## Basic rebase workflow

First inspect the branches:

```bash id="r6k2mv"
git log --oneline --graph --all
```

Switch to the branch that should be rebased:

```bash id="x9p4wc"
git switch feature
```

Then rebase it onto `main`:

```bash id="v3m8qn"
git rebase main
```

Git replays the feature commits on top of the current `main`.

---

## Rebase conflicts

A rebase can stop when Git cannot automatically apply a commit.

Check the repository state:

```bash id="c5r7yk"
git status
```

Resolve the conflicted files manually.

Then stage the resolved files:

```bash id="p8m2vd"
git add <resolved-file>
```

Continue the rebase:

```bash id="w4k9zs"
git rebase --continue
```

Git then continues replaying the remaining commits.

---

## Aborting a rebase

If the rebase becomes undesirable or confusing, it can be cancelled:

```bash id="f7n3qx"
git rebase --abort
```

This is an important recovery mechanism.

It tells Git:

> Stop the current rebase operation and return the branch to the state it was in before the rebase started.

---

## Skipping a commit

In certain situations, a particular commit may no longer be needed during a rebase.

Git provides:

```bash id="k2v8mp"
git rebase --skip
```

This skips the commit currently being replayed.

This should only be used when you understand why that commit should not be replayed.

---

## Interactive rebase

Interactive rebase provides more control over local commit history.

Example:

```bash id="n6q3wr"
git rebase -i HEAD~3
```

It can be used to:

- Reorder commits
- Edit commit messages
- Squash commits
- Fix up commits
- Edit commits
- Remove commits

Common commands in the interactive rebase editor include:

```text id="b5m9xc"
pick    → keep the commit
reword  → change the commit message
edit    → stop and modify the commit
squash  → combine with the previous commit
fixup   → combine without keeping the commit message
drop    → remove the commit
```

Interactive rebase is especially useful for cleaning up **local, unpublished history**.

---

## Why rebased commits get new hashes

A Git commit is identified partly by the data describing its parent commit.

When a commit is replayed onto a different parent:

```text id="t7q4mz"
Original:

B → D

Rebased:

C → D'
```

The content may represent the same logical change, but its parent relationship has changed.

Therefore Git creates a new commit identity.

This is why:

> **Rebase rewrites history.**

---

## The golden rule of rebase

Be careful when rebasing commits that other people already depend on.

If a shared branch contains:

```text id="j4p8vx"
A ── B ── C
```

and those commits are already used by other developers, rewriting them can cause synchronization problems.

A practical rule is:

> **Rebase your own local/unpublished work freely; be cautious about rebasing shared/public history.**

The exact policy depends on the team's workflow.

---

## Rebase and force push

After rebasing a branch that has already been pushed, its history may no longer match the remote branch.

A normal push may be rejected.

In appropriate situations, a safer force-push form is:

```bash id="z8m3qk"
git push --force-with-lease
```

`--force-with-lease` provides an additional safety check compared with a blind:

```bash
git push --force
```

It helps prevent overwriting remote changes that you did not know about.

Force-pushing should still be used carefully on shared branches.

---

## Rebase and stash

Git may require a clean working tree before starting certain rebase operations.

If unfinished changes are present, you may need to:

```bash id="e5r7nw"
git stash
```

perform the rebase, and then restore the work.

This is one reason understanding stash and rebase together is useful.

---

## Useful commands

```bash id="s4k8xp"
# View history
git log --oneline --graph --all

# Rebase current branch onto main
git rebase main

# Continue after resolving a conflict
git rebase --continue

# Skip the current commit
git rebase --skip

# Abort the rebase
git rebase --abort

# Start interactive rebase
git rebase -i HEAD~3

# Safely force-push rewritten history
git push --force-with-lease
```

---

## What we learned

The most important lesson was not the command itself.

We learned to recognize **when rebase is appropriate and what it actually changes**.

```text
```

## 🚀 12. Stash ✅

- Why stash
- Create stash
- List stash
- Apply
- Pop
- Drop
- Clear
- Stashing specific work
- Practical use cases

### Footnote — Git Stash

---
📌 git stash
→ Temporarily save your tracked, uncommitted changes
→ Working tree becomes clean
→ Think: “Put my unfinished work aside.”

📌 git stash list
→ Show all saved stashes
→ stash@{0} = newest
→ stash@{1} = next older
→ Think: “What unfinished work have I saved?”

📌 git stash apply
→ Restore a stash
→ Keep the stash in the stash list
→ Think: “Bring it back, but keep a backup.”

📌 git stash pop
→ Restore a stash
→ Remove that stash from the stash list
→ Think: “Bring it back and remove the backup.”

📌 git stash drop
→ Delete one stash without restoring it
→ Example: git stash drop stash@{1}
→ Think: “I don't need this saved work anymore.”

📌 git stash push -u
→ Stash tracked changes + untracked files
→ -u = --include-untracked
→ Think: “Save everything unfinished, including new files.”

📌 git stash push -m "message"
→ Save your changes with a meaningful description
→ Makes multiple stashes easier to identify
→ Example: git stash push -m "Work on login feature"

📌 git stash clear
→ Delete ALL saved stashes
→ Cannot choose individual entries
→ ⚠️ Use carefully
→ Think: “Empty the entire stash stack.”

---

stash        → save
list         → see
apply        → restore + keep
pop          → restore + remove

---

**What is `git stash`?**
`git stash` temporarily saves changes from the working tree and staging area so you can return to a clean working tree without committing unfinished work.

It is useful when you are in the middle of one task but need to temporarily switch context—for example, to change branches, handle an urgent fix, or investigate another problem.

**Mental model:**

> **Stash = temporary storage for unfinished work.**

```text id="n4k8wp"
Working on Task A
      ↓
Unfinished changes
      ↓
git stash
      ↓
Clean working tree
      ↓
Work on Task B
      ↓
Return to Task A
      ↓
Restore stashed changes
```

### Why use stash?

A developer may have local changes that are not ready to become a commit.

For example:

```text id="q7m3vx"
Feature work
    ↓
50% complete
    ↓
Urgent bug needs investigation
    ↓
Cannot commit unfinished feature
    ↓
git stash
    ↓
Clean repository
```

Stash allows the unfinished work to be temporarily put aside.

### What we practiced

We practiced the complete basic stash workflow:

```bash id="k5r9tc"
git stash
```

This temporarily stored the current working changes and returned the working tree to a clean state.

We then inspected available stashes:

```bash id="m2x7qp"
git stash list
```

This showed the saved stash entries.

A stash is identified using a reference such as:

```text id="b8v4zn"
stash@{0}
```

We also inspected the contents of a stash:

```bash id="c6w9ks"
git stash show --stat stash@{0}
```

and examined the actual patch:

```bash id="r3n5mv"
git stash show -p stash@{0}
```

This demonstrated that a stash is not just an unexplained "save"; it contains actual changes that can be inspected.

### Applying a stash

To restore a stash while **keeping the stash entry**:

```bash id="x9q4wd"
git stash apply stash@{0}
```

This is useful when you want to restore the work but retain the stash as a safety copy.

### Popping a stash

To restore the stash and remove it from the stash list:

```bash id="v6m2kp"
git stash pop
```

Conceptually:

```text id="r8n3yc"
apply → restore changes + keep stash

pop   → restore changes + remove stash
```

### Dropping a stash

When a stash is no longer needed:

```bash id="t4k7zs"
git stash drop stash@{0}
```

This removes that stash entry.

To remove all stashes:

```bash id="w5p8mq"
git stash clear
```

Use this carefully because removing stash entries can make previously saved work difficult to recover.

### Important distinction: stash is not a commit

A stash is useful temporary storage, but it should not be treated as permanent project history.

```text id="j7c2rx"
Commit
    ↓
Permanent project history

Stash
    ↓
Temporary unfinished work
```

If the work is important and complete, commit it.

### Stash and untracked files

By default, `git stash` primarily saves tracked modifications.

To also stash untracked files:

```bash id="e8m4qn"
git stash -u
```

To include ignored files as well:

```bash id="s3v7kp"
git stash -a
```

Be deliberate with these options because they save more than a normal stash.

### Named stash messages

A descriptive message can make stash entries easier to understand:

```bash id="y6n2wc"
git stash push -m "unfinished authentication work"
```

Then:

```bash id="p4r8zm"
git stash list
```

might show a meaningful description instead of an anonymous stash.

### Stash conflicts

Applying a stash can sometimes produce conflicts if the current working tree has changed significantly since the stash was created.

The normal approach is:

```bash id="u7k3qx"
git status
```

Resolve the conflicts, stage the resolved files, and continue working normally.

Unlike a commit, a stash does not automatically create a new commit when it is applied.

### What we learned about real-world stash management

During the Git syllabus work, multiple stash entries accumulated.

Instead of blindly popping them, we inspected them individually:

```bash id="a2m9vf"
git stash list
git stash show --stat stash@{0}
git stash show -p stash@{0}
```

We identified which stash contained important syllabus progress and which contained obsolete or unrelated practice changes.

The important lesson was:

> **Inspect a stash before applying or deleting it when its contents matter.**

We deliberately used:

```bash id="h5q8wd"
git stash apply stash@{0}
```

instead of immediately using `pop`, because `apply` preserves the stash as a safety copy.

### Useful commands

```bash id="d8m4xp"
# Save current changes
git stash

# Save including untracked files
git stash -u

# List stashes
git stash list

# Inspect stash summary
git stash show --stat stash@{0}

# Inspect stash changes
git stash show -p stash@{0}

# Apply without deleting the stash
git stash apply stash@{0}

# Apply and remove the stash
git stash pop

# Delete one stash
git stash drop stash@{0}

# Delete all stashes
git stash clear
```

### Practical rule

Use stash when work is **temporary and unfinished**.

If the work represents a meaningful completed change, **commit it instead**.

### Mental model

> **Stash = temporarily put unfinished work aside so the working tree can be used for something else.**

```text id="z9c5vk"
Unfinished work
      ↓
    STASH
      ↓
Clean working tree
      ↓
Do other work
      ↓
Restore stash
      ↓
Continue unfinished work
```

## 🚀 13. Cherry-pick & Patch

- Cherry-pick
- Selective commit application
- Cherry-pick conflicts
- Abort/continue
- Patch concepts
- When useful

### Footnote — Cherry-pick & Patch

**What is `git cherry-pick`?**
`git cherry-pick` takes the change introduced by a **specific existing commit** and applies that change onto the current branch.

It is useful when you need **one particular commit** from another branch without merging the entire branch.

**Mental model:**

> **Cherry-pick = a gap-filling mechanism.**

If another branch contains a useful commit:

```text id="p8m4vz"
main:       A ── B ── C
                  \
feature:           D ── E
```

and only commit `D` is needed on `main`:

```bash id="x4n7kc"
git cherry-pick <commit-hash>
```

Git applies the change introduced by `D` to the current branch and creates a **new commit** on that branch.

Conceptually:

```text id="r2q6wm"
main:       A ── B ── C ── D'
                  \
feature:           D ── E
```

`D'` contains the same change as `D`, but it is a **different commit with a different commit identity**.

---

### Why use cherry-pick?

Cherry-pick can be useful when:

- One specific bug fix is needed on another branch.
- A useful commit was made on the wrong branch.
- A hotfix needs to be transferred to a release branch.
- You need one isolated change rather than the entire branch history.

It should not automatically replace merging or rebasing. The correct tool depends on the situation.

---

### What we learned

The important distinction was:

```text id="j7c3ns"
Merge
    ↓
Bring branch histories together

Rebase
    ↓
Replay a branch on a different base

Cherry-pick
    ↓
Bring one specific commit's change
```

This is why cherry-pick is particularly useful when you need a **specific change rather than an entire line of development**.

---

### Basic workflow

First identify the commit:

```bash id="v5n8rx"
git log --oneline
```

Then switch to the branch that should receive the change:

```bash id="m3q7kp"
git switch main
```

Then cherry-pick the required commit:

```bash id="a6w2zt"
git cherry-pick <commit-hash>
```

Git creates a new commit containing the selected change.

---

### Cherry-pick conflicts

A cherry-pick can produce conflicts if the selected change cannot be applied cleanly to the current branch.

Git may stop and show conflicted files.

The normal recovery process is:

```bash id="d9k4qw"
git status
```

Resolve the conflicting files, then:

```bash id="f2m8vc"
git add <resolved-file>
git cherry-pick --continue
```

If you decide not to continue:

```bash id="s6r3xp"
git cherry-pick --abort
```

This returns the repository to the state before the cherry-pick operation.

---

## What is a patch?

A **patch** is a representation of changes between versions of files.

Git can create a patch from a commit:

```bash id="n7v4km"
git format-patch -1 <commit-hash>
```

This produces a patch file that represents the commit's changes.

A patch can then be applied elsewhere with:

```bash id="q3w8zs"
git apply <patch-file>
```

There is also:

```bash id="h6p2rx"
git am <patch-file>
```

which applies an email-style patch and can preserve commit metadata when the patch was produced by `git format-patch`.

---

### `git apply` vs `git am`

```text id="u4k9nb"
git apply
    ↓
Applies file changes
    ↓
Does not automatically create the original commit

git am
    ↓
Applies a mail-formatted patch
    ↓
Can recreate the commit with its metadata
```

This distinction matters when working with patches as part of a contribution workflow.

---

### Important distinction

Cherry-pick and patch are related but not identical:

```text id="w8m3qz"
Cherry-pick
    ↓
Select a Git commit
    ↓
Apply its change
    ↓
Create a new commit


Patch
    ↓
Represent changes as a patch
    ↓
Transfer/apply those changes
```

Cherry-pick works directly with Git commits. A patch is a portable representation of changes.

---

### Useful commands

```bash id="e5r7kx"
# Find commits
git log --oneline

# Apply one commit
git cherry-pick <commit-hash>

# Continue after resolving a conflict
git cherry-pick --continue

# Cancel cherry-pick
git cherry-pick --abort

# Create a patch from a commit
git format-patch -1 <commit-hash>

# Apply a patch
git apply <patch-file>

# Apply a mail-formatted patch
git am <patch-file>
```

### Mental model

> **Cherry-pick m**

## 🚀 14. Tags & Releases

- Tags
- Lightweight tags
- Annotated tags
- Create/delete tags
- List tags
- Push tags
- Versioning
- Release workflow

### Footnote — Tags & Releases

**What is a Git tag?**
A Git tag is a **named reference to a specific commit**.

Instead of referring to a commit only by its hash:

```text
a1b2c3d...
```

we can give that commit a meaningful name:

```text
v1.0.0
```

Tags are commonly used to identify important points in a project's history, especially versions and releases.

**Why use tags?**

A branch such as `main` continues to move forward:

```text
A ── B ── C ── D ── E ── F
          ↑
        v1.0.0
```

The tag `v1.0.0` continues to identify commit `C` even after new commits are added.

This makes it easy to say:

> "This repository's version 1.0.0 corresponds to this exact commit."

**Tag vs branch:**

```text
Branch
    ↓
Moves as new commits are added

Tag
    ↓
Normally stays attached to the commit it identifies
```

This makes tags appropriate for marking versions, milestones, and other important historical points.

-----------------------------------------------------

### What is a release?

A **GitHub Release** is a human-facing publication built around a particular Git tag.

It can provide:

- Version number
- Release title
- Release notes
- Description of changes
- Links/downloadable assets
- Pre-release or stable-release status

Think of it as:

```text
Git commit
    ↓
Git tag
    ↓
GitHub Release
    ↓
Human-readable published version
```

A tag identifies the exact code; a release communicates that version to people.

---

### What we practiced

We created a lightweight version tag:

```bash id="q7v3km"
git tag v1.0.0
```

Then verified the tag:

```bash id="c8n5rx"
git tag
```

and pushed it to GitHub:

```bash id="m4p9ws"
git push origin v1.0.0
```

We then created a GitHub Release associated with `v1.0.0`.

The release was deliberately marked as a **pre-release/test release**, with the description:

```text
It is a test release only.
```

This demonstrated the complete relationship between a Git commit, a tag, and a GitHub Release.

---

### Lightweight vs annotated tags

A lightweight tag is essentially a simple named reference:

```bash id="h2k6wd"
git tag v1.0.0
```

An annotated tag stores additional tag information such as:

- Tag message
- Tagger
- Tagging date
- Tag object

Example:

```bash id="r5t8qn"
git tag -a v1.0.0 -m "Release version 1.0.0"
```

For serious published releases, annotated tags are generally more informative because the tag itself carries metadata.

---

### Useful commands

```bash id="z3f7kp"
# Create a lightweight tag
git tag v1.0.0

# Create an annotated tag
git tag -a v1.0.0 -m "Release version 1.0.0"

# List tags
git tag

# Show tag information
git show v1.0.0

# Push one tag
git push origin v1.0.0

# Push all local tags
git push origin --tags

# Delete a local tag
git tag -d v1.0.0

# Delete a remote tag
git push origin --delete v1.0.0
```

**Important:** Deleting a tag does not delete the commit itself. The commit remains part of Git history as long as it is otherwise reachable.

---

### Version naming

A common convention is **Semantic Versioning**:

```text
MAJOR.MINOR.PATCH

1.0.0
│   │ │
│   │ └── Patch: backward-compatible bug fixes
│   └──── Minor: backward-c
```

## 🚀 15. .gitignore

- Why it exists
- Patterns
- Files/directories
- Environment files
- node_modules
- Build output
- OS/editor files
- Common mistakes

### Footnote — `.gitignore`

**What is `.gitignore`?**
`.gitignore` is a repository-level file that tells Git which **untracked files and directories should normally be ignored**.

It is commonly used for files that should remain on a developer's machine but should not become part of the repository, such as:

- Secrets and credentials
- Environment files
- Dependencies such as `node_modules/`
- Build output
- Temporary files
- IDE/editor files
- Operating-system-generated files
- Local development artifacts

**Why use `.gitignore`?**
A project usually contains files that are necessary for one developer's local environment but should not be committed to the shared repository.

For example:

```text id="p5x8zr"
.env
node_modules/
dist/
*.log
```

This keeps the repository cleaner and prevents accidental commits of files that do not belong in source control.

**What we practiced:**

Initially the repository contained:

```text id="r2k6qm"
GITSYLLABUS.md
```

in `.gitignore`.

We then added:

```text id="x7n4cs"
secret.txt
practice-secret.txt
```

This allowed us to demonstrate the difference between an **untracked ignored file** and a **file that Git is already tracking**.

**Important behavior — `.gitignore` does not remove already tracked files.**

We demonstrated this with `practice-secret.txt`.

The sequence was:

```text id="v8m3qt"
File exists
    ↓
Git tracks the file
    ↓
Add the file to .gitignore
    ↓
Git continues tracking it
```

Adding a tracked file to `.gitignore` does **not** automatically remove it from Git.

To stop tracking it while keeping the local file:

```bash id="k4q9wp"
git rm --cached practice-secret.txt
```

Then `.gitignore` can prevent it from being tracked again.

The result is:

```text id="m6s2fd"
Repository → file no longer tracked
Local machine → file still exists
.gitignore → prevents it from being added again
```

**What we verified:**

After removing `practice-secret.txt` from the index and committing the `.gitignore` change:

```bash id="c3v7na"
git status --ignored
```

showed the ignored files:

```text id="f1x9qb"
practice-secret.txt
secret.txt
```

This confirmed that Git was ignoring them.

**Important security distinction:**
`.gitignore` is **not a security mechanism**.

If a secret has already been committed and pushed:

```text id="z9r4mk"
Adding it to .gitignore
        ↓
does NOT erase the secret
        ↓
from Git history
```

If a real credential is accidentally exposed, it should be **revoked/rotated immediately**. Depending on the situation, the repository history may also need to be cleaned.

**Useful commands:**

```bash id="u2c8hj"
# Check repository status
git status

# Show ignored files
git status --ignored

# Stop tracking a file but keep the local copy
git rm --cached <file>

# See which ignore rule applies to a file
git check-ignore -v <file>
```

**Mental model:**

> **`.gitignore` tells Git what untracked things to leave alone.**

It does not delete files, does not untrack existing files, and does not erase previously committed secrets.

**Relationship with `.gitattributes`:**

```text id="e5w7kp"
.gitignore
    ↓
What should Git ignore?

.gitattributes
    ↓
How should Git treat tracked files?
```

**Practical rule:**
Create `.gitignore` early in a project and define local-only files before they are accidentally committed.

## 🚀 16. .gitattributes

- What it does
- Line endings
- File attributes
- Why teams use it
- Practical awareness

### Footnote — `.gitattributes`

**What is `.gitattributes`?**
`.gitattributes` is a Git configuration file stored inside a repository that defines **how Git should treat particular files or paths**.

It can control things such as:

- Line-ending behavior
- Text vs binary classification
- Git LFS tracking
- Diff behavior
- Merge behavior
- File-specific Git attributes

**Why is it important?**
Different operating systems can use different line-ending conventions.

For example:

```text id="q1s8pz"
Windows → CRLF
Linux/macOS → LF
```

Without an agreed policy, a file can appear to have many changed lines simply because its line endings changed.

`.gitattributes` allows a project to define a consistent repository-level policy.

**What we configured:**

```text id="z6r3kx"
* text=auto
*.txt text eol=lf
```

Meaning:

- `* text=auto` → Git automatically determines whether files should be treated as text.
- `*.txt text eol=lf` → `.txt` files are treated as text and normalized to LF line endings.

This is especially useful when a project is developed across Windows, Linux, and macOS.

**What we practiced:**

1. Checked that the repository did not initially have `.gitattributes`.
2. Created `.gitattributes`.
3. Added text and line-ending rules.
4. Committed the file to the repository.
5. Later added the Git LFS rule to the same file:

   ```text id="w5r2nc"
   *.zip filter=lfs diff=lfs merge=lfs -text
   ```

This demonstrated that `.gitattributes` can control **different Git behaviors for different file types**.

**Relationship with `.gitignore`:**

These two files solve different problems:

```text id="p7k4mz"
.gitignore
    ↓
Which untracked files should Git ignore?

.gitattributes
    ↓
How should Git treat tracked files?
```

Example:

```text id="h4m9vx"
.gitignore
*.log
```

means Git should normally ignore matching untracked log files.

Whereas:

```text id="n2c6wd"
*.txt text eol=lf
```

means Git should treat tracked `.txt` files as text and normalize their line endings.

**Important:**
`.gitattributes` does **not** determine whether a file is tracked or ignored. That is primarily the role of `.gitignore`.

**Useful commands:**

```bash id="a8k3qf"
# Check the attributes applied to a file
git check-attr -a -- path/to/file

# Inspect the .gitattributes file
cat .gitattributes

# Check repository status
git status
```

**Mental model:**
**`.gitignore` controls what Git ignores; `.gitattributes` controls how Git treats files it knows about.**

**Practical rule:**
`.gitattributes` is especially valuable in shared repositories because the rules travel with the project and apply consistently to other contributors' clones.

## 🚀 17. Git LFS

- What it is
- Why large files are a problem
- When LFS is appropriate
- Basic usage
- When you don't need it

### Footnote — Git LFS

**What is Git LFS?**
Git LFS (Large File Storage) is a Git extension designed to handle large binary files more efficiently than storing their full contents directly in the normal Git repository.

Typical examples include:

- Large images
- Videos
- Audio files
- ZIP/archives
- Design files
- Other large binary assets

**Why use Git LFS?**
Normal Git stores the contents of every committed version of a file in the repository's history. Large binary files can therefore make a repository unnecessarily large and slow.

Git LFS changes this model:

```text
Normal Git
Large file
    ↓
Git repository stores the file contents
    ↓
Repository history becomes large


Git LFS
Large file
    ↓
Git stores a small pointer
    ↓
Actual file → LFS storage
```

**The LFS pointer**
When a file is tracked by LFS, Git does not store the actual binary contents in the normal Git object database. Instead, the repository contains a small pointer file containing information such as:

```text id="z5a3qk"
version https://git-lfs.github.com/spec/v1
oid sha256:<object-hash>
size <file-size>
```

The `oid` identifies the actual object stored by LFS.

**What we practiced:**

1. Verified Git LFS installation:

   ```bash
   git lfs --version
   ```

2. Initialized Git LFS:

   ```bash
   git lfs install
   ```

3. Configured ZIP files to use LFS:

   ```bash
   git lfs track "*.zip"
   ```

4. Git automatically updated `.gitattributes`:

   ```text id="8y7n2c"
   *.zip filter=lfs diff=lfs merge=lfs -text
   ```

5. Created a ZIP file for practice.

6. Added the ZIP file to Git:

   ```bash
   git add practice.zip
   ```

7. Verified that Git was tracking it through LFS:

   ```bash
   git lfs ls-files
   ```

8. Inspected the staged version and confirmed that Git stored an LFS pointer rather than the complete ZIP contents.

9. Committed the LFS-tracked file.

10. Pushed the repository and confirmed that the LFS object was uploaded successfully.

**Important file: `.gitattributes`**

Git LFS tracking rules are stored in `.gitattributes`.

Example:

```text id="5j8w2r"
*.zip filter=lfs diff=lfs merge=lfs -text
```

This tells Git:

> Files matching `*.zip` should be handled through Git LFS.

Therefore `.gitattributes` should normally be committed and shared with the repository.

**Useful commands:**

```bash id="4s6m1p"
# Check LFS version
git lfs --version

# Initialize LFS
git lfs install

# Track a file pattern
git lfs track "*.zip"

# Show LFS-tracked files
git lfs ls-files

# Show tracked patterns
git lfs track

# Fetch LFS objects
git lfs fetch

# Download LFS content
git lfs pull
```

**Important distinction:**
Git LFS is **not a replacement for Git**. Git still manages commits, branches, history, and repository metadata. LFS handles the storage of selected large files.

**When to use LFS:**
Use it when large binary files would unnecessarily inflate the normal Git repository—for example, large media, archives, or design assets.

Do **not** normally use LFS for ordinary source files such as `.js`, `.ts`, `.jsx`, `.json`, or `.md`.

**Mental model:**
**Git tracks the file reference → Git LFS stores the large binary object → `.gitattributes` tells Git which files use LFS.**

**Security/maintenance note:**
Git LFS does not encrypt files or make sensitive files safe to commit. Do not use LFS as a method for hiding secrets.

## 🚀 18. Signing

- Signed commits
- Signed tags
- Why signing exists
- Trust/authenticity
- Practical awareness

### Footnote — GPG Signing

**What is GPG?**
GPG (GNU Privacy Guard) is an implementation of OpenPGP used for cryptographic signing, verification, encryption, and identity-related security tasks. In Git, we use it primarily to **sign commits**.

**Why sign Git commits?**
A normal Git commit contains author information such as name and email, but that information alone does not cryptographically prove who created the commit. GPG signing adds a cryptographic signature to the commit.

**How the process works:**

```text
GPG key pair
    │
    ├── Private key → kept secret → signs the commit
    │
    └── Public key  → shared → verifies the signature
                              │
                              ↓
                           GitHub
                              │
                              ↓
                         "Verified"
```

**Private key vs public key:**

- **Private key:** stays on the developer's computer and must never be shared.
- **Public key:** can be shared with GitHub and others so they can verify signatures.
- **Passphrase:** protects access to the private key.

**What we configured:**

```bash
git config --global user.signingkey <KEY-ID>
git config --global commit.gpgsign true
```

This means Git automatically asks GPG to sign new commits.

**What we practiced:**

1. Verified GPG installation.
2. Generated an RSA 3072-bit GPG key.
3. Configured Git to use the key.
4. Enabled automatic commit signing.
5. Created a signed commit.
6. Verified the signature locally with:

   ```bash
   git log -1 --show-signature
   ```

7. Exported the public key.
8. Added the public key to GitHub.
9. Pushed the signed commit.
10. Confirmed GitHub displayed **Verified**.

**Important distinction:**
GPG signing does **not** mean the code is correct, secure, or trustworthy. It verifies that the commit carries a valid cryptographic signature corresponding to the public key registered for the account.

**Useful commands:**

```bash
# List secret keys
gpg --list-secret-keys --keyid-format=long

# Generate a key
gpg --full-generate-key

# Configure Git signing
git config --global user.signingkey <KEY-ID>
git config --global commit.gpgsign true

# Show signature on latest commit
git log -1 --show-signature

# Export public key
gpg --armor --export <KEY-ID>
```

**Mental model:**
**Private key signs → public key verifies → GitHub confirms the signature → Verified.**

**Security rule:**
Never share the private key, private-key file, or GPG passphrase. The public key is the part intended for sharing.

## 🚀 19. Git Hooks

- What hooks are
- Client-side hooks
- Server-side hooks
- Common use cases
- Relationship to quality checks/CI
- Practical awareness

## 🚀 20. Submodules

- What they are
- Why they exist
- Add/update/remove
- Clone with submodules
- Common problems
- When to use them
- Practical awareness

## 🚀 21. Advanced Remote Git

- Remote branches
- Fetching
- Tracking
- Upstream
- Multiple remotes
- Remote management
- Synchronization
- Divergence
- Practical remote troubleshooting

## 🚀 22. Recovery & Troubleshooting ⭐

- Reflog
- Recover deleted commits
- Recover after reset
- Recover after rebase
- Detached HEAD
- Wrong branch
- Wrong commit
- Merge gone wrong
- Rebase gone wrong
- Diverged branches
- Lost-looking work
- Common Git errors
- Recovery methodology

## 🚀 23. Git + CI/CD

Already learned separately, but we'll connect the pieces:

Git commit
     ↓
Git push
     ↓
GitHub
     ↓
CI
     ↓
Tests
     ↓
Build
     ↓
Docker
     ↓
Deployment

## 🚀 24. Professional Team Simulation

We'll finish by operating git-demo like a real development repository:

Fork / Clone
      ↓
Feature branch
      ↓
Development
      ↓
Commits
      ↓
Push
      ↓
Pull Request
      ↓
Review
      ↓
Changes
      ↓
Merge
      ↓
Sync
      ↓
Next feature

And we'll deliberately introduce problems and recover from them.

🎯 Final boundary

After this, your Git knowledge should cover:

Local Git + GitHub + collaboration + branching + merging + conflicts + remote work + PRs + fork workflow + undo + rebase + stash + cherry-pick + tags + recovery + professional workflow.

That is solid full-stack developer Git.

We won't turn this into Git administration or Git internals research.

Syllabus locked. git-demo remains the project. Phase 0 is next.

Quick setup — if you’ve done this kind of thing before
or
https://github.com/bishwajit1965/git-demo.git
Get started by creating a new file or uploading an existing file. We recommend every repository include a README, LICENSE, and .gitignore.

…or create a new repository on the command line
echo "# git-demo" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/bishwajit1965/git-demo.git
git push -u origin main

…or push an existing repository from the command line
git remote add origin https://github.com/bishwajit1965/git-demo.git
git branch -M main
git push -u origin main


Fetch practice
