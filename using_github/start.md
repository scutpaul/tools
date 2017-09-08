# git使用总结
---

>学习资源 from [廖雪峰的网站](https://www.liaoxuefeng.com)

## 安装
* ubuntu :
`sudo apt-get install git-core`

* windows: [msysgit下载](https://git-for-windows.github.io/)

* 下载后配置：
```
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
```

## 创建版本库
* 创建目录
`git init`
* 文件添加到git仓库
`git add ****`
* 文件提交到仓库
`git commit -m "注释"`

## 查看git仓库历史
* 掌握仓库的当前状态
`git status`
* 查看上次修改内容
`git diff`
* 查看最近的提交日志
`git log`
* 回退到之前的版本
`git reset --hard commit_id`版本号不必写全
* 查看历史的版本
`git reflog`

## 修改与删除
* 第一次修改->`git add`—>第二次修改->`git add`->再统一提交`git commit`
* 撤销工作区修改`git checkout -- **`  会回退到最近一次add或commit
* 删除文件后，1.`git rm **`->`git commit` 2.恢复到删除前：`git checkout -- **`

## 远程仓库
* 首次连接

第一次创建ssh密钥` ssh-keygen -t rsa -C "youremail@example.com"`；用户主目录下有`id_rsa`私钥，`id_rsa.pub`公钥；登陆GitHub，打开“Account settings”，“SSH Keys”页面：然后，点“Add SSH Key”，填上任意Title，在Key文本框里粘贴`id_rsa.pub`文件内容

GitHub允许添加多个Key。如有若干电脑，只要把每台电脑的Key都添加到GitHub，就可以在每台电脑上往GitHub推送了

* 添加到远程仓库

在github网站新建Repository; 在本地git仓库下输入` git remote add origin git@github.com:scutpaul/***.git` 关联到远程创建的库; 将本地内容推送到远程`git push -u origin master`

* 从远程仓库克隆

本地输入`git clone git@github.com:scutpaul/***.git`

## 使用他人的仓库

* 在网站上的开源项目点击Frok，就复制到自己的远程仓库中


## git仓库示意图
![](http://ovwzquk58.bkt.clouddn.com/tools/using_git/graph/0.jpg)
