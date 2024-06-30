What is GitHub, and what are its primary functions and features? Explain how it supports collaborative software development.

Github is a version control system for which allow develpers keep track of the changes they make to their code.

Functions

    1. It makes it possible for more than one developer to work on a project.

    2. It also give access to other developers to fork repo and make changes to code without affecting the original repo

    3. It allow developer to solve issues and bugs through the use of branches.

HOW IT SUPPOETS COLLABORATIVE SOFTWARE DEV

    1. The use of comments allow for developers to communicate ideas to one another about a project

    2. Developers can also work on features or bugs using different branches. And once changes are approved, they can be merge to the main branch.



What is a GitHub repository? Describe how to create a new repository and the essential elements that should be included in it.

GITHUB REPOSITORY:  is where a particular project file is stored and managed

HOW TO CREATE A NEW REPO

    1. Click on the + icon at the header of your gihub profile page, then click on 'Create a New Repository'

    2. Then enter the repo name in the field provided

    3. You can include a description of the repo

    4. Select if you want the repo to be public or private

    5. Then click on the button 'Create repository' to finish

ESSENTIAL ELEMENTS IN REPO

    1. README.md file - it provide information about the repository to others - like a description, how to run or use it.

    2. SRC FILES: this is the main source code of the project

    3. License Files and other important Documentations


Explain the concept of version control in the context of Git. How does GitHub enhance version control for developers?

Version Control is a system that record changes made to a set of files over a period of time and make it possible to recall previous version

HOW GITHUB ENHANCE VERSION CONTROL FOR DEVELOPERS

    1. It provide Graphic User Interface (GUI) instead of CLI provided by Git. 

    2. Github forking feature allow other developers to import other repository so experiment with it and also contribute and submit through pull request


What are branches in GitHub, and why are they important? Describe the process of creating a branch, making changes, and merging it back into the main branch.

Branches is a separate workspace apart from the main codespace which allow developers to work on other features, experiments or fix bugs without affecting the main codespace.

IMPORTANCE

    1. It allows developers to experiment or try new ideas without affecting the main project, so if successful, it would be merged to the main project and is otherwise, it would be discard

    2. It enable developers to work on different part of a project simultaneously thereby boosting productivity


HOW TO CREATE A BRANCH USING GIT

    1. Enter the command "git checkout -b new-feature"

    2. To commit changes on the main branch, enter command "git add ." then commit using "git commit -m "new feature""

    3. To merge changes from new branch to main branch; switch the branch using this command "git checkout main"

    4. Then merge using "git merge new-feature"


What is a pull request in GitHub, and how does it facilitate code reviews and collaboration? 
Outline the steps to create and review a pull request.

Pull request allows our code to be pulled into another branch allowing anyone to review our cide, commit on it and ask us to make update

HOW IT FACILITATE CODE REVIEWS AND COLLABORATION

    It allows the team members to review the proposed changes by asking questions, asking for improvements before pull request is approved

    It allows team members to check if it meets up with their code quality and consitency and meets their standards

    It allow for open discussions concerning issues, or features to be added.

Explain what GitHub Actions are and how they can be used to automate workflows. Provide an example of a simple CI/CD pipeline using GitHub Actions.


Github Actions allow for automation of workflows with github repos

HOW IT IS USED TO AUTOMATE WORKFLOWS

    1. Continuous Integration (CI); It automatically build your code when pull requests are made or changes are pushed

    2. Continous Deployment (CD): It deploy application automatically when changes is made to specific branches.

    3. It runs specific analysis tool to maintain code quality and run backups and updates.

Here’s an example of a simple CI/CD pipeline using GitHub Actions for a Node.js project. This pipeline will run tests when code is pushed to the main branch or a pull request is created.

Build and deploy the application when changes are pushed to the main branch.

Step-by-Step Workflow

1.Create a file named .github/workflows/ci-cd.yml in your repository. This YAML file defines the workflow for CI/CD.

        name: CI/CD Pipeline

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Set up Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '14'

      - name: Install dependencies
        run: npm install

      - name: Run tests
        run: npm test

  deploy:
    runs-on: ubuntu-latest
    needs: build
    if: github.ref == 'refs/heads/main'

    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Deploy to Production
        run: |
          echo "Deploying application..."
          # Add your deployment script or commands here


2.Commit the workflow file to your repository and push it to GitHub:

    git add .github/workflows/ci-cd.yml
    git commit -m "Add CI/CD pipeline"
    git push origin main


3.Observe the Workflow
Once pushed, GitHub Actions will automatically trigger the workflow based on the defined events.
You can monitor the workflow's progress, review logs, and view results in the "Actions" tab of your GitHub repository.


What is Visual Studio, and what are its key features? How does it differ from Visual Studio Code?
Visual Studio is an Integrated Development Environment (IDE) developed by Microsoft to develop desktop application, consoles, web and mobile application, GUI.

KEY FEATURES OF VISUAL STUDIO

    1. Allows for collaboration

    2. Allow users to add extensions to IDE

    3. Provide a very good GUI for code editing

    4. It provide powerful debugging process

    5. Works well with Git

    6. Work across different platform

VISUAL STUDIO VS VISUAL STUDIO CODE

    1. Visual studio is bulky in size with VS code is a ligtweight version

    2. To enjoy full features of VS, it comes with a subscription fee with VS Code is free

    3. VS focuses on deployment while VS Code doesn't


Describe the steps to integrate a GitHub repository with Visual Studio. How does this integration enhance the development workflow?

INTEGRATION

    1.Visit the GitHub for Visual Studio site.

    2.Click the Download GitHub Extension for Visual Studio button.

    3.In your computer's Downloads folder, double-click GitHub.VisualStudio.vsix.

    4.In the pop-up window, click Install.

    5.After the installation is completed, run Visual Studio.

    -- SOURCE: https://github.com/github/VisualStudio/blob/master/docs/getting-started/installing-github-for-visual-studio.md

HOW INTEGRATION ENHANCE THE DEVELOPMENT WORKFLOW

    1. It allow you to perform various version control operation

    2. It facilitates team collaboration


Explain the debugging tools available in Visual Studio. How can developers use these tools to identify and fix issues in their code?

DEBUGGING TOOLS:

    1. Breakpoint: they allow you to inspect the code at certain point, they are visually showed as a red dot

    2. Debugging Windows: usualy open at the left side of the interface. Used to inspect and analyze the code.

    3. Step-Through Code: allow us to navigate through the code

HOW TO USE TOOLS

    1. Place breakpoints around the suspected problematic code

    2. Use step tool to navigate the through the code and wathc the behaviour of variables

    3. Analyze and inspect values using the debugging window.

    4. Fix issue and run the code to check if it still persist


A REAL-WORLD EXAMPLE OF A PROJECT which enjoy the integration of Github in Visual Studio is 
REACT from FACEBOOK

React is a popular open-source JavaScript library for building user interfaces, maintained primarily by Facebook

The React project is hosted on GitHub, and Facebook developers use Visual Studio Code, a lightweight but powerful code editor from Microsoft, for development.

