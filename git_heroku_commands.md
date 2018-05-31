## Push to master branch:
- git init
- git add .
- git commit -m "first commit"
- git remote add origin "your git url"
- git push -u origin master

## create side branch and push to side branch
- git checkout -b side-branch
- git init
- git add .
- git commit -m "feature added to side branch"
- git push origin master


## On github: Send for review/ compare code difference between master and side branch

- if no issue. merge side branch to main branch, either by generating pull request on git hub or follow below steps in terminal

- git checkout master
- git merge side-branch
- git branch -d side-branch (delete the barnch locally)
- git push origin --delete side-branch (deletes teh branch remotely)
- git push -u origin master


## push to heroku after pushing to github
- heroku login
- heroku create APP-NAME
- git push -u heroku master
- heroku run rake db:migrate (if there is a database)
- heroku run rake db:seed (if you want to push default data from database)

## Generate rails app with postgres database
- rails new myapp --database=postgresql
- rails db:create (create database before migration)
