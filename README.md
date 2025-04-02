# Git Collaboration Project (Tom & Jerry)

## Project Overview

This project demonstrates effective Git collaboration by simulating two developers, Tom and Jerry, working on the same file using separate branches in VS Code. The goal is to merge their changes successfully without conflicts.

## Prerequisites

- Git installed (Download [Git](https://git-scm.com/))
- VS Code installed (Download [VS Code](https://code.visualstudio.com/))
- Basic familiarity with Git commands

## Project Setup

### 1. Initialize a Git Repository

```bash
mkdir git-project
cd git-project
git init
```
![Screenshot 2025-04-02 at 9 39 54 AM](https://github.com/user-attachments/assets/f88b4c3b-8f4d-4716-9266-6104c0643a87)

### 2. Create an index.html File
### Create an index.html file and add the following structure:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Git Project</title>
</head>
<body>
    <h1>Welcome to the Git Project</h1>
</body>
</html>
```
![Screenshot 2025-04-02 at 9 40 31 AM](https://github.com/user-attachments/assets/cdb0cb2f-5575-41e8-a14c-3c46ceec533f)

### Commit the file:

```bash
git add index.html
git commit -m "Initial commit with index.html"
```

## Branching Workflow

### 3. Create Separate Branches

```bash
git checkout -b tom  # Tom's branch
git checkout -b jerry  # Jerry's branch
```

### 4. Make Changes

### Tom (Navigation Bar)

#### Switch to Tom’s branch:

```bash
git checkout tom
```

#### Add a navigation bar to *index.html:*

```html
<nav>
    <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Contact</a></li>
    </ul>
</nav>
```
![Screenshot 2025-04-02 at 9 41 01 AM](https://github.com/user-attachments/assets/7bbc6447-d58b-4145-98ab-6674e18937e6)

#### Commit the change:

```bash
git add index.html
git commit -m "Added navigation bar"
```
### Jerry (Footer Contact Info)

#### Switch to Jerry’s branch:

```bash
git checkout jerry
```

#### Add contact info in a footer:

```html
<footer>
    <p>Contact us at contact@example.com</p>
</footer>
```

#### Commit the change:

```bash
git add index.html
git commit -m "Added footer contact information"
```
![Screenshot 2025-04-02 at 9 41 33 AM](https://github.com/user-attachments/assets/a9a2ddeb-ce6c-407d-8412-a36d4aced495)

## Merging Changes

### 5. Merge Tom's Work First

```bash
git checkout main
git merge tom
```
#### Resolve conflicts if needed, then commit:

```bash
git add index.html
git commit -m "Merged tom into main"
```

## 6. Merge Jerry's Work

```bash
git checkout jerry
git merge main
```
#### Resolve conflicts if needed, then commit:

```bash
git add index.html
git commit -m "Resolved merge conflicts"
```

```bash
git checkout main
git merge jerry
```

## Push to Remote Repository

```bash
git remote add origin <repository-url>
git push -u origin main
```

## Verification

#### Open index.html and confirm:

- Navigation bar added ✅

- Footer contact info added ✅
