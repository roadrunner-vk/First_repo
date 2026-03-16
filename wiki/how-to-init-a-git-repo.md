# How to Create and Initialise a Git Repo 🐣

## What is Git? (Simple version)

Imagine you are drawing a picture. Git is like a **magic notebook** that remembers **every single change** you make to your drawing. So if you mess up, you can go back to how it looked before. Cool, right?

A **repository (repo)** is just a folder where Git watches and remembers all your changes.

---

## Step 1 — Make sure Git is installed

Open a terminal (PowerShell or Command Prompt) and type:

```bash
git --version
```

If you see something like `git version 2.x.x`, you're good to go!
If not, download Git from [git-scm.com](https://git-scm.com) and install it.

---

## Step 2 — Go to your folder

Navigate to the folder you want to turn into a repo. For example:

```bash
cd "C:\Users\YourName\Documents\MY_REPOSITORIES\First_repo"
```

Think of this like walking into the room where your drawing is kept.

---

## Step 3 — Initialise the repo

Now tell Git to start watching this folder:

```bash
git init
```

You will see a message like:

```
Initialized empty Git repository in .../First_repo/.git/
```

Git has now created a hidden folder called `.git` inside your folder. That's where Git stores all its magic memory.

---

## Step 4 — Check it worked

Run:

```bash
git status
```

If you see **"On branch master"** or **"On branch main"**, it worked! Git is now watching your folder.

---

## Step 5 — Stage your files

Before Git can save your work, you need to tell it **which files** to include. This is called **staging**.

```bash
git add .
```

The `.` means "add everything in this folder". Think of it like putting all your drawings into an envelope before sealing it.

You can check what's been staged by running `git status` again.

---

## Step 6 — Make your first commit

A **commit** is like sealing that envelope and writing a note on the front describing what's inside.

```bash
git commit -m "Initial commit"
```

The `-m` flag lets you write a short message explaining what changed. Always write something meaningful!

---

## Step 8 — Create a new repo on GitHub

1. Go to [github.com](https://github.com) and sign in
2. Click the **"+"** button in the top-right corner → **"New repository"**
3. Give it a name (e.g. `First_repo`)
4. **Do NOT** tick "Add a README", "Add .gitignore" or "Choose a license" — keep it empty so it doesn't conflict with your local repo
5. Click **"Create repository"**

GitHub will show you a page with a URL like:
```
https://github.com/your-username/First_repo.git
```
Copy that URL — you'll need it in the next step.

---

## Step 9 — Link your local repo to GitHub

Tell your local Git repo where GitHub is (called adding a "remote"):

```bash
git remote add origin https://github.com/your-username/First_repo.git
```

Think of `origin` as a nickname for the GitHub address.

---

## Step 10 — Rename your branch to main (recommended)

GitHub uses `main` as the default branch name. To match:

```bash
git branch -M main
```

---

## Step 11 — Push to GitHub

Now send your local commits up to GitHub:

```bash
git push -u origin main
```

- `-u` sets GitHub as the default place to push/pull from now on
- After this, future pushes are just `git push`

You may be prompted to sign in to GitHub the first time.

---

## Step 12 — Verify it worked

Go to `https://github.com/your-username/First_repo` in your browser — your files should be there! 🎉

---

## Quick Cheat Sheet

| Command | What it does |
|---|---|
| `git init` | Starts a new repo in the current folder |
| `git status` | Shows what has changed |
| `git add .` | Stages all changes (gets them ready to save) |
| `git commit -m "message"` | Saves a snapshot of your work |
| `git remote add origin <url>` | Links local repo to GitHub |
| `git branch -M main` | Renames branch to main |
| `git push -u origin main` | Pushes code to GitHub for the first time |
| `git push` | Pushes subsequent changes to GitHub |
