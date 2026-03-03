1. 在本地初始化 git 仓库并提交
在 PowerShell 里进入你的项目目录：
cd d:\coding
初始化仓库：
git init
可选：看一下有哪些文件准备提交：
git status
把当前所有文件加入暂存区：
git add .
创建一次初始提交（提交信息可以改成你喜欢的）：
git commit -m "Initial commit"
2. 在 GitHub 上创建远程仓库
打开浏览器，登录 GitHub。
右上角 + → New repository。
取一个仓库名（例如 tetris-game），其他选项默认即可。
点击 Create repository。
GitHub 会给你显示类似：
HTTPS 地址：https://github.com/<你的用户名>/tetris-game.git
或 SSH 地址：git@github.com:<你的用户名>/tetris-game.git
先记下 HTTPS 地址。
3. 关联远程仓库并 push
回到 PowerShell，在项目目录下：
git remote add origin https://github.com/<你的用户名>/tetris-game.git
把本地 master/main 分支推到远程（现代 Git 默认分支多是 main，如果不确定先看一下）：
git branch
如果显示 * main，说明当前是 main；假设是 main，执行：
git push -u origin main
如果是 master，就改成：
git push -u origin master
首次 push 时，Git 会弹出 GitHub 登录/Token 验证窗口，按提示登录即可。
4. 以后如何更新代码
以后你在 d:\coding 里改了文件，只需要三步：
git add .git commit -m "描述这次改了什么"git push

