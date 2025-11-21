#   Git usage cheatsheet    #
##   Reference    ##
[GitLab Git Cheatsheet](https://about.gitlab.com/images/press/git-cheat-sheet.pdf)
##  Commit  ##
-   add and commit in one step
    >`git commit -am "message"`
    >
##  Sync to local  ##
-   If you have NO local changes (Replace main with your branch name if different.) This force-syncs your working directory to be identical to the remote branch.)
    > `git fetch`
    > “Get me the latest info, but don’t touch my files yet.”
    > 
    > `git reset --hard origin/main`
-   If you DO have local changes you want to keep
    > `git pull --rebase` "Get the latest info AND update my files right now."
    > Rebase only your local branches that nobody else uses.
    > 
    > This applies your changes on top of the latest remote commit. If there are conflicts, Git will pause and ask you to resolve them, then continue:
    
    > `git rebase --continue`
 ##  Discard local changes  ##
-   discard local changes and back to original workspace version
    >'git restore path/to/your-file'
   
-   discard local chagnes and sync to latest remote version
    > 'git fetch'          # get latest remote version
    > 'git checkout origin/main -- path/to/your-file'



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
