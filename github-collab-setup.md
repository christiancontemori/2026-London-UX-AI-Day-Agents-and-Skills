# Setting Up Your Team's Collaborative Workspace

Each team shares one GitHub repository. Everyone connects to it through Claude Code and works from their own local copy.

---

## Step 1 — One person creates the repository

One team member creates the repo on GitHub. Everyone else joins it.

1. Go to [github.com](https://github.com) and sign in (or create a free account if you don't have one)
2. Click the **+** icon in the top right → **New repository**
3. Give it a name — something short and descriptive, e.g. `ux-ai-day-team-3`
4. Set it to **Public** (easiest for sharing) or **Private** (then you'll need to invite members manually)
5. Check **Add a README file** so the repo isn't empty
6. Click **Create repository**

---

## Step 2 — Share the repo with your team

The person who created the repo adds everyone else as collaborators.

1. Go to your new repo on GitHub
2. Click **Settings** → **Collaborators** (in the left sidebar)
3. Click **Add people** and enter each teammate's GitHub username or email
4. They will receive an email invitation — they need to accept it before they can push changes

---

## Step 3 — Each person links Claude Code to the repo

Each team member does this on their own machine.

1. Open **Claude Code** (the desktop app or terminal)
2. Open a terminal in Claude Code and clone the repo:

```bash
git clone https://github.com/<your-username>/<repo-name>.git
```

Replace `<your-username>` and `<repo-name>` with the actual values from your GitHub repo URL.

3. Navigate into the folder:

```bash
cd <repo-name>
```

4. Open that folder in Claude Code — it will now treat this as your working directory

---

## Step 4 — Start adding files and code

Everyone works from their local copy and syncs changes through GitHub.

**Before you start working**, pull the latest changes so you're up to date:

```bash
git pull
```

**After you add or change something**, save it back to the shared repo:

```bash
git add .
git commit -m "describe what you added or changed"
git push
```

**If two people edit the same file at the same time**, Git will flag a conflict. Ask Claude Code to help you resolve it — paste the conflict and it will walk you through it.

---

## Tips for the day

- **Pull often** — before you start a new piece of work, always run `git pull` first
- **Commit small** — push one thing at a time rather than everything at the end; it's easier to untangle if something goes wrong
- **Use clear commit messages** — "added decision calculator" is more useful than "update" when you're reviewing what happened
- **One folder per artifact** — if your team builds more than one thing, keep each in its own folder inside the repo

---

## Quick reference

| What you want to do | Command |
|---|---|
| Get the latest from the team | `git pull` |
| See what files you've changed | `git status` |
| Stage all your changes | `git add .` |
| Save a commit | `git commit -m "your message"` |
| Push to GitHub | `git push` |
