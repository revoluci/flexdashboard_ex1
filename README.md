# flexdashboard_ex1
test
1. Creat a new repository
2. Clone by Rstudio: File > New Project... > Version Control > Git
3. Creat a _site.yml: File -> New File -> Text File
4. Creat a index.Rmd: File -> New File -> R Markdown. Choose the Flex Dashboard template.
5. Render the dashboard: Knit option
6. Commit & Push
7. Publish the docs/index.html: settings -> options -> Github Pages -> source. Select the master branch and the docs folder.

https://www.r-bloggers.com/deploying-flexdashboard-on-github-pages/
https://revoluci.github.io/flexdashboard_ex1/



git reflog
git log --oneline
git log --name-status
tree .

git filter-branch --tree-filter 'rm -f' HEAD --all
git reflog expire --expire=now --all
git gc --aggressive --prune=now
git push --force origin master

git rebase -i xxx
