| Command | Explanation | Example Use Case |
| ------- | ----------- | ---------------- |
| `git clone <required_repo>` | Clones the specified repository, creating a local copy on your machine. | `git clone https://github.com/example/repository.git` |
| `git clone -b <branch_name> <required_repo>` | Clones a specific branch from the remote repository. | `git clone -b 5.6.1 https://github.com/example/repository.git` |
| `git clone --depth <depth> <required_repo>` | Clones a repository with limited history, specifying the number of commits to include in the clone. | `git clone --depth 1 https://github.com/example/repository.git` |
| `git pull --rebase` | Updates your local repository with the latest changes from the remote repository. The `--rebase` option ensures local changes are applied on top of remote changes. | `git pull --rebase origin master` |
| `git tag -a 1.0.0 -m "bahmni-lite Release version 1.0.0"` | Creates a new annotated tag named "1.0.0" with a descriptive message. Annotated tags include additional metadata like tagger's name, email, and creation date. | `git tag -a 1.0.0 -m "bahmni-lite Release version 1.0.0"` |
| `git push origin 1.0.0` | Pushes the newly created or updated tag "1.0.0" to the remote repository named "origin", making it available to others. | `git push origin 1.0.0` |
| `git tag -d 1.0.0` | Deletes a specific tag, here named "1.0.0", from the repository if it exists. | `git tag -d 1.0.0` |
| `git tag -l` | Lists all tags in the repository, indicating specific points in its history, such as releases or milestones. | `git tag -l` |
| `git reset --hard HEAD~1` | Performs a hard reset to the commit one step before the current commit. | `git reset --hard HEAD~1` |
| `git log --merge` | Displays commit logs with information related to merges. | `git log --merge` |
| `git merge --abort` | Aborts an ongoing merge operation and returns the repository to its pre-merge state. | `git merge --abort` |
| `git merge --no-ff <feature_branch_name>` | Merges changes from a feature branch into the current branch, preserving a non-fast-forward merge. | `git merge --no-ff feature-branch` |
| `git merge --squash <feature_branch_name> && git commit -m ""` | Merges changes from a feature branch into the current branch and squashes all commits into one, followed by a commit with a message. | `git merge --squash feature-branch && git commit -m "Merged feature XYZ"` |
| `git commit -am "<commit_message>"` | This is a shortcut that allows you to stage all modified files and commit them with a single command. | `git commit -am "Fix typos in README"` |
| `git merge <feature_branch_name>` | Merges changes from a feature branch into the current branch. | `git merge feature-branch` |
| `git show <tag_name>` | Displays information about a specific tag, showing the tag's associated commit and its details. | `git show v1.0.0` |
| `git cherry-pick <commit_sha>` | Applies the changes introduced by a specific commit to the current branch. | `git cherry-pick abc123` |
| `git diff` | Shows the changes between commits, commit and working tree, etc. | `git diff` |
| `git stash clear` | Removes all stashed changes. | `git stash clear` |
| `git stash drop` | Removes the last stashed changes. | `git stash drop` |
| `git stash apply` | Retrieves a stashed change back without removing it from the stash. | `git stash apply` |
| `git stash pop` | Retrieves a stashed change back and removes it from the stash. | `git stash pop` |
| `git stash push -m "<stash message>"` | Adds a message to stash commits while stashing changes. | `git stash push -m "Working on feature XYZ"` |
| `git stash list` | Lists all stashed changes. | `git stash list` |
| `git reflog` | Displays a log of all project changes made, including deleted commits. | `git reflog` |
| `git switch -c <branch_name>` | Creates a new branch and switches to it. | `git switch -c new-feature` |
| `git remote add origin <remote_url>` | Adds a remote repository named "origin" with the specified URL. This is typically done when setting up a new repository or connecting to an existing remote repository. | `git remote add origin https://github.com/example/repository.git` |
| `git pull origin <branch_name>` | Fetches changes from the remote repository ("origin")[short hand for the url] and merges them into the specified local branch. This is useful to update your local branch with changes made by others. | `git pull origin main` |
| `git push origin <branch_name>` | Pushes the changes from a local branch to the remote repository ("origin"). This is used to share your local changes with others or update the remote branch with your local commits. | `git push origin feature-branch` |
| `git push -u origin <branch_name>` | The -u or --set-upstream option is used to set up tracking information. This means that the local branch will be associated with the corresponding branch on the remote repository, simplifying future push and pull operations. | git push -u origin feature-branch |
| `git branch` | Lists all local branches in the repository. | `git branch` |
| `git branch <branch_name>` | Creates a new branch with the specified name. | `git branch feature-branch` |
| `git branch -d <branch_name>` | Deletes the specified branch. The `-d` flag ensures a safe deletion by preventing the deletion of branches with unmerged changes. | `git branch -d outdated-feature` |
| `git branch -D <branch_name>` | Forces the deletion of the specified branch, even if it has unmerged changes. | `git branch -D outdated-feature` |
| `git branch -m <new_branch_name>` | Renames the current branch to the specified new name. | `git branch -m main` |
| `git branch -c <new_branch_name>` | Creates a new branch with the specified name and switches to it. Similar to creating a new branch and then checking it out. | `git branch -c new-feature` |
| `git branch -v` | Displays additional information about each branch, including the commit message and SHA-1. | `git branch -v` |
| `git branch --merged` | Lists branches that have been merged into the current branch. Useful for identifying branches that can be safely deleted. | `git branch --merged` |
| `git branch --no-merged` | Lists branches that have not been merged into the current branch. Helpful for identifying branches that may still have changes to be integrated. | `git branch --no-merged` |
| `git branch -r` | Lists remote branches in the Git repository. | `git branch -r` |
| `git branch --track <local_branch> <remote>/<remote_branch>` | Sets up the local branch to track the remote branch `<remote_branch>` from the remote repository named `<remote>`.  | `git branch --track feature-branch origin/feature-branch` |
| `git branch --set-upstream-to=origin/<remote_branch> <local_branch>` | Sets the upstream branch for the local branch named "<local_branch>" to "origin/<remote_branch>." The upstream branch is the remote branch that your local branch is tracking. It helps Git understand where to push and pull changes. | `git branch --set-upstream-to=origin/main main` |
| `git branch -vv` | Provides details about the upstream branches that the local branches are tracking. | `git branch -vv` |
| `git remote show origin` | Shows information such as the URL of the remote repository, the branches present on the remote, and the local branches that are configured to track branches on the remote. | `git remote show origin` |
| `git push origin --delete <branch_name>` | The --delete option indicates that you want to delete the specified branch on the remote. | `git push origin --delete feature-branch` |
| `git ls-remote <remote>` | Displays a list of commit hashes and their corresponding references (branches, tags, etc.). | `git ls-remote origin` |

