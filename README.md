# n8n Docker Production Deploy (lite)

Free subset. SQLite Compose file, env example, nginx snippet, and a short checklist. The Postgres profile, the long bilingual checklist, and the config checker are in the full pack.

## English

### Deliverables

- `deliverables/docker-compose.yml` — n8n only, SQLite, loopback port 5678
- `deliverables/.env.example` — `n8n.example.com` and `CHECK_UPSTREAM_TAG`
- `deliverables/nginx-n8n.conf` — snippet for `n8n.example.com`
- `deliverables/checklist.md` — short volume, timezone, and webhook notes

Copy the env file and replace the tag before you start anything. Check upstream docs. This folder does not run `docker compose up`.

```bash
cp deliverables/.env.example .env
docker compose --env-file .env -f deliverables/docker-compose.yml config
```

Full version: GUMROAD_URL

## 中文

免费子集：SQLite 的 Compose、环境示例、nginx 片段和一份短清单。Postgres 配置档、完整的中英检查清单和配置检查命令在完整版里。

### 交付物

- `deliverables/docker-compose.yml` — 只有 n8n，SQLite，端口绑在本机 5678
- `deliverables/.env.example` — `n8n.example.com` 和 `CHECK_UPSTREAM_TAG`
- `deliverables/nginx-n8n.conf` — `n8n.example.com` 的片段
- `deliverables/checklist.md` — 数据卷、时区和 webhook 的短说明

先复制环境文件并换掉镜像标签。Check upstream docs。本目录不会执行 `docker compose up`。

Full version: GUMROAD_URL

## Delivery time / 交付时间

- Lite (this folder): free, available now. / 精简版（本目录）：免费，立即可用。
- Full version: instant download after purchase (GUMROAD_URL). / 完整版：购买后即时下载（GUMROAD_URL）。
