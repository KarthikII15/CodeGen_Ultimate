# CodeGen_Ultimate

# 🚀 CodeZen CLI  
### Automated Code Analysis & Pull Request Integration

This repository contains the **CodeZen CLI** package along with setup documentation for enabling automated code review, AI-based code analysis, and Pull Request generation workflows.

---

## 📦 Prerequisites

Before using CodeZen CLI, ensure the following are installed:

| Requirement | Description |
|------------|-------------|
| **Python 3.8+** | Required to run the CLI package |
| **Git** | Required for repository and PR automation |
| **CodeZen `.whl` Package** | File named `codezen_cli-xx.xx.x-py3-none-any.whl` placed in the **root folder** |

---

## ⚙️ Installation & Setup (For All Users)

These steps apply to both **Team Leads** and **Developers**.

### 1️⃣ Clone the Repository

git clone <your-repo-url>
cd <repo-name>

# Create virtual environment
python -m venv venv

# Activate (Windows)
.\venv\Scripts\activate

# Activate (Mac/Linux)
source venv/bin/activate

# Install the package
pip install codezen_cli-xx.xx.x-py3-none-any.whl

### Verify Installation
codezen version

🏗 Phase 1: Team Lead Workflow (Run Once Per Repository)

These steps initialize CodeZen integration for the repository.

1️⃣ Configure Backend URL
codezen config --backend https://unflutterable-noncurtailing-jaylin.ngrok-free.dev

2️⃣ Initialize Repository
codezen init

3️⃣ Connect GitHub App

During init, a GitHub authorization URL will be shown:

Click the URL in the terminal.

Install & authorize the CodeZen GitHub App.

Return to the terminal once installation is complete.

👨‍💻 Phase 2: Developer Workflow (Daily Usage)
1️⃣ One-Time Configuration
codezen config --backend https://unflutterable-noncurtailing-jaylin.ngrok-free.dev

2️⃣ Daily Code Analysis & Auto PR

After modifying or adding files:

❌ Do NOT run:

git add
git commit
git push


✔ Instead, run:

codezen analyze
