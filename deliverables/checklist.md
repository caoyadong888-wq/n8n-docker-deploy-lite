# Lite checklist / 精简清单

SQLite only. The Postgres profile, the config checker, and the long checklist are in the full pack.

## Volumes / 数据卷

Keep a volume on `/home/node/.n8n`. n8n docs say that directory holds the encryption key. With SQLite, the database file is `~/.n8n/database.sqlite`.

把卷挂到 `/home/node/.n8n`。n8n 文档说明加密密钥在这个目录。SQLite 的库文件是 `~/.n8n/database.sqlite`。

## Timezone / 时区

Set `TZ` and `GENERIC_TIMEZONE` to the same IANA name. The example uses `Asia/Shanghai`. n8n docs: `TZ` is the container clock, and `GENERIC_TIMEZONE` is what Schedule Trigger uses.

`TZ` 和 `GENERIC_TIMEZONE` 用同一个 IANA 时区。示例是 `Asia/Shanghai`。

## Webhook URL / Webhook 地址

Set `N8N_WEBHOOK_URL` to `https://n8n.example.com/` with the trailing slash. n8n docs: `N8N_WEBHOOK_URL` is the name from n8n 2.30.0, and `WEBHOOK_URL` is deprecated from n8n 2.35.0. Set `N8N_PROXY_HOPS=1` for one proxy. Check upstream docs.

`N8N_WEBHOOK_URL` 设为 `https://n8n.example.com/`，末尾保留斜杠。一层反代时 `N8N_PROXY_HOPS=1`。Check upstream docs.

## Proxy / 反代

`nginx-n8n.conf` proxies `n8n.example.com` to `127.0.0.1:5678`. Replace the certificate paths. This folder does not reload host nginx.

`nginx-n8n.conf` 把 `n8n.example.com` 反代到 `127.0.0.1:5678`。换掉证书路径。这里不会重载宿主机的 nginx。
