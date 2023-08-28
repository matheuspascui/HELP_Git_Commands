# GitHub Tutorial

### Initialize Git on an existing repository

In my case, most of the times, I already have a folder that contains my coding exercises that I want to push to GitHub.
To start all the process, **organize the folder with the codes**. Then, the first command is `git init`. This will **initialize a git repository in the current folder**.

Writing the commands in a logical order would be:

- `git init` :arrow_right: to initialize a git repo in the current folder of my D:/ or C:/ directory
- `git status` :arrow_right: this will show the status of the git repo, at the moment, it is possible that i have some code that will be marked as untracked. To make Git track those codes, the following command:
- `git add`, `git add -A`, `git add .` :arrow_right: this will add all the files and folders to the git local repository. (Using "." or "-A" to add ALL)
- `git commit -m` :arrow_right: to commit the codes and files (it's like a printscreen of all the content). The `-m` flag is used to write a commit message (a good practice), to inform what the changes or the purpose of that commit
- `git remote add <name> <url>` :arrow_right: to create the link between my local and my GitHub repository. The `<name>` is to give the name and the `<url>` is to pass the url of the GitHub repo.
- `git push origin main`

### Errors

In case of errors, read the error message and if necessary, search google. My error was error assignin the push to my remote GitHub repo. So i read some tutorials and:
- updated git remote (`git remote update`)
- reseted the main branch of local repository (`git reset origin main`). In this case, i reseted the origin (that is the name i gave the remote repo) and the main branch.
- `git status` to see what is missing
- As the status message returned that i had some files untracked, i added them using `git add -A`
- I checked the status again, and needed to commit those changes, so `git commit -m <message>`
- after the commit was successfully done, i pushed to the remote repo (origin, in the main branch) using `git push origin main`. The push message returned success. Also, i checked my remote repo at GitHub, refreshing the page and mi files were there, as expected.

### BRANCHES

In a real world scenario, the changes in the branch won't be committed on the main, instead on any "development" or so branch.
To create a different branch:
- `git checkout -b development` :arrow_right: this creates a branch called "development"
- `git checkout development` :arrow_right: this moves you to the "development" branch (if you aren't in it)

After the "development" is ready, you can switch to the "main" and then **merge then**.
- `git checkout main`
- `git merge development`
- `git push` :arrow_right: to push all

