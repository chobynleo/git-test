#部署命令
heroku git:remote -a deduce-tree
git add .
git commit -am "init"
git remote rm heroku
git remote add heroku git@heroku.com:deduce-tree.git
git push heroku master
heroku open
heroku logs