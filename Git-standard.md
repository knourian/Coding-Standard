# 1. Git Standards

In this document best practices and a common ground for using git is proposed:

- [1. Git Standards](#1-git-standards)
  - [1.1. Common Rules](#11-common-rules)
  - [1.2. Branch](#12-branch)
    - [1.2.1. Add a new branch](#121-add-a-new-branch)
    - [1.2.2. Keep branch Updated with master](#122-keep-branch-updated-with-master)
  - [1.3. Git Submodules](#13-git-submodules)
    - [1.3.1. clone](#131-clone)
    - [1.3.2. Pull](#132-pull)
  - [1.4. Refrences](#14-refrences)

## 1.1. Common Rules

1. Each Project Should Have a **Readme&bull;md** and **.gitignore** file for the Project.
2. Each Commit Should bed **Clean**,**Single-Purpose**.
3. Commit messages should be **clear** , **Readable** and **Related to What was Actually done** .
4. **Do Not Push Directly into Master Branch** (More about this will be Covered in [branch](#Branch) section)

[Git cheat sheet](https://education.github.com/git-cheat-sheet-education.pdf)

[Another Git Cheat Sheet with Explanation](https://www.jrebel.com/blog/git-cheat-sheet)

For Further Study git look at [Git Book](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)

## 1.2. Branch

There are 3 main branches

- Master
- Development
- Test

**Development**
all Tasks will be done on this branch

**Test**
Codes on the Developement Branch After Completion will be merged within this branch with Code Review

Code Will be Published to a staging server to be tested by the users
if user Test is Succesful then the Test Branch will be merged with Master

**Master**
Stable Code , Production
After Merging Test with master a new release will be published

### 1.2.1. Add a new branch

whenever you wnated to work on a new feature create a new branch with

    git checkout -b <branch-name>

&lt;branch-name> Will Follow the Following Format:

    <branch-name> = <Type>_<Jira-Task-Number>_<Branchname>

Type:

- Bug
- Feature
- Task

**Example:**

	Bug_65_fix_order_duplicate

### 1.2.2. Keep branch Updated with master

Pull Master branch Daily into your branch to keep up with changes with master

Submit a Pull Request on That branch and wait to code being reviewed

if Everything was alright merge branch to Test

## 1.3. Git Submodules

Each project may be consisting of other projects, in order to maintain each of them separately we use git submodules.
each submodules has own git repository and this allows submodules to develop seperatly

### 1.3.1. clone

    git clone --recurse-submodules <Repo-Url>

### 1.3.2. Pull

    git pull
    git submodule update --init --recursive

[Git Submodules Documents](https://git-scm.com/book/en/v2/Git-Tools-Submodules)

[Watch Tutorial On Youtube](https://www.youtube.com/watch?v=ZYq3NJnO08U)

## 1.4. Refrences

Ref: [Using Branches](https://www.atlassian.com/git/tutorials/using-branches)

Ref #2: [Pull request](https://www.atlassian.com/git/tutorials/making-a-pull-request)
