**在本地 pull 远程仓库时，报错**

![图片.png](http://upload-images.jianshu.io/upload_images/4712888-99984df5f967a0e9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# solve method
> In my case, error was just fatal: refusing to merge unrelated histories on every especially first pull request after remotely adding a git repo.
Using --allow-unrelated-histories flag worked with pull request in this way:
git pull origin branchname --allow-unrelated-histories

**gitignore 失效**
清除本地缓存
git rm -r --cached .
关联后，使用命令 git push -u origin master 第一次推送 master 分支的所有内容