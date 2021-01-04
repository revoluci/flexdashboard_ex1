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


##logの確認
git reflog
git log --oneline
git log --name-status
F2
tree .

## tmpフォルダ以下の全ファイルに関するhistoryを消去

git filter-branch -f --index-filter "git rm -rf --ignore-unmatch tmp/" --prune-empty -- --all
git reflog expire --expire=now --all
git gc --aggressive --prune=now
git push --force origin master

https://dskd.jp/archives/46.html
https://spring-mt.tumblr.com/post/25934691482/git%E6%9C%80%E5%BC%B7%E3%81%AE%E3%82%AA%E3%83%97%E3%82%B7%E3%83%A7%E3%83%B3-filter-branch
https://gist.github.com/ktx2207/3167fa69531bdd6b44f1

--chacedオプションがあると commit log からだけ削除してワークツリーでは残すようになる（つまりファイルが手元に残る）
git filter-branch --index-filter "git rm -rf --cached --ignore-unmatch tmp/" --prune-empty -- --all
git filter-branch --tree-filter 'rm -f tmp/' HEAD --all
git rebase -i xxx
