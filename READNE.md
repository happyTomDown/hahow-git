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



## checkout , branch
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

