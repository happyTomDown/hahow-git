# Command-Line(命令列)指令

## cmd指令
---
| Windows     | MAC／Linux | 描述               | 範例                    |
|-------------|------------|-------------------|------------------------|
| `cd`        | `cd`       | 移動到指定的資料夾 | `cd Desktop`           |
| `mkdir`     | `mkdir`    | 建立新的資料夾     | `mkdir dir1`           |
| `move`      | `mv`       | 移動檔案           | `move dir2 dir1`       |
| `copy`      | `cp`       | 複製單個檔案       | `copy pratice.txt pratice2.txt` |
| `xcopy`     | `cp -r`    | 複製整個資料夾     | `xcopy dir2 dir3`      |
| `dir`       | `ls`       | 查看當前資料夾內的檔案 | `dir`                |
| `del`       | `rm`       | 刪除檔案           | `del pratice.txt`      |
| `rmdir`     | `rm -r`    | 刪除整個資料夾     | `rmdir dir1`           |
| `cls`       | `clear`    | 清空命令列工具     | `cls`                  |
| `exit`      | `exit`     | 關閉命令列工具     | `exit`                 |

# Git指令
## remote , push , pull , fetch
---
| 指令                                      | 內容                                                                 |
| ----------------------------------------- |:------------------------------------------------------------------- |
| `git remote add <remote-name> <remote-url>` | <ul><li>向現有的 Git 儲存庫添加新的遠端儲存庫</li></ul>             |
| `git remote -v`                             | <ul><li>顯示所有遠端`儲存庫的名稱`和 `URL`</li></ul>                    |
| `git remote show origin`                    | <ul><li>顯示 `origin` 遠端儲存庫的詳細信息，包括它的 `URL`跟蹤分支等等</li></ul> |
| `git push -u origin mybranch-name`          | <ul><li>推送本地分支到遠端儲存庫，並設置上游分支</li></ul>          |
| `git clone <repository-url>`                | <ul><li>首次下載遠端儲存庫的完整副本到本地</li></ul>                |
| `git pull`                                  | <ul><li>從遠端儲存庫下載最新的資料到本地儲存庫</li><li>將本地儲存庫取出到工作目錄</li></ul> |
| `git fetch`                                 | <ul><li>從遠端儲存庫下載最新的資料到本地儲存庫</li><li>但不會自動合併</li></ul>      |



