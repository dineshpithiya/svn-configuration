1) Bydefault when we fire SVN command then it will create your project folder

```	
svn checkout https://www.domain.com/svn/xyz_project/
```
2) Check your folder created or not, if yes then OK else need to check with admin or SVN link provider
 Put whatever your project content inside created project
 ```
 svn status
 ```
3) Create version vise folders
```
svn mkdir -m "Version 1.1 laravel with mysql" https://www.domain.com/svn/xyz_project/version-1.1
```
4) Delete directory
```
svn delete https://www.domain.com/svn/xyz_project/version-1.1
svn rm -m "Deleting folder" https://www.domain.com/svn/xyz_project/newdir
```
5) Add specific file or folder
> Add specific file or folder
```
svn add yournewfilehere 
svn add yournewdirectoryincludingfiles/ 
```
OR

Update specific file from your local system to SVN
```
svn update xyz_file_name.ext
```
Update specific folder from your local system to SVN
```
svn svn yournewdirectoryincludingfiles/ 
```
Commit means upload to SVN server
```
svn commit -m "I made changes.  Woohoo."
```
## Remove all .svn folders, recursively
> For Mac OS X
```
rm -rf `find . -type d -name .svn
```
> For Windows
```
for /r %R in (.svn) do if exist %R (rd /s /q "%R")
```

> to check out in your global server
```
git svn init --prefix=svn/ --username='user' --no-metadata --no-minimize-url --trunk='trunk' --tags='tags' --branches='branches' http://www.domain.com/xyz
```
> OR
```
svn co --username='xxx' --password xxxxx http://www.domain.com/xyz
```
Get more help [Click](https://stat.ethz.ch/pipermail/bioc-devel/2016-May/009224.html)