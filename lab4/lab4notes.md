1. '--global` makes Git save my github username and email in the user-level config file (`~/.gitconfig`), so the settings apply to every repository on the computer.

2. The `.git` directory appeared in `ls -a` but not in `ls`. It is hidden because its name starts with a dot. It contains everything Git uses to track the project, including the commit history, the repository settings, and a record of the current branch.

3. Git offered to track hundreds of files and folders. Many of these were not written by me.
   
4. Everything inside `.venv/` disappeared from the `git status` output, along with `pycache` and `.DS_Store` entries that were present. 

5. 'gitignore' should be commited as it is a part of the project file and will get saved in its history. This ensures the ignore rules are held in place.

6. `README.md` moved from "Untracked files" to "Changes to be committed." In the three-places model `git add` moved it from the working directory into the staging area. It is now selected for the next commit but has not yet been saved to the repository's history.

7. git printed "[main (root-commit) d5a0748] Lab work so far" 5 files changed, 20 insertions(+)

8. d5a0748 - is the commit's unique ID. Git generates it, and it is used to refer to that exact commit later. 
