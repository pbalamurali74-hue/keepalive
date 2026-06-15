# 🟢 Keepalive — GitHub Contribution Streak Active

A lightweight, automated GitHub Action that updates a heartbeat log file daily, ensuring your GitHub contribution streak remains active and green even on days when you don't commit code.

---

## 🚀 How It Works

1. **Daily Trigger**: The workflow is scheduled using GitHub Actions cron syntax to run every day at **18:05 UTC**.
2. **Heartbeat Log**: It appends the current date in UTC (e.g., `2026-06-15 heartbeat`) to the [.keepalive](.keepalive) file.
3. **Automated Commit**: It commits the change and pushes it back to the repository under the name `github-actions[bot]`.
4. **Manual Trigger**: Can also be triggered manually at any time via the **Actions** tab on GitHub (using `workflow_dispatch`).

---

## 🛠️ Setup Instructions

To get this running on your GitHub account, follow these quick steps:

### 1. Create a GitHub Repository
1. Go to [github.com/new](https://github.com/new).
2. Create a new repository (e.g., named `keepalive`).
3. **Important**: Leave it completely empty (do not add a README, license, or `.gitignore` file).

### 2. Push these Files to GitHub
Open your terminal in this directory and run:
```bash
# Link the local repository to your new GitHub repository
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/YOUR_REPO_NAME.git

# Push the commit to the main branch
git push -u origin main
```
*(Remember to replace `YOUR_GITHUB_USERNAME` and `YOUR_REPO_NAME` with your actual GitHub username and the name of the repository you created).*

### 3. Enable Workflow Permissions
By default, GitHub Actions may not have permission to push changes to your repository. To enable this:
1. Navigate to your repository on GitHub.
2. Go to **Settings** > **Actions** > **General**.
3. Scroll down to **Workflow permissions**.
4. Select **Read and write permissions**.
5. Click **Save**.

---

## 📝 Configuration

If you want to change the time the commit is made, edit the cron schedule in [.github/workflows/keep-streak-green.yml](.github/workflows/keep-streak-green.yml):
```yaml
on:
  schedule:
    # Runs at 18:05 UTC everyday. Customize using cron syntax.
    - cron: '5 18 * * *'
```

---

*Keep your contributions green!* 🟢
