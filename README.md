# ubuntu-script.sh
 * 這是一個全自動設定 Centos7 的全自動懶人腳本。
 * 版本是 ubuntu 20.04測試安裝
# 執行前準備工作
## 安裝 ubuntu
* 下載 ubuntu-20.04.1-live-server-amd64
* 安裝 ubuntu 並設定網卡IP，讓伺服器可以上網
* 安裝好 OpenSSH 與建立使用者
## 切換到root (有的人怕安全性問題，如果擔心請自行想辦法)
### 方法一: 
```
sudo -s
```
### 方法二: 
```
sudo passwd root
su -
```
## 設定腳本權限
* chmod +x centos-script.sh 讓他有執行權限
* 使用 root 最高權限管理員執行
# 他做了哪些事情
* 初始化系統:他會將環境設定成台灣時區，語言，並更新最新版的yum 倉儲。
* 安裝基本常用的網管軟體，像是 p7zip ftp screen telnet等等的。
* 將內建防火牆關閉，使用老牌 iptables 防火牆，設定檔案內容是 鳥哥 抄過來的，並稍微調整功能。
* 安裝 docker
* 安裝 MariaDB 
* 安裝 apache
* 安裝 NGINX (測試功能 還沒完成，懶得換nginx)
* 安裝 PHP 可自選版本
* 安裝 vsftpd FTP Server
* 安裝 squid Proxy Server


