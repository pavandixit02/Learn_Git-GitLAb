# 🚀 GitLab Learning & DevOps Practice

A structured learning repository for understanding **GitLab, GitLab CI/CD, Runners, SSH authentication, Groups, Projects, Branching, Merging, and DevOps workflows**.

This repository contains practical notes, examples, commands, and HTML-based learning resources that I am creating while learning **GitLab and DevOps**.

---

## 📚 About This Project

The goal of this project is to learn GitLab from **beginner to intermediate level** through practical implementation.

Instead of only reading theory, I am creating individual HTML notes for each important GitLab topic so that I can:

- Understand GitLab concepts clearly
- Practice Git and GitLab commands
- Learn GitLab repository management
- Understand branching and merging
- Learn GitLab CI/CD
- Understand GitLab Runners
- Build practical DevOps knowledge
- Maintain a personal DevOps learning portfolio

---

## 🗂️ Project Structure

```text
.
├── branchs
│   └── create-merge.html
│
├── GitLab-Intro
│   └── introducation.html
│
├── groups-project
│   └── groups-projects.html
│
├── Runner GitLab
│   └── runner.html
│
└── ssh-key
    └── add-ssh-key.html
```

---

## 📖 Topics Covered

### 1. GitLab Introduction

📁 `GitLab-Intro/`

File:

```text
introducation.html
```

Topics covered:

- What is GitLab?
- Why GitLab is used
- Git vs GitLab
- GitHub vs GitLab
- GitLab features
- GitLab account creation
- GitLab interface
- GitLab repositories/projects
- GitLab in DevOps
- Basic GitLab workflow

---

### 2. SSH Key with GitLab

📁 `ssh-key/`

File:

```text
add-ssh-key.html
```

Topics covered:

- What is SSH?
- Why SSH is used with GitLab
- SSH vs HTTPS
- Public and private keys
- SSH key generation
- Adding SSH key to GitLab
- Testing SSH connection
- Using GitLab with SSH
- Common SSH errors
- SSH security best practices

Example:

```bash
ssh-keygen -t ed25519 -C "your-email@example.com"
```

Test connection:

```bash
ssh -T git@gitlab.com
```

---

### 3. GitLab Groups & Projects

📁 `groups-project/`

File:

```text
groups-projects.html
```

Topics covered:

- What is a GitLab Group?
- What is a Subgroup?
- What is a GitLab Project?
- Group vs Project
- Multiple projects inside a group
- Repository management
- Project visibility
- Private / Internal / Public projects
- Creating a GitLab project
- Connecting local Git repository with GitLab
- Pushing code to GitLab

Example:

```bash
git init
git add .
git commit -m "Initial commit"

git branch -M main

git remote add origin git@gitlab.com:USERNAME/PROJECT.git

git push -u origin main
```

---

### 4. Git Branch & Merge

📁 `branchs/`

File:

```text
create-merge.html
```

Topics covered:

- What is a Git branch?
- Why branches are used
- Creating branches
- Switching branches
- Feature branches
- Merging branches
- Fast-forward merge
- Three-way merge
- Merge conflicts
- Conflict resolution
- GitLab Merge Requests
- Branch naming conventions
- Branch deletion

Example:

```bash
git switch -c feature-login
```

Switch to main:

```bash
git switch main
```

Merge:

```bash
git merge feature-login
```

Push:

```bash
git push origin main
```

---

### 5. GitLab Runners

📁 `Runner GitLab/`

File:

```text
runner.html
```

Topics covered:

- What is a GitLab Runner?
- Why GitLab Runner is required
- How GitLab Runner works
- GitLab CI/CD architecture
- Runner types
- Instance / Shared Runner
- Group Runner
- Project-specific Runner
- GitLab-hosted runners
- Self-managed runners
- Runner executors
- Shell executor
- Docker executor
- Kubernetes executor
- SSH executor
- Runner tags
- Runner security
- Runner troubleshooting

Basic architecture:

```text
Developer
    │
    ▼
GitLab Repository
    │
    ▼
.gitlab-ci.yml
    │
    ▼
GitLab CI/CD Pipeline
    │
    ▼
GitLab Runner
    │
    ▼
Executor
    │
    ├── Shell
    ├── Docker
    ├── Kubernetes
    └── SSH
    │
    ▼
Application Build / Test / Deploy
```

---

# 🛠️ Technologies & Tools

This project focuses on technologies commonly used in DevOps:

- Git
- GitLab
- GitLab CI/CD
- GitLab Runners
- SSH
- Linux
- Bash
- Docker
- Kubernetes
- CI/CD
- DevOps
- Version Control

---

# 🔄 GitLab Learning Workflow

My learning workflow for this project is:

```text
Learn Concept
     │
     ▼
Understand Theory
     │
     ▼
Practice Commands
     │
     ▼
Create Example
     │
     ▼
Create HTML Notes
     │
     ▼
Push to GitLab
     │
     ▼
Review & Improve
```

