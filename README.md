#  Auto Git Commit Bot

The **Auto Git Commit Bot** is a GitHub Actions workflow that automatically updates a file, creates a commit, and pushes the changes back to the repository on a scheduled basis. It can also be triggered manually from the GitHub Actions interface.

This project demonstrates how to automate repetitive Git operations using **GitHub Actions**, making it useful for learning CI/CD, automation, and scheduled workflows.


##  Features

*  Automatic daily commits using a cron schedule
*  Manual workflow execution via GitHub Actions
*  Automatically updates a file with the current date and time
*  Creates a new Git commit when changes are detected
*  Pushes commits directly to the repository
*  Runs entirely on GitHub's cloud runners (no local machine required)


##  Project Structure

```text
Git-Commit-Bot
│
├── .github
│   └── workflows
│       └── auto_commit.yml
│
├── myfile.txt
├── README.md
```


##  How It Works

```text
Scheduled Time (Cron)
          │
          ▼
GitHub Actions starts a runner
          │
          ▼
Checkout Repository
          │
          ▼
Configure Git
          │
          ▼
Update myfile.txt
          │
          ▼
Commit Changes
          │
          ▼
Push to GitHub
          │
          ▼
Workflow Complete
```


##  Technologies Used

* Git
* GitHub
* GitHub Actions
* YAML


##  Workflow Schedule

The workflow is scheduled using a cron expression:

```yaml
schedule:
  - cron: "0 0 * * *"
```

This runs **every day at 00:00 UTC** (approximately **5:30 AM IST**).

The workflow can also be started manually using the **Run workflow** button in the **Actions** tab.


##  Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/Git-Commit-Bot.git
```

### 2. Create the Workflow

Create the following file:

```text
.github/workflows/auto_commit.yml
```

### 3. Add the Workflow

Copy the GitHub Actions workflow into `auto_commit.yml`.

### 4. Enable Workflow Permissions

Go to:

```
Repository
→ Settings
→ Actions
→ General
→ Workflow permissions
```

Select:

* ✅ Read and write permissions
* ✅ Allow GitHub Actions to create and approve pull requests

Save the changes.

### 5. Run the Workflow

Open:

```
Actions
→ Auto Commit Bot
→ Run workflow
```

or wait for the scheduled execution.


##  Learning Outcomes

By building this project, you will learn:

* GitHub Actions fundamentals
* CI/CD workflow automation
* Scheduled jobs using cron expressions
* Git automation (add, commit, push)
* Repository permissions and workflow configuration
* YAML workflow syntax


---

⭐ If you found this project useful, consider giving the repository a **star**.
