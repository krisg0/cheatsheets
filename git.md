#   Git usage cheatsheet    #
##   Reference    ##
[GitLab Git Cheatsheet](https://about.gitlab.com/images/press/git-cheat-sheet.pdf)
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

##  SSH  ##
1.    ssh-keygen -t ed25519 -C "krisg0@tee.dummy.com"
2.    add public key to github account
3.    eval "$(ssh-agent -s)"
4.    ssh-add <path_to_private_key>
