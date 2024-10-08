# GitHub Repository Splitting

```
pip install git-filter-repo
```

## Move all the files with same folder structure:

 ```
 git filter-repo --path aaa/ddd --force
 git ls-tree -r HEAD --name-only
 git remote add splited-new-repo-local-name https://github.com/Infinite-demo/Split-1.git
 git push splited-new-repo-local-name main
```

 ## Move all the files to new folder(test):

 ```
 git filter-repo --path aaa/ddd --force --path-rename aaa/ddd:test
 git ls-tree -r HEAD --name-only
 git remote add splited-new-repo-local-name https://github.com/Infinite-demo/Split-2.git
 git push splited-new-repo-local-name main
```

 ## Move all the files to Root:

 ```
 git filter-repo --subdirectory-filter aaa/ddd/ --force
 git ls-tree -r HEAD --name-only
 git remote add splited-new-repo-local-name https://github.com/Infinite-demo/Split-3.git
 git push splited-new-repo-local-name main
```
