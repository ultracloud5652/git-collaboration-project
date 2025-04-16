# Git Collaboration Project (Tom & Jerry)

## Project Overview

This project demonstrates effective Git collaboration by simulating two developers, Tom and Jerry, working on the same file using separate branches in VS Code. The goal is to merge their changes successfully without conflicts.

## Prerequisites

- Git installed (Download [Git](https://git-scm.com/))
- VS Code installed (Download [VS Code](https://code.visualstudio.com/))
- Basic familiarity with Git commands

## Project Setup

### 1. Initialize a Git Repository

#### 1. Open your terminal.

#### 2. Run the following commands:

```bash
mkdir git-project
cd git-project
git init
```

![Screenshot 2025-04-16 at 10 16 17 AM](https://github.com/user-attachments/assets/d9b9fecf-4059-40d0-aa16-ba59664203c7)

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

![Screenshot 2025-04-16 at 10 19 42 AM](https://github.com/user-attachments/assets/2811c133-c2ef-4123-a932-7e0d3908ba7b)

## Branching Workflow

### 1. Create Branches (Tom & Jerry)

```bash
git checkout -b tom
```

#### Make Changes as Tom

- Add a navigation bar to *index.html:*

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

- Commit the change:

```bash
git add index.html
git commit -m "Tom: Added navigation bar"
```

![Screenshot 2025-04-16 at 11 38 14 AM](https://github.com/user-attachments/assets/7ecddd7f-46ef-4e78-92d3-638e364924fa)

### Now Create Jerry's branch:

```bash
git checkout main
git checkout -b jerry
```

#### Make Changes as Jerry:

- Add a footer to index.html.

```html
<footer>
    <p>Contact us at contact@example.com</p>
</footer>
```

![Screenshot 2025-04-02 at 9 41 33 AM](https://github.com/user-attachments/assets/a9a2ddeb-ce6c-407d-8412-a36d4aced495)

- Commit the changes:

```bash
git add index.html
git commit -m "Jerry: Added footer"
```

![Screenshot 2025-04-16 at 11 45 18 AM](https://github.com/user-attachments/assets/e76ef143-f9aa-4612-ae1c-a241d52e9e7e)


## STEP 4: Merging

### 1. Merge Tom's branch into main:

```bash
git checkout main
git merge tom
```

![Screenshot 2025-04-16 at 11 49 49 AM](https://github.com/user-attachments/assets/7f6e94a3-95b8-4af6-a6de-bb660bfc1ced)

#### Resolve conflicts if needed, then commit:

![Screenshot 2025-04-16 at 11 32 20 AM](https://github.com/user-attachments/assets/30d0f56a-9bf3-4fee-a1e5-240fee37601b)

```bash
git add index.html
git commit -m "Resolved merge conflict between tom and main branches"
```

![Screenshot 2025-04-16 at 11 51 01 AM](https://github.com/user-attachments/assets/b2a05bdc-c4f8-40f5-8092-370f7d194e50)

## 6. Merge Jerry's Work

```bash
git merge jerry
```

![Screenshot 2025-04-16 at 11 52 53 AM](https://github.com/user-attachments/assets/8953a3e2-7f06-4ca3-89b3-483cea2905f8)

#### Resolve conflicts if needed, then commit:

![Screenshot 2025-04-16 at 11 33 42 AM](https://github.com/user-attachments/assets/7af36459-ddda-42eb-88cb-ad1e50a953b1)

```bash
git add index.html
git commit -m "Resolved merge conflict between tom and jerry branches"
```

![Screenshot 2025-04-16 at 11 55 01 AM](https://github.com/user-attachments/assets/1c8f50d7-7534-4708-9c89-3806ed27522b)



## Push to Remote Repository

```bash
git remote add origin <repository-url>
git push -u origin main
```


## Verification

#### Open index.html and confirm:

- Navigation bar added ✅

- Footer contact info added ✅
