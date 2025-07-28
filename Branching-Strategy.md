# 📌 Branching Strategy 

## 🔖 Overview
This document outlines the Git branching strategy adopted for this technical assessment. It demonstrates how a collaborative team can manage code changes efficiently using GitHub's version control features such as branches, pull requests (PRs), and code reviews.

---

## 🌿 Branching Model

We follow a simplified version of **GitHub Flow**, which is widely adopted for continuous integration and delivery. The structure ensures:
- Isolation of new features
- Safe integration into the `main` branch
- Traceability of all changes

### 🗂 Branch Types

| Branch Name Pattern      | Purpose                                  |
|--------------------------|-------------------------------------------|
| `main`                   | Stable, production-ready code             |
| `feature/<task-name>`    | New features or tasks under development   |
| `hotfix/<issue>`         | Emergency fixes applied directly to main  |
| `release/<version>`      | Optional: Prepare code for production     |

---

## 🔁 Git Workflow

### 1. Create a Repository
A new GitHub repository named `devops-challenge` was created for this assignment.

### 2. Clone the Repository
```bash
git clone https://github.com/<username>/devops-challenge.git
cd devops-challenge
