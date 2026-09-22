# 📌 FINAL GIT SYLLABUS QUESTIONNAIRE — LOCKED

## 1. Git Fundamentals ✅

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

## 2. Git History ✅

- Log
- Show
- Commit hashes
- HEAD
- Parent commits
- Comparing commits
- History inspection
- Commit messages
- Amend

## 3. Git Branching ✅

- Branch concept
- Create branch
- Switch branch
- Rename branch
- Delete branch
- Branch listing
- Branch pointers
- Tracking branches
- Feature branches

## 4. Merge ✅

- Fast-forward merge
- Three-way merge
- Merge
- Merge conflicts
- Conflict markers
- Conflict resolution
- Abort merge
- Merge history

## 5. Git Workflow ✅

- Working with branches
- Feature workflow
- Main/development concepts
- Best practices
- Clean commits
- Team conventions

## 6.GitHub & Remote Repositories ✅

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

## 7. GitHub Authentication

- HTTPS
- SSH
- SSH keys
- Add SSH key to GitHub
- Test authentication
- Secure authentication practices

## 8. Forking & Collaboration / Contribution ⭐ ✅

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

## 9. Pull Requests ✅

- Create PR
- PR branches
- Review
- Review comments
- Requested changes
- Update PR
- Merge PR
- Delete feature branch
- Keep local repository synchronized

## 10. Undo & Modification

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

## 11. Rebase ✅

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

## 12. Stash ✅

- Why stash
- Create stash
- List stash
- Apply
- Pop
- Drop
- Clear
- Stashing specific work
- Practical use cases

## FOOT NOTE ON stash

-----------------------------------------------------
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

-----------------------------------------------------

stash        → save
list         → see
apply        → restore + keep
pop          → restore + remove

-----------------------------------------------------

## 13. Cherry-pick & Patch

- Cherry-pick
- Selective commit application
- Cherry-pick conflicts
- Abort/continue
- Patch concepts
- When useful

## 14. Tags & Releases

- Tags
- Lightweight tags
- Annotated tags
- Create/delete tags
- List tags
- Push tags
- Versioning
- Release workflow

## 15. .gitignore

- Why it exists
- Patterns
- Files/directories
- Environment files
- node_modules
- Build output
- OS/editor files
- Common mistakes

## 16. .gitattributes

- What it does
- Line endings
- File attributes
- Why teams use it
- Practical awareness

## 17. Git LFS

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

## 20. Submodules

- What they are
- Why they exist
- Add/update/remove
- Clone with submodules
- Common problems
- When to use them
- Practical awareness

## 21. Advanced Remote Git

- Remote branches
- Fetching
- Tracking
- Upstream
- Multiple remotes
- Remote management
- Synchronization
- Divergence
- Practical remote troubleshooting

## 22. Recovery & Troubleshooting ⭐

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

## 23. Git + CI/CD

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

## 24. Professional Team Simulation

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