---

# 🎯 Learning Goals

The main objectives of this repository are:

- [x] Understand GitLab fundamentals
- [x] Understand GitLab Groups and Projects
- [x] Configure SSH authentication
- [x] Understand Git branching
- [x] Understand Git merging
- [x] Learn GitLab Runners
- [ ] Learn GitLab CI/CD
- [ ] Learn `.gitlab-ci.yml`
- [ ] Learn Pipelines
- [ ] Learn Jobs and Stages
- [ ] Learn CI/CD Variables
- [ ] Learn Artifacts and Cache
- [ ] Learn Environments
- [ ] Learn Deployment
- [ ] Learn Docker with GitLab CI/CD
- [ ] Build complete CI/CD projects

---

# 🚀 Upcoming Topics

The repository will gradually be expanded with more GitLab and DevOps topics.

### GitLab CI/CD

- GitLab CI/CD Introduction
- `.gitlab-ci.yml`
- Jobs
- Stages
- Pipelines
- Pipeline workflow
- Variables
- Predefined variables
- Secrets
- Artifacts
- Cache
- Dependencies
- Rules
- Conditions
- Manual jobs
- Scheduled pipelines
- Pipeline triggers

### GitLab Runner

- Runner installation
- Runner registration
- Runner configuration
- Runner tags
- Docker Runner
- Shell Runner
- Kubernetes Runner
- Runner security
- Runner troubleshooting

### Deployment

- CI/CD deployment
- Docker deployment
- Linux server deployment
- SSH deployment
- Environment management
- Development environment
- Staging environment
- Production environment

---

# 💻 Example GitLab Workflow

A typical development workflow:

```text
                    GitLab
                      │
                      ▼
                Main Repository
                      │
          ┌───────────┴───────────┐
          │                       │
          ▼                       ▼
    feature/login           feature/payment
          │                       │
          ▼                       ▼
       Coding                  Coding
          │                       │
          ▼                       ▼
        Commit                  Commit
          │                       │
          ▼                       ▼
         Push                    Push
          │                       │
          └───────────┬───────────┘
                      ▼
               Merge Request
                      │
                      ▼
                 CI/CD Pipeline
                      │
                      ▼
                  GitLab Runner
                      │
                      ▼
             Build → Test → Deploy
                      │
                      ▼
                     main
```

---

# 📌 Important Git Commands

Check repository status:

```bash
git status
```

Check branches:

```bash
git branch
```

Create a branch:

```bash
git switch -c feature-name
```

Switch branch:

```bash
git switch main
```

Add files:

```bash
git add .
```

Commit:

```bash
git commit -m "Add new GitLab notes"
```

Push:

```bash
git push -u origin main
```

Pull:

```bash
git pull origin main
```

Fetch:

```bash
git fetch origin
```

Merge:

```bash
git merge feature-name
```

Check remote:

```bash
git remote -v
```

---

# 🔐 Security Practices

While working with Git and GitLab, sensitive information should never be committed to the repository.

Do **NOT** commit:

```text
.env
.env.*
*.pem
*.key
id_rsa
id_ed25519
passwords
API keys
Access tokens
Cloud credentials
AWS credentials
Private SSH keys
```

Use `.gitignore` to prevent accidental commits.

Example:

```gitignore
.env
.venv/
__pycache__/
node_modules/
*.log
*.pem
*.key
```

---

# 🧪 Practical Learning

This repository is not only theoretical.

For every major topic, I try to follow:

```text
Theory
   ↓
Command
   ↓
Practical Example
   ↓
GitLab Implementation
   ↓
Documentation
   ↓
Troubleshooting
```

This approach helps me develop practical DevOps skills rather than only memorizing commands.

---

# 📈 DevOps Learning Path

My broader DevOps learning journey includes:

```text
Linux
  ↓
Git & GitLab
  ↓
GitLab CI/CD
  ↓
Docker
  ↓
Kubernetes
  ↓
Terraform
  ↓
Jenkins
  ↓
Cloud
  ↓
Monitoring
  ↓
Security
  ↓
DevOps / Cloud Projects
```

---

# 👨‍💻 Author

**Pavan Kumar Dixit**

BCA Graduate | RHCSA | RHCE | Cloud & DevOps Learner

### Areas of Learning

- DevOps
- Cloud Computing
- Linux
- Git & GitLab
- CI/CD
- Docker
- Kubernetes
- Infrastructure as Code
- Automation
- Python for DevOps

---

# ⭐ Repository Purpose

This repository represents my **hands-on GitLab and DevOps learning journey**.

I am continuously adding new topics, practical examples, commands, projects, and documentation as I progress from beginner to job-ready DevOps professional.

If you are also learning GitLab or DevOps, feel free to explore the notes and examples.

---

## 📜 License

This project is created for **learning, practice, and educational purposes**.

---

**Learning → Practicing → Building → Documenting → Improving 🚀**