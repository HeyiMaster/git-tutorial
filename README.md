# git-tutorial
### 1.配置git中的username，email
- ```git config --global user.name “Walker-Leee”```
- ```git config --global user.email “flana_zhong#163.com”```

#### 查看commit：帮助文档
- `git help commit   git help [something]`

### 2.创建仓库
- 首先新建一个文件夹gitComponent
- `git init` _初始化，会在文件夹中生成一个.git文件以及. .._
- `git add .` 			*/*主要添加的文件， 这里的. 表示添加文件中的所有文件*/*
- `git commit -m “this is my first commit”` 		*提交，并且附上说明信息*

### 3.添加文件以及日志文件
- `git log`  _查看日志信息（这个就是我们commit的时候附加的说明信息）_
- `git log author=”Walker-Lee”`
- `git status` _查看文件的状态，是否发布_

### 4.在上一步骤中，我们新建了两个txt文件，这是 我们将second.txt文件添加进去
- `git add second.txt`		_这是比较安全可行的做法相比_ . 
- **working copy > staging area > repository 执行的过程**

### 5.查看文件的修改细节
- `git diff`   _比较work中文件和repository中的差异_
- `git diff --staged`

### 6.文件的删除移动与重命名
- `git rm <file>`	_删除文件_  `git commit -m “some message”` _提交_
- `git mv <oldfile> <newfile>`
_在已经添加到repository情况下，多个文件更改后，要提交：_
- `commit git commit -am “same message”`

### 7.文件的检查，想将本地文件和repository中的文件进行对比，我们就可以检查文件       
- `git checkout -- index.html`   _检查index.html文件与repository中文件的差异并与之同步。_

### 8.文件提交到stage以后，如果想做修改后再添加到repository中
- `git reset HEAD index.html`

### 9.同步repository中，过去某一时刻的文件
1. git log 查看需要同步的过去文件version
2. git checkout <commit version number> <file name>
3. git checkout dg152 index.html   其实这做法和7类似，7默认对比上一版本。

### 10.github	
- new repository -> name
- 本地提交文件到repository
  - git init -> git add . -> git commit -m “first commit”
  - 上传到github：
  - `git remote add githubRep http://github.com/Walker-Lee/tutorials.git(github上的http)`
  - `git push -u githubRep master`

### 11.github Desktop

### 12.git分支管理
1. 分支的创建和合并
  + \# git branch local
  + \# git checkout local
2. 在local分支进行开发，完成后合并到master
  + \# git checkout master
  + \# git merge local
  + \# git branch -d local  _合并后删除branch_
