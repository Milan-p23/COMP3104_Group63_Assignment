# COMP3104_Group63_Assignment

## Group Members
- **Leader:** Milan Patel (101397631) - [GitHub Profile](https://github.com/Milan-p23)
- **Member 1:** Parthkumar Patel (101399114) - [GitHub Profile](https://github.com/Parth-2601)
- **Member 2:** Deep Patel (101415117) - [GitHub Profile](https://github.com/Deeppatel91)
- **Member 3:** Neeraj Kumar (1011415118) - [GitHub Profile](https://github.com/NeerajBudhiraja1807)
- **Member 4:** Mohmadsahil Shaikh (101413469) - [GitHub Profile](https://github.com/sahils777)

## Project Description
This repository contains the group assignment for the COMP3104 DevOps course. The assignment focuses on collaborative Git workflows, branching strategies, and CI/CD integration using GitHub Actions. Each member contributes to the project through individual branches that are later merged into the main branch, ensuring continuous integration and collaboration.

## Objectives
- Implement Git branching strategies and best practices.
- Set up continuous integration (CI) using GitHub Actions.
- Maintain version control and collaboration using Git and GitHub.
- Demonstrate teamwork through commits, pull requests, and merging.

## Getting Started
To get a local copy of the project, clone the repository using the following command:

```bash
git clone https://github.com/Milan-p23/COMP3104_Group63_Assignment.git

```

# Setup Instructions

## Prerequisites
1. **Install Git:** Ensure that Git is installed on your machine. You can download it from [git-scm.com](https://git-scm.com).

## Cloning the Repository
1. **Clone this Repository:** Open your terminal (or command prompt) and run the following command to clone the repository to your local machine:
   ```bash
   git clone https://github.com/Milan-p23/COMP3104_Group63_Assignment.git

## Navigate to the Project Directory
Change into the project directory:
   ```bash
   cd COMP3104_Group63_Assignment
   ```


## Creating a Personal Branch
Create Your Personal Branch: Each member should create a personal branch using the naming convention `STUDENTID-Name`. Run the following command, replacing `STUDENTID` and `Name` with your actual student ID and name:
  ```bash
 git checkout -b STUDENTID-Name

```
## Working on Your Branch
1. **Make Changes or Add New Files:** Modify existing files or add new files as needed for the project.
2. **Stage and Commit Your Changes:** After making your changes, stage and commit them with clear commit messages:
   ```bash
   git add .
   git commit -m "Your Meaningful commit message"
   git push -u origin STUDENTID-Name
## Merging to Main
1. **Create a Pull Request (PR):** After pushing your branch, go to the GitHub repository page, and you will see an option to create a pull request. Click on "Compare & pull request."

2. **Review Process:**
   - Other members or the team leader will review the pull request. Make sure to address any comments or requested changes before merging.

3. **Resolve Merge Conflicts:**
   - If there are merge conflicts, resolve them locally by checking out the main branch, pulling the latest changes, and then merging your branch back into the main branch. Follow these commands:
   ```bash
   git checkout main
   git pull origin main
   git checkout STUDENTID-Name
   git merge main
## Resolving Merge Conflicts
- Resolve any conflicts that arise, then stage and commit the resolved files:
  ```bash
  git add .
  git commit -m "Resolved merge conflicts"
  git push
  ```
  
## Finalize the Merge
Once the PR is approved, it can be merged into the main branch.

## Final Notes
- Always ensure to keep your branch updated by regularly pulling from the main branch to avoid conflicts.
- Use meaningful commit messages to make it easier for others to understand your changes.

# CI/CD Pipeline

This repository is integrated with GitHub Actions to automate testing and builds on every push event. The CI/CD pipeline is defined in the .github/workflows/ci.yml file and includes the following steps:

1. *Clone the Repository*: The pipeline checks out the code from the repository.
2. *Set Up the Environment*: It sets up the environment on an Ubuntu server.
3. *Run Basic Checks*: The pipeline runs checks on branch changes, including file integrity and repository structure.
4. *Display Job Statuses*: Job statuses and relevant outputs are displayed.

This automation ensures that code pushed to the repository is automatically validated through continuous integration, improving code quality and collaboration.

## GitHub Actions CI Workflow

The GitHub Actions workflow is designed to trigger automatically on every push to any branch, helping maintain a functional, conflict-free repository. Below is an example configuration found in the .github/workflows/ci.yml file:

yaml
name: GitHub Actions CI
```
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Run CI Pipeline
        run: |
          echo "CI pipeline triggered for ${GITHUB_REF}"
          # Add additional commands for testing and building the project.
```

## How It Works

- *Triggering the Workflow*: The workflow is automatically triggered by a push event to any branch.
- *Running on Ubuntu*: The pipeline runs on the latest version of Ubuntu.
- *Checkout Action*: The actions/checkout@v4 action is used to check out the repository code.
- *CI Pipeline Execution*: The pipeline runs and outputs a message that includes the reference of the triggered event.

## Customization

You can customize the workflow by adding commands in the run section to include specific testing, linting, or build commands necessary for your project.

## Branching Strategy

Each member of the group is required to work on a separate branch, named following the convention STUDENTID-Name. This ensures that all changes are tracked separately before being merged into the main branch through pull requests. The leader and collaborators will review and approve each pull request (PR) before merging.

### Branches:
- *101397631-Milan:* Leader’s branch.
- *101399114-Parth:* Member 1's branch.
- *101415117-Deep:* Member 2's branch.
- *101413469-Sahil:* Member 3's branch.
- *101415118-Neeraj:* Member 4's branch.

#### Contribution Guide
- All members are expected to contribute with at least 10 commits, each with meaningful messages.
- Every member should create three files as outlined in the assignment.
- Ensure you follow the proper Git workflow to avoid merge conflicts.
- Regularly pull changes from the main branch to your own branch to stay up-to-date:
- bash

