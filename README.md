# Linux
Practice of Linux Operating System

---
## Linux基本指令
* 目錄、檔案 ls  
* 目前ip ip address show  
* 使用者身分查詢 id +使用者名稱  
---
## Linux基本架構
* kernel > shell(bash、tcsh、sh...) > application  
  * 不同shell有不同前綴詞  
  * exit或ctrl+D回到原本的殼  
**這學期教的Linux版本是ubuntu 24.04**  
* 分大小寫
* 採用LTS(Long term support)  

---
## Linux使用
### 快照
snapshot > 類似儲存  

### 電源關閉
* **系統管理者叫root** 有時候會設定成系統管理者才能關閉電源
* **管理者的ｉｄ是０**
* 提權指令 sudo su > su=super user=root  
* **一般使用者提示符號是$ 管理者提示符號是#**  
* whoami > 知道自己現在的身分  
* hostname > 機器名稱  
#### UI介面
* suspend 休眠    
* restart 重啟  
* power off 關機  
#### 終端機指令
* poweroff 立即關機  
* halt -p  
* shutdown -h now 可調整時間  

### 釘選
* pin to dash  

