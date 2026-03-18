# Linux 作業系統實務筆記 (Practice of Linux Operating System)

---

## Linux 基本指令
* 目錄、檔案：`ls` (加上 `-a` 可以看隱藏檔)
* 目前 IP：`ip address show` (或 `ifconfig`)
* 使用者身分查詢：`id [使用者名稱]`
* `|` 管道：類似生產線，將前面的結果傳給後面 (例如配合 `grep` 過濾文字)

---

## Linux 基本架構
* 架構層次：kernel > shell (bash、tcsh、sh...) > application
  * 不同 shell 有不同前綴詞
  * `exit` 或 `Ctrl+D` 可回到原本的殼
* **這學期教的Linux版本是ubuntu 24.04**
* 採用 LTS (Long term support)

---

## Linux 使用實務

### 快照與電源
* snapshot：類似存檔/紀錄點
* **系統管理者叫root** (管理者權限最高)
* **管理者的ｉｄ是０**
* 提權指令：`sudo su` (su = super user = root)
* **一般使用者提示符號是$ 管理者提示符號是#**
* whoami：知道自己現在的身分
* hostname：機器名稱

#### 關機指令 (Terminal)
* poweroff：立即關機
* halt -p
* shutdown -h now：可調整時間的關機指令

### 遠端連線與 SSH
* 安裝與啟動：
  1. `sudo apt update` (更新清單)
  2. `sudo apt install openssh-server -y` (安裝)
  3. `sudo systemctl status ssh` (檢查狀態)
* 防火牆放行：`sudo ufw allow ssh`
* 連線指令：`ssh user@ip` (可用 Windows 的 PowerShell 連線)

### 軟體與環境設定
* 軟體管理：`sudo apt remove` (移除)、`sudo apt purge` (徹底清除)
* 過濾資料：`grep` (顯示符合行)、`grep -v` (排除符合行)
* 隱藏概念：檔名開頭有 `.` 的是隱藏檔 (例如 `.env`)
* Token 設定：在 `.env` 檔案中，金鑰引號必須成對 (例如 `TOKEN="key"`)

### 操作小撇步
* Ctrl + C：強制終止執行中的程式 (當畫面卡住或沒反應時)
* Ctrl + O：Nano 編輯器存檔
* Ctrl + X：Nano 編輯器離開
* 上鍵 (↑)：翻閱歷史指令紀錄
