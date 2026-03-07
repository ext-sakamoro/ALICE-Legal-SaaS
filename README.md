# ALICE-Legal SaaS

Deterministic legal tree compilation and contract API

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum, ALICE-Legal |

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST /api/v1/compile` | 法律文書コンパイル |
| `POST /api/v1/execute` | 契約実行 |
| `GET  /api/v1/templates` | 法律テンプレート一覧 |
| `GET`  | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
