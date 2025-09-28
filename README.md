Version-Controlled DevOps Project with Git
1. Objective
The primary goal of this project is to demonstrate a practical understanding of Git and GitHub for managing a simple DevOps project. It covers essential version control workflows, including repository initialization, strategic branching, merging through pull requests, and proper project documentation. This serves as a foundational exercise in applying Git best practices.

2. Tools Used
Git: For local version control, including branching, committing, and merging.

GitHub: As the central remote repository for collaboration, code hosting, and managing pull requests.

3. Git Workflow and Branching Strategy
This project adheres to a structured Git workflow to ensure a clean and manageable codebase. Our branching strategy is as follows:

main Branch: This branch represents the stable, production-ready code. Direct commits to main are restricted. Merges into main only happen from the dev branch after thorough review and testing.

dev (Development) Branch: This is the primary development branch where all completed features are integrated. It serves as a staging area before features are released to main.

feature/* Branches: All new features or bug fixes are developed in separate feature branches. These are branched off from dev. For example, a new feature for user authentication would be developed in a branch named feature/user-authentication. This isolates work-in-progress and prevents destabilizing the dev branch.

Workflow Diagram
main <--- (Pull Request) <--- dev <--- (Pull Request) <--- feature/new-feature

4. Project Setup and Execution
a. Initialize Repo and Push to GitHub
The project was started by creating a local Git repository and linking it to a remote repository on GitHub.

# Initialize a new Git repository locally
git init

# Add a remote origin pointing to the GitHub repository
git remote add origin <your-github-repo-url>

# Create an initial commit and push the main branch
git add .
git commit -m "Initial commit: Project setup"
git push -u origin main

b. Create dev and feature Branches
The dev branch was created from main, and a sample feature branch was created from dev.

# Create and switch to the dev branch from main
git checkout -b dev main

# Push the dev branch to the remote repository
git push -u origin dev

# Create a feature branch from dev for a new feature
git checkout -b feature/initial-readme dev

c. Use Pull Requests to Merge
All merges into dev and main are handled exclusively through Pull Requests (PRs) on GitHub. This practice enables code review, discussion, and automated checks before code is integrated.

Process:

Push the feature branch to GitHub (git push origin feature/initial-readme).

Navigate to the GitHub repository and open a new Pull Request.

Set the base branch to dev and the compare branch to feature/initial-readme.

Add a descriptive title and summary for the changes.

Assign reviewers (if applicable).

Once approved, merge the PR into dev.

Delete the feature branch after a successful merge.

d. Add a Proper README.md
This README.md file was created to provide comprehensive documentation for the project, its structure, and its processes. It is written in Markdown for clear formatting.

e. Use .gitignore
A .gitignore file is included in the root of the repository to prevent tracking of unnecessary files and directories. This keeps the repository clean and lightweight.

Example .gitignore content:

# IDE and editor files
.vscode/
.idea/

# Dependency directories
node_modules/

# Environment variables
.env

# Build outputs
dist/
build/

f. Use Tags for Versioning
Git tags are used to mark specific points in the repository's history as important, typically for version releases.

# Tag the first stable release on the main branch
git tag -a v1.0.0 -m "Version 1.0.0: Initial stable release"

# Push the tag to the remote repository
git push origin v1.0.0

5. Summary of Tasks
[x] Initialized a new Git repository.

[x] Pushed the initial project structure to a remote GitHub repository.

[x] Implemented the main, dev, and feature branching strategy.

[x] Created a .gitignore file to exclude unnecessary files.

[x] Developed a feature (this README) in a feature/initial-readme branch.

[x] Merged the feature into dev using a Pull Request.

[x] Merged the dev branch into main to simulate a release.

[x] Created a version tag v1.0.0 on the main branch.

[x] Documented all steps and processes within this README.md file.