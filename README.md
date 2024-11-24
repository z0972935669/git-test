
# Git Bash 使用指南

## 1. 前往目錄
```bash
cd 你要去的地方
```

## 2. 建立 `.git`
```bash
git init
```

## 3. 檢查 Git 是否安裝成功
```bash
git --version
```

## 4. 設定個人資料
- 輸入姓名：
  ```bash
  git config --global user.name "變更裡面的名稱"
  ```
- 輸入個人的 Email：
  ```bash
  git config --global user.email "變更裡面的 email 名稱"
  ```
- 查詢 Git 設定內容：
  ```bash
  git config --list
  ```

## 5. Git 基本指令架構
工作目錄 → `(add)` → 索引 → `(commit)` → 本地數據庫 → `(push)` → 遠端數據庫  
↕ ↕ `(checkout)` ← ↓↑ `(clone/fetch)` ← ↓ ↓ `(pull)`

## 6. 常見終端機指令
- **Windows 指令**
  ```bash
  cd      # 前往資料夾
  dir     # 顯示資料夾
  mkdir   # 新增資料夾
  copy    # 複製檔案
  move    # 移動檔案
  del     # 刪除檔案
  cls     # 清除畫面上的內容
  ```

## 7. 查詢當前狀態
```bash
git status
```

## 8. 將檔案加入索引
```bash
git add .
```

## 9. 將索引檔案變成一個更新（commit）
```bash
git commit -m "修改內容"
```

## 10. 查看 Commit 歷史記錄
```bash
git log
```

## 11. 下載遠端數據庫
```bash
git clone 數據庫網址
```

## 12. 更新遠端數據庫
```bash
git push origin master
```

## 13. 新增 GitHub 遠端
```bash
git remote add origin https://github.com/z0972935669/github_0416.git
```

> **注意：** 如果已經有 `git init`，可使用以下指令：
```bash
git branch -M main
git push -u origin main
```

檢查是否綁定：打開 `.git/config` 查看以下內容：
```text
[remote "origin"]
url = https://github.com/z0972935669/github_0416.git
fetch = +refs/heads/*:refs/remotes/origin/*
```

## 14. 更新到遠端數據庫
```bash
git branch -M main
git push -u origin main
```

## 15. Git 縮寫設定
```bash
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.st status
git config --global alias.ci commit
```

## 16. 查看 Git 配置列表
```bash
git config --list
```

## 17. 遠端儲存庫操作
- 註冊遠端儲存庫：
  ```bash
  git remote add origin 遠端儲存庫網址
  ```
- 更新資料到遠端 master 分支：
  ```bash
  git push -u origin master
  ```

## 18. Checkout 查看
`checkout` 可將 HEAD 指到你想去的地方：
```bash
git checkout commit編號
```

## 19. 開分支
```bash
git branch dev
```

## 20. 切換分支
```bash
git checkout 切換的分支名稱
```

## 21. 合併分支範例
```bash
git checkout dev
touch index2.html
git add .
git commit -m 'update'
git checkout main
git merge dev
git push -u origin main
```

## 22. 快轉與取消快轉機制
```bash
git merge dev --no-ff
git push -u origin main
```

## 23. 練習 Branch
[點此練習分支](https://learngitbranching.js.org/?locale=zh_TW)

## 24. 還原
- 還原到上一版本：
  ```bash
  git reset HEAD^
  ```
- 硬還原：
  ```bash
  git reset HEAD^ --hard
  ```
- 還原至指定 Commit：
  ```bash
  git reset commit編號
  ```

## 25. 查看線圖
```bash
git log --oneline --graph
```

## 26. 移動 HEAD 到指定 Commit
```bash
git checkout commit編號
```

## 27. 查看詳細歷史記錄
```bash
git reflog
```

## 28. 開啟 VS Code
```bash
code .
```

## 29. 從遠端拉檔案
```bash
git pull
```

## 30. 上傳分支
```bash
git push origin dev
```
