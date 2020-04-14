#Git

## 2.1 目的
托管代码

## 2.2 基本概念
* 仓库**Repository**:存放项目代码，1个项目对应1个仓库
* 收藏**Star**:
* 复制克隆项目**fork**：把别人仓库复制一份到自己的仓库ori-->test_repo，对其进行修改时不会影响原始的项目，即，fork得到的仓库是独立的
* 发起请求**pull request**：向代码原作者发送此请求，待原作者查看，原作者如果觉得可以就会合并(**merge**)到原有仓库，源代码此时发生了改变pr-->ori-->ori_modified
* 关注**watch**：关注项目，第一时间收到项目的更新
* 事务交流**issue**：讨论问题

## 2.3 仓库管理
* 新建文件：
* 在仓库中搜索文件：快捷键 `T`

## 2.4 Git安装和使用
* [下载地址](https://git-scm.com/download/win)
### Git本地操作：
  - 代码路径：工作区-->暂存区-->Git仓库
  - 设置用户名：`$ git config --global user.name 'liuyaoxinneo'`
  - 设置邮箱：`$ git config --global user.email 'neo19941120@hotmail.com'`
  - 查看设置：
  - 在当前目录下初始化Git：`$ git init`，会在当前目录下生成.git隐藏目录记录git信息
  - 从工作区向暂存区提交文件：`$ git add test.py`
  - 从暂存区向Git仓库提交文件：`$ git commit -m '使用Git bash提交文件测试'`，出现`nothing to commit, working tree clean`即提交成功
  - 修改文件：本地修改文件-->和提交新文件一样的流程重新提交该文件即可
  - 删除本地文件：`rm test.py`
  - 删除Git库中的文件：`$ git rm test.py`，然后需要添加本次操作的描述`$ git commit -m '使用Git bash删除文件测试'`

### Git管理远程仓库(Github上的仓库)
  - git克隆的目的：将远程仓库（github上的仓库）下载到本地，在本地进行修改
  - 只需要初始化一次就会记住所有信息，查看初始化信息：`git config --list`
  - 克隆项目到本地：`git colne https://github.com/liuyaoxinneo/git_use_test.git`
  - 进行修改：添加/删除文件、编辑文件等
  - git add
  - git commit -m '说明'
  - 将本地仓库同步到git远程仓库中：`git push`

## 2.5 Github Pages搭建网站
### 搭建个人站点（静态）
* 访问：https://liuyaoxinneo.github.io
* 搭建步骤：
  1. 创建个人站点：新建仓库，仓库名必须是**用户名.github.io**
  2. 在仓库下新建 `index.html`的文件作为网站首页
* 注意点：
  - 每个网页是静态的，即没法提供交互
  - 每个repo里面只能有index.html这一个文件，否则无法访问
### 搭建项目站点
* 访问：https://liuyaoxinneo.github.io/仓库名
* 搭建步骤：**存在问题！需要按照官方文档操作**
  1. 选择需要生成站点的repository
  2. settings
  3. Github Pages板块

| 命令                     | 作用             |
| ------------------------ | ---------------- |
| git status               | 查看当前库的状态 |
| git add 文件名.后缀      |                  |
| git commit -m '提交描述' |                  |




*参考文献*
1. [简明教程](https://www.cnblogs.com/yaoxiaowen/p/8227873.html)
2. [【教程】学会Git玩转Github【全】](https://www.bilibili.com/video/BV1Xx411m7kn?p=3)
