# all used commands

# creating task1 file with README.md inside and pushing
git  commit -m "some message";
git push origin main

#creating new branch dev: committed new file and pushed
git checkout -b dev
git commit -m "some message"
git push origin dev

#creating new branch zkurbonov-new-feature: adding readme md file, checking git status, adding
# .gitignore file, committing and pushing
git checkout -b zkurbonov-new-feature
git add README.md
git status
git add .gitignore
git commit -m "some message"
git push origin zkurbonov-new-feature

#creating pull request to dev branch and merging current branch to dev branch and checking out dev branch
#and creating pull request from dev branch to main branch and merging to main branch
git checkout dev
git merge zkurbonov-new-feature
git checkout main
git merge dev

#checking out zkurbonov-new-feature branch and making changes to README.md file, commiting, reverting last commit in this branch
git checkout zkurbonov-new-feature
git commit -m "some message"
git revert --hard HEAD^

#checking out main branch, getting git log, saving to file, committing and pushing
git checkout main
git log
git commit -m "some message"
git push origin main

#deleting local and remote branch zkurbonov-new-feature
git branch -d zkurbonov-new-feature
git push -d origin zkurbonov-new-feature