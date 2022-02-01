# learning-git

This repo was used to learn Git from amigoscode.

https://youtu.be/3fUbBnN_H2c

1:25:47 -- Git Workflow

# git test
Hello Odin!

# git cheatsheet
Commmands related to a remote repository:
.. git clone git@github.com:km3gna/learning-git.git
.. git push or git push origin main

Commands related to workflow:
.. git add .
.. git commit -m "Memo describing what was done to make this snapshot different"

Commands related to checking status or log history:
.. git status
.. git log

Basic Git syntax is "program | action | destination":
.. git add .  >>  git | add | . (period represents everything in current directory)
.. git commit -m "message"  >>  git | commit -m | "message"
.. git status  >>  git | status | (no destination)

Best practices:
.. atomic commits (commit that includes changes related to only one feature or task of your program)
.. leveraging those atomic commits

Why?
.. (1) if something you change turns out to cause problems, it is easy to revert the specific change without losing other changes
.. (2) enables you to write better commit messages

Changing the Git Commit Message Editor:
.. Using VSCode and don't want to get stuck writing a commit message in Vim (git commit without message flag, -m)
.. git config --global core.editor "code --wait"
.. above command will open a new tab in VSCode with the ability to write commit message and an optional description below it; save, exit

# HTML
macOS/navigate to directory containing file and use:
open ./index.html