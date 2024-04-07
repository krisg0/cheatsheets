#   Git usage cheatsheet    #
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
