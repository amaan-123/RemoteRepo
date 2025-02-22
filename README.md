# This repo explains steps to clone a remotely created repo on GitHub to local machine (Caution: This is a work under progress)

## It is an attempt to understand local &amp; remote repo work. Please confirm with official documentation from git, github or microsoft before executing the steps for your use case

Create New Repo on GitHub web e.g Repository name is RemoteRepo(instead of "RemoteRepo", put your specific repo name):
Choose settings: e.g. good practice:

1) Clear & concise description.
2) Add README.
3) Add .gitignore: select Visual Studio (search why?).
4) Choose a license: MIT (search why?: for protection against liabilities).

After creation of "RemoteRepo" repo on GitHub web, go to settings of this newly created repo:
Set Branch protection rules in Settings>Code and automation> Branches:
Branch name pattern: main
Protect matching branches: Select "Require a pull request before merging" checkbox

You can edit/create new files in your "RemoteRepo" repo on GitHub web e.g., edit README.md and commit it online.

/*Clone & Status*/
Clone (cloning a remote repo to our local machine e.g., clone the RemoteRepo repo from your GitHub web to        local PC/laptop):
git clone "copy your GitHub web RemoteRepo repo's HTTPS link here"
/*To obtain your GitHub web "RemoteRepo" repo's HTTPS link, navigate to your GitHub web repo>     Code> Code button(green)> Local> copy HTTPS link*/
Open Terminal in VS Code(select your default terminal profile to be Git Bash):
/*To clone your GitHub web "RemoteRepo" repo inside your "MyLocalFolder" folder in VS Code on   your local machine, enter the commands:*/

```bash
git clone "https://github.com/username/RemoteRepo.git"
```

Status
ls -a //should show .git
git status //types of file status

/*Add & Commit*/
git add "file name"
git add .
git status
git commit -m "some message"
git status

/*Push Command*/
git push origin main // authorization occurs at this  step b/w VSCode & github
