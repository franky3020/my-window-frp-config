# my-window-frp-config

## inner-client
需從 frpc.ini.example 複製一份 重新命名為 frpc.ini
再設定機密文件


* docker build -t frp .
* docker container rm -f frp
* docker run -d --restart always --name frp frp

## 設定host

127.0.0.1 gitlab.com
127.0.0.2 redmine.com

