# my-window-frp-config

## inner-client
這是在內網 需要deploy 的, 目標是將內網的 服務 可以從外往連接

```
local_port = 3389  // 這是內網的 port
remote_port = 33389 // 這是會讓 Relay-Station-Docker-container 所在機器開啟的入口, 所以該機器要設定此 port 的 防火牆
```

需從 frpc.ini.example 複製一份 重新命名為 frpc.ini
再設定機密文件

```
cd ./inner-client
docker build -t frp .
docker container rm -f frp
docker run -d --restart always --name frp frp
```
### windows 遠端
windows 遠端需要 有 udp 與 tcp 才能不會卡頓
windows 的本地 ip 需要先自行在本機電腦查詢出來





## 設定 host 教學

127.0.0.1 gitlab.com
127.0.0.2 redmine.com

