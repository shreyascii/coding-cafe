1. '--global` makes Git save my github username and email in the user-level config file (`~/.gitconfig`), so the settings apply to every repository on the computer.

2. The `.git` directory appeared in `ls -a` but not in `ls`. It is hidden because its name starts with a dot. It contains everything Git uses to track the project, including the commit history, the repository settings, and a record of the current branch.

3. Git offered to track hundreds of files and folders. Many of these were not written by me.
   
4. Everything inside `.venv/` disappeared from the `git status` output, along with `pycache` and `.DS_Store` entries that were present. 

5. 'gitignore' should be commited as it is a part of the project file and will get saved in its history. This ensures the ignore rules are held in place.

6. `README.md` moved from "Untracked files" to "Changes to be committed." In the three-places model `git add` moved it from the working directory into the staging area. It is now selected for the next commit but has not yet been saved to the repository's history.

7. git printed "[main (root-commit) d5a0748] Lab work so far" 5 files changed, 20 insertions(+)

8. d5a0748 - is the commit's unique ID. Git generates it, and it is used to refer to that exact commit later. 

9.
The four steps of the loop are: edit (create or change files), check with `git status` to see what changed, stage the changes with `git add`, and save them with `git commit`. Running `git log --oneline` afterward confirms the new commit was recorded.

10.
`README.md` has a special name and location because it is the file people look for first when they open a project. GitHub recognizes the name and automatically displays it on the repository's front page, so it works as the project's introduction. A file called `notes.md` would just be another file in a folder and would not be shown or treated as the project overview. Keeping it in the top-level folder also means it is visible without having to dig through subfolders.

11.
`gh auth login` signed the terminal into the GitHub account and saved a login token on the computer. Git is set up to use that saved token whenever it talks to GitHub over HTTPS, so there is no need to type a username or password on each push. This is also safer than typing a password, since the token is stored by the system and is not entered by hand each time.

12.
The front page of the repository shows the contents of `README.md`, displayed as formatted text (with the heading, bolded text, and the list of contents) rather than raw markdown, along with the list of files and folders. The README appears there because GitHub automatically renders the `README.md` in the top-level folder as the project description for anyone visiting the repository.

13.
No, pushing did not change the local history. `git log --oneline` shows the same three commits with the same hashes as before. A push only copies the commits to the remote repository on GitHub. The one visible difference is that the local branch is now linked to `origin/main`, which shows up in `git status`, but the commits themselves are unchanged.

14.
A private repository exists on GitHub, but access is restricted, so only the owner and people who have been given permission, such as the TAs added as collaborators, can see it. A repository that does not exist on GitHub has not been uploaded at all, so it is only stored on the local computer. Private still means the work is backed up online and can be shared with chosen people, while not existing on GitHub means there is no online copy.
