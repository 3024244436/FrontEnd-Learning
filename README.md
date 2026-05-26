# 前端学习之路 🚀

> 千万要来tju软件学院，教的实在是太多了
> 开始时间：2026年5月

## 学习路线
**随便吧，反正还有又臭又长的专业课占我时间**

## 项目目录
**无，自己看**

## 时刻鞭策自己git的用法

> 学一次记不住，那就把它写进 README，每次进仓库都看一眼 😤

查看当前配置：
```bash
git config --global --list
```

---

### 🚀 把本地文件夹首次推送到 GitHub

**前置条件**：先在 GitHub 网页上建好一个空仓库（不要勾 README / .gitignore / LICENSE）。

```bash
# 1. 进入本地项目文件夹
cd E:\FrontEnd

# 2. 初始化 git 仓库
git init

# 3. （可选但推荐）新建 .gitignore 屏蔽垃圾文件
#    内容见下方"常用 .gitignore"

# 4. 把所有文件加入暂存区
git add .

# 5. 提交到本地仓库
git commit -m "init: 项目初始化"

# 6. 改主分支名为 main
git branch -M main

# 7. 关联远程仓库（地址换成你自己的）
git remote add origin https://github.com/3024244436/FrontEnd-Learning.git

# 8. 首次推送（-u 让以后只要 git push 就行）
git push -u origin main
```

---

### ⚡ 日常三连（写完代码就执行）

```bash
git add .                              # 暂存所有改动
git commit -m "feat: 完成 xxx 练习"     # 提交并写清楚做了啥
git push                               # 推送到 GitHub
```

**Commit message 前缀规范**（养成好习惯）：
| 前缀 | 含义 | 示例 |
|------|------|------|
| `feat:` | 新功能 / 新内容 | `feat: 新增 Flex 布局练习` |
| `fix:` | 修 bug | `fix: 修复图片路径错误` |
| `docs:` | 改文档 / 笔记 | `docs: 更新 README` |
| `style:` | 调样式 / 格式 | `style: 统一缩进` |
| `refactor:` | 重构代码 | `refactor: 抽离公共样式` |

---

### 📥 常用查询命令

```bash
git status              # 看哪些文件改了 / 没提交（最常用！）
git log --oneline       # 看提交历史
git diff                # 看具体改了哪些行
git remote -v           # 看关联了哪个远程仓库
git branch              # 看本地分支
```

---

### 🌿 分支操作（以后协作会用）

```bash
git branch dev          # 新建 dev 分支
git checkout dev        # 切换到 dev 分支
git checkout -b feature # 新建并切换（合并版）
git merge dev           # 把 dev 合并到当前分支
git branch -d dev       # 删除已合并的分支
```

---

### 🆘 救命操作（手滑时用）

```bash
# 撤销工作区某个文件的修改（还没 add）
git checkout -- 文件名

# 取消暂存（已 add 但还没 commit）
git reset HEAD 文件名

# 修改最后一次 commit 的信息
git commit --amend -m "新的消息"

# 拉取远程最新代码（开多台电脑时记得先拉）
git pull

# 远程有内容但本地没有，强制合并不相关历史
git pull origin main --allow-unrelated-histories
```

---

### 📋 常用 .gitignore

在项目根目录建 `.gitignore` 文件，写入：

```gitignore
# 系统文件
.DS_Store
Thumbs.db
desktop.ini

# 编辑器
.vscode/
.idea/
*.swp

# 依赖与构建产物
node_modules/
dist/
build/

# 日志与临时
*.log
*.tmp

# 大文件
*.mp4
*.zip
*.rar
```

---

### ⚠️ 新手坑提醒

1. **`.gitignore` 必须在 `git add .` 之前建好**，否则垃圾文件已被跟踪，删起来麻烦
2. **HTTPS push 时的密码不是 GitHub 登录密码**，是 Personal Access Token（PAT）
3. **别把密码 / API key / 大视频文件传上来**，GitHub 单文件 100MB 上限
4. **报 `Updates were rejected`**：远程有本地没有的提交，先 `git pull` 再 push
5. **每次写代码前先 `git status`**，养成习惯，永远知道当前仓库状态

---

## 📬 联系我

- GitHub: [@3024244436](https://github.com/3024244436)
- Email: qinzhiqian666@outlook.com
- Email：qzq5566_0@qzq.com
- QQ:1416678578
