# Lab 1 – Git & GitHub

| # | Command | Definition |
|---|---------|------------|
| 1 | `mkdir "Lab1git&github"` then `cd "Lab1git&github"` | Creates the lab folder on the PC and moves into it. Quotes are needed because of the `&` in the name. |
| 2 | `git init` | Turns the folder into a Git repository by creating a hidden `.git` folder that tracks all changes. |
| 3 | `touch README.md` | Creates a README file that describes the project. GitHub shows it on the repo's main page. |
| 4 | *(copy `mycv.txt` into the folder)* | Adds the CV text file to the working directory. Git sees it as an untracked file. |
| 5 | `git add mycv.txt` | Moves the file to the staging area, so it will be included in the next commit. |
| 6 | `git commit -m "first commit"` | Saves a snapshot of the staged files in the history, with the message "first commit". |
| 7 | *(edit `mycv.txt`: add "ENG" to the name)*, then `git add mycv.txt` | Changes the file, then stages the change so it can go into the amended commit. |
| 8 | `git commit --amend -m "first commit"` | Replaces the last commit with a new one that includes the staged change. You can also change the message. No extra commit is added to the history. |
| 9 | *(edit `mycv.txt`: add "bad skills: bakrah el nas kolaha")*, then `git add mycv.txt` | Makes a new change to the file and stages it. |
| 10 | `git commit -m "new another commit"` | Creates a second commit containing the "bad skills" change. |
| 11 | `git reset --hard HEAD~1` | Moves the branch back one commit and deletes that commit's changes from the files. The "bad skills" line is gone. `--hard` discards changes permanently. |
| 12 | `git push -u origin main` | Uploads the local `main` branch to the GitHub repo (`origin`). `-u` sets it as the default upstream, so later you can just type `git push`. |
| 13 | `git add .` | Stages every new or changed file in the folder. Here it picks up the README that wasn't added before. |
| 14 | `git commit -m "forgotten readme file"` | Commits the README file to the history. |
| 15 | `git push -u origin main` | Pushes the new commit to GitHub, so the README now appears in the remote repo. |

**Note:** Before the first push, the GitHub repo must be linked with
`git remote add origin <repo-URL>`. If your default branch is called `master`, rename it with `git branch -M main`.