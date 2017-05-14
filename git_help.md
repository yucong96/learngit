# Git 使用帮助



## 安装

*安装后，设置名字*

**git config --global user.name "your_name"**

*安装后，设置邮箱*

**git config --global user.email "your_email"**



## add 和 commit

*新建一个文件夹*

**git init**

*（出现.git隐藏文件夹）*

*新建一个文件，如readme.md*

*编辑readme.md，保存*

**git add readme.md**

**git commit -m "add_some_comment"**

*再次编辑readme.md，保存*

**git add readme.md**

**git commit -m "add_some_comment"**

*（可以多次add一个文件，或多次add多个文件到暂存区后，一次性commit）*



## 撤销

*撤销编辑（在add之前，退回到编辑前的状态）*

**git checkout -- readme.md**

*撤销编辑（在add之后，commit之前，退回到编辑前的状态）*

**git reset HEAD readme.md**

**git checkout -- readme.md**



## 查看状态

**git status**



## 查看当前文件与仓库里的文件的区别

**git diff readme.md**



## 查看版本号日志

**git log**



## 版本控制

*回退（一个）版本*

**git reset --hard HEAD^**

*回退（两个）版本*

**git reset --hard HEAD^^**

*回退（十个）版本*

**git reset --hard HEAD~10**

*回到最新版本*

**git reset --hard several_top_number_of_version_id**




## 查看版本号变化记录

**git reflog**



## 文件删除

*文件夹中删除了readme.md，如果确实删除，则*

**git rm readme.md**

*文件夹中删除了readme.md，如果想要恢复，则*

**git checkout -- readme.md**



## 删库

**rm -rf .git**


## 远程

*生成SSH密钥*

**ssh-keygen -t rsa -C "your_email"**

*（然后一路Enter）*

*在用户主目录（C:\Users\郁葱）下找到.ssh文件夹，中有id_rsa（私钥）和id_rsa.pub（公钥）*

*登录Github，进入Setting->SSH and GPG keys，随便设置一个标题，并将id_rsa.pub中的内容复制进去即可*

*在Github上建立仓库learngit*

**git remote add origin git@github.com:yucong96/learngit.git**

*（git@github.com:yucong96/learngit.git可以从Github网站上复制，origin为通常设置，可以修改）*

**git push -u origin master**

*（第一次使用会出现authenticity can't be established，输入yes继续，之后会出一个Warning）*

*之后提交更改*

**git push origin master**



## 克隆

**git clone origin git@github.com:yucong96/learngit.git**