# drone-scripts

offical link: https://www.drone.io/

# 使用教學

建立 ```.env```，可以直接複製 ```.env.sample```

```yml
# Github 設定 OAuth
DRONE_GITHUB_CLIENT_ID=?
DRONE_GITHUB_CLIENT_SECRET=?

# 設定管理員
DRONE_USER_CREATE=username:?,admin:true

# 設定可以使用的使用者或組織
DRONE_USER_FILTER=?
DRONE_SERVER_HOST=0.0.0.0:8080

# 架在 http
DRONE_SERVER_PROTO=http
DRONE_TLS_AUTOCERT=false

# 架在 https
# DRONE_SERVER_PROTO=https
# DRONE_TLS_AUTOCERT=true

# 下面有生成的指令
DRONE_RPC_SECRET=?

DRONE_RUNNER_CAPACITY=3
DRONE_CRON_INTERVAL=1m

DRONE_RUNNER_NAME=docker-runner
DRONE_RPC_HOST=drone-server:80
```

# 如何創建 DRONE_RPC_SECRET

```
$ openssl rand -hex 16
beaxxxxx26a222xxxxxxxx <-- copy this
```