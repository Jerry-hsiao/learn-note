## Github 建立一個專案 [git-note]

## SSH Key 設定

- 產生 SSH Key

```bach
ssh-keygen
# 確認 id_rsa 位置
# 密碼
# 確認密碼
```

- 複製 SSH Key

```bach
cat ~/.ssh/id_rsa.pub
```

- 到 GitHub 網站依據下列路徑並點擊按鈕後將其貼上，Title 的部分依據設備命名

```
Github > Settings > SSH and GPG keys > New SSH Key
```

# Git 指令

### 基本設定

```
查詢版本
git version

查詢設定列表
git config --list

輸入姓名
git config --global user.name "你的名字"

輸入email
git config --global user.email "你的email"
```

### 新增本地/遠端數據庫

```
在本地資料夾新增數據庫
git init

複製遠端數據庫
git clone 遠端數據庫網址
```

### 增加/刪除檔案

```
增加檔案進入索引
git add 檔案名稱

增加全部檔案進入索引
git add .

查詢狀態
git status

顯示歷史紀錄
git log

將索引提交到數據庫
git commit -m '更新訊息'
```

### 還原指令

```
還原工作目錄與索引，會跟最後一次 commit 保持一樣
git reset --hard

全部檔案取消索引
git reset HEAD

單一檔案取消索引
git reset HEAD 檔案名稱

恢復單一檔案到最新 commit 狀態
git checkout 檔案名稱

刪除最近一次 commit
git reset --hard HEAD^

上面語法如果刪除錯了可以再用此語法還原
git reset --hard ORIG_HEAD

刪除最近一次 commit，但保留異動內容
git reset --soft HEAD^

commit 後發現有幾個檔案忘了加入進去，想要補內容進去時
git commit --amend
```

### 分支

```
顯示所有本地分支
git branch

新增分支
git branch 分支名稱

切換分支
git checkout 分支名稱

ＨEAD 目前所在位置指標
git checkout commit前面四碼 （用來查看之前commit的檔案）
git checkout master （恢復到最新狀態）

合併指定分支到目前的分支
git merge 分支名稱

刪除分支
git branch -d 分支名稱
```

### 遠端數據庫操作

```
複製遠端數據庫
git clone 遠端數據庫網址

查詢遠端數據庫
git remote

將本地分支推送到遠端分支
git push 遠端數據庫名稱 遠端分支名稱

將遠端分支拉下來與本地分支進行合併
git pull
```

### 標籤

```
查詢標籤
git tag

查詢詳細標籤
git tag -n

刪除標籤
git tag -d 標籤名稱

新增輕量標籤
git tag 標籤名稱

新增標示標籤
git tag -am "備註內容" 標籤名稱
```

### 暫存

```
暫時儲存當前目錄
git stash

瀏覽 stash 列表
git stash list

還原暫存
git stash pop

清除最新暫存
git stash drop

清除全部暫存
git stash clear

```