## checkout , branch , merge
---
| 指令                                      | 內容                                                                |
| ----------------------------------------- |:------------------------------------------------------------------- |
| `git checkout <sha1>`                     | <ul><li>將儲存庫 `<sha1>` 版本的所有資料取出到工作目錄 (HEAD)</li><li>工作目錄會移動到 `<sha1>`</li></ul> |
| `git checkout <sha1> <file>`              | <ul><li>將儲存庫 `<sha1>` 版本的 `<file>` 取出至工作目錄 (HEAD)</li><li>工作目錄上的 `<file>` 會變成 `<sha1>` 版本的</li></ul> |
| `git checkout <sha1> .`                   | <ul><li>將儲存庫 `<sha1>` 版本的所有資料取出至工作目錄 (HEAD)</li><li>工作目錄上的所有檔案會變成 `<sha1>` 版本的</li></ul> |
| `git checkout HEAD <file>`                | <ul><li>將儲存庫的 HEAD 版本的 `<file>` 取出至工作目錄 (HEAD)</li><li>工作目錄的 `<file>` 會變成 HEAD 版本的</li></ul> |
| `git checkout -- <file>`                  | <ul><li>將儲存庫的 HEAD 版本的 `<file>` 取出至工作目錄 (HEAD)</li><li>工作目錄的 `<file>` 會變成 HEAD 版本的</li></ul> |
| `git checkout -- .`                       | <ul><li>將儲存庫的 HEAD 版本的所有檔案取出至工作目錄 (HEAD)</li><li>工作目錄的所有檔案會變成 HEAD 版本的</li></ul> |
| `git branch <branchName>`                 | <ul><li>將工作目錄 (HEAD) 新增一個分支，名為 `<branchname>`</li></ul> |
| `git branch <branchName> <sha1>`          | <ul><li>將 `<sha1>` 新增一個分支，名為 `<branchName>`</li></ul> |
| `git branch -D <branchName>..`            | <ul><li>刪除名為 `<branchName>` 的分支</li></ul> |
| `git checkout <branchName>`               | <ul><li>將儲存庫名為 `<branchName>` 的所有資料取出至工作目錄 (HEAD)</li><li>工作目錄會移動至 `<branchName>`</li></ul>|
| `git merge <branchName>` | <ul><li>將<branchName>合併到工作目錄(HEAD)</li></ul> |
| `git merge --abort` | <ul><li>中止合併：如果你在合併過程中遇到衝突，並且不希望解決這些衝突，可以使用 `git merge --abort` 來取消合併操作</li><li>恢復狀態：`git merge --abort` 會將儲存庫恢復到合併開始之前的狀態，這意味著任何合併過程中產生的變更都會被撤銷</li></ul> |
| `git cherry-pick <sha1>`| <ul><li>通常是把已發佈的分支修正bug之後,把同一個bug也在其他分支中修復</li></ul> |
| `git reset --soft <commit>`| <ul><li>移動 (HEAD)，保留暫存區和工作目錄</li></ul> |
| `git reset --mixed <commit>`| <ul><li>移動 (HEAD) 和暫存區，保留工作目錄</li></ul> |
| `git reset --hard <commit>`| <ul><li>移動 (HEAD)，重置暫存區和工作目錄</li></ul> |
| `git reflog `| <ul><li>查看 (HEAD) 的變動歷史</li><li>找回丟失的提交：當使用 `git reset --hard` 或其他命令丟失了提交時，可以通過 reflog 找回。</li></ul> |
| `git rebase `| <ul><li>將工作目錄 (HEAD) 的所有紀錄嫁接到 <branchName> 分支上</li></ul> |
| `git stash `| <ul><li>把目前工作目錄的變更，存放到git內部的暫存堆疊</li><li>將工作目錄還原至 (HEAD) </li></ul> |
| `git stash list `| <ul><li>列出目前已經存放在暫存堆疊的內容</li></ul> |
| `git stash pop `| <ul><li>還原暫存堆疊的內容</li></ul> |
| `git stash drop `| <ul><li>刪除暫存堆疊的內容</li></ul> |
| `git revert <sha1> `| <ul><li>常發生在 <sha1> 的變更內容錯誤，需要還原的時候</li></ul> |
| `git diff --cached `| <ul><li>顯示暫存區的所有變更</li></ul> |
| `git diff --name-status `| <ul><li>顯示工作目錄的所有檔案狀態</li></ul> |
| `git log -S <keyword> `| <ul><li>在儲存庫內做搜尋</li></ul> |
| `git log --since --until `| <ul><li>常發生在 <sha1> 的變更內容錯誤，需要還原的時候</li></ul> |
| `git log --author `| <ul><li>在儲存庫內限定作者搜尋</li></ul> |
| `git log -n <number> <sha1> `| <ul><li>只顯示最新的 n 筆 commit </li></ul> |
| `git revert <sha1> `| <ul><li>常發生在 <sha1> 的變更內容錯誤，需要還原的時候</li></ul> |
| `git log --all --decorate --oneline --graph --color=always `| <ul><li>顯示樹狀結構</li></ul> |
| `git bisect `| <ul><li>使用二元搜尋法找出變更的起始點</li><li>常用來找出 bug 發生源頭</li></ul> |
| `gitignore `| <ul><li>常用的可執行檔、暫存檔、套件管理工具上面</li><li>.DS_Store</li><li>*.tmp</li><li>*.bak</li><li>機密性資料</li><li>https://gitignore.io</li></ul> |
| `git branch -av `| <ul><li>列出所有分支</li></ul> |
| `git branch --set-upstream-to=origin/<branchName> `| <ul><li>設定遠端分支</li></ul> |
| `git push origin :<branchName> `| <ul><li>刪除遠端分支</li></ul> |
| `git remote prune origin `| <ul><li>刪除已經沒有遠端分支的遠端追蹤分支</li></ul> |    