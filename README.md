# Git and GitHub commands

## Initialize a new Git repository.
```bash
git init 
```

## Clone an existing repository
```bash
git clone [url]
```

## Know status of staging area 
```bash
git status
```

## Add files to staging area
```bash
git add (file name)
git add * (to add all files at the same time)
```

## Restore files
if you add file to staging area and you want to restore it 
```bash
git restore --staged ( file name )
git reset ( file name )
```

## Move to local repo  
you can give descriptive message for your edit in the project
```bash 
git commit -m " descriptive meassage "
```

## Know all branches in local repo
```bash
git branch
```

## Know remote repo name 
```bash
git remote -v
```

## Publish your local commits to remote repo 
you can publish more than commit
```bash
git push Remote_Repo_Name Branch_Name
```

## Get changes from remote repo 
featch changes from remot repo and merge changes with local repo
```bash
git pull origin
```

## Git configration 
add your email and user name
```bash 
git config --glabal user.emal "youremail@gmail.com"
git config --glabal user.name "your Name"
```

## Open global config file
you can edit user_name , email and anything other in file
```bash
git config --global --edit
```


## Generate public key
```bash
ssh-keygen -t  rsa -b 4096 -c "your email"
-t = (algorithm type)   rsa = (algorithm)   -b = (bit numbers)  
```

## Link GitHub with shell 
```bash
ssh -T git@github.com 
```

## Create alias for commands
you can refer to command by abbreviation
```bash
git config --global aliass.st status
st = status 
```

## Create new branch
```bash
git branch ( branch name )
```

## Switch between branches
```bash
git checkout ( branch name)
```

## Create branch and move to it
```bash
git checkout -b ( branch name)
```

## Delete branch
- save delete ( if branch isn't merged , branch will not be deleted )
```bash
git branch -d ( branch name )
```
- force delete ( branch will be deleted anyway )
```bash
git branch -D ( branch name )
```
## Rename branch
```bash
git branch -m " branch name "
```

## Temporarily save changes (stash)
This is useful when you need to switch branches or work on something else but want to come back to your current changes later
```bash
git stash 
```

## Stash with a message
```bash
git stash save " message "
```

## Apply the most recent stash
This will reapply the most recent stash but keep it in the stash list
```bash
git stash apply
```

## Apply a specific stash
```bash
git stash apply stash@{No}

```

## Apply and remove the most recent stash
This will reapply the most recent stash and remove it from the stash list
```bash
git stash pop
```

## Apply and remove a specific stash
```bash
git stash pop stash@{No}
```

## List stashes
```bash
git stash list
```

## Clear all stashes
```bash
git stash clear
```

## Drop a specific stash
```bash
git stash drop stash@{No}
```

## Restore files from staging area
```bash
git restore --staged ( file name )
```

## Show files U want to delete it 
```bash
git clean -n
```

## Delete files 
```bash
git clean -f ( file name )
```

## Delete commits 
```bash
git reset --hard ( commit hash )
```
then update remote repo
```bash 
git push origin main --force 
```