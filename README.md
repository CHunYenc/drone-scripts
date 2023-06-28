# drone-scripts

offical link: https://www.drone.io/

# 使用教學

建立 ```.env```，可以直接複製 ```.env.sample```

```yml
#################################################
# 以下為 DRONE SERVER 與 RUNNER 都需要
#################################################

# 如果有 HOST 與 Client, 必須一樣
DRONE_RPC_SECRET=?

#################################################
# 以下為 DRONE-SERVER 的設定
#################################################

# DRONE GITEA SERVER URL 簡單來說就是你的 GIT URL
DRONE_GITEA_SERVER=http://??:??/
# 到 DRONE GITEA 申請的 ID 與 SECRET
DRONE_GITEA_CLIENT_ID=??
DRONE_GITEA_CLIENT_SECRET=??
# DRONE SERVER ADMIN
DRONE_USER_CREATE=username:??,admin:true
# DRONE SERVER 瀏覽的網址
DRONE_SERVER_HOST=http://??:??
DRONE_SERVER_PROTO=http
DRONE_TLS_AUTOCERT=false
# 如果是要部署 SSL 環境時，要使用下面的方式
# DRONE_SERVER_PROTO=https
# DRONE_TLS_AUTOCERT=true

# 限制 DRONE CI/CD 的使用者
# DRONE_USER_FILTER=
# LOGS 有顏色
DRONE_LOGS_COLOR = true
# 檢查 GIT 有沒有要執行 CI/CD 的任務, 間格設定一分鐘檢查
DRONE_CRON_INTERVAL=1m

#################################################
# 以下為 DRONE-RUNNER 的設定
#################################################

DRONE_RUNNER_CAPACITY=2
DRONE_RUNNER_NAME=docker-runner
DRONE_RPC_HOST=drone-server:80
DRONE_RPC_PROTO=http
```

# 如何創建 DRONE_RPC_SECRET

```
$ openssl rand -hex 16
beaxxxxx26a222xxxxxxxx <-- copy this
```