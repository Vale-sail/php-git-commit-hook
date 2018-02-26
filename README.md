# php-git-commit-hook
git PHP代码提交 语法错误检查hook

```
打开项目的 .git/hook目录，将pre-commit拷贝到该目录，给与相依的权限即可 暴力解决直接 777
本脚本只检测当前用户工作区的文件即使用了git add 的文件

附赠 检测当前目录所有PHP文件是否存在语法错误检查 
ls | grep .php | awk "{print $1}" | xargs -L 1 php -l