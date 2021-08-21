# Common Rules

1. Each Project Should Have a **Readme.md** and **.gitignore** file for the Project.
2. Each Commit Should bed **Clean**,**Single-Purpose**. 
3. Commit messages should be **clear** , **Readable** and **Related to What was Actually done** .
4. **Do Not Push Directly into Master Branch** (More about this will be Covered in [branch](#Branch) section)



[Git cheat sheet](https://education.github.com/git-cheat-sheet-education.pdf)

[Another Git Cheat Sheet with Explanation](https://www.jrebel.com/blog/git-cheat-sheet)

For Further Study git look at [Git Book](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)

# Branch



Whenever You wanted to Modify code Create a branch

`git branch <branch-name>`

`git checkout<branch-name> `

and do your work Commit and push to that branch.



Submit a Pull Request on That branch and wait to code being reviewed 

if Everything was alright merge branch to master 



Ref: [Using Branches](https://www.atlassian.com/git/tutorials/using-branches)

Ref #2: [Pull request](https://www.atlassian.com/git/tutorials/making-a-pull-request)



# Git Submodules

Each project may be consisting of other projects, in order to maintain each of them separately we use git sub modules.

Please Read reference 

to clone a project with submodules use
>
	git clone --recurse-submodules <repo name>

Ref : [Git Submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules)
