#   Git usage cheatsheet    #
##  Commit  ##
-   add and commit in one step
    >`git commit -am "message"`
##  HEAD and detached HEAD  ##
-   if you dont have any changes to keep
    >   `git checkout main`

-   if you have changes that you want to keep
    >   option1:
`git branch temp`
`git checkout main`
`git merge temp`

    >   option2:
`git stash`
`git checkout main`
`git stash pop`

##  Branch  ##
-   delete local branch
    >   `git branch -d <branchname>`
    ***only deletes if the branch has already been fully merged in its upstream branch***

-   delete remote branch
    >   `git push -d <branchname>`
