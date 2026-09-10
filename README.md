# chatproxy-api

FastAPI gateway in front of an LLM with response caching

## What it does

- SHA-256 keyed in-memory response cache
- POST /v1/chat with prompt/model/max_tokens
- Latency measured and returned per request
- Provider SDK plugs into one function

## How to use

```bash
curl localhost:8000/v1/chat \
  -H 'content-type: application/json' \
  -d '{"prompt": "hello", "model": "gpt-4o-mini"}'
```

## Install

```bash
pip install -r requirements.txt
uvicorn main:app --reload
```

## Project structure

```text
├── .github/
│   ├── workflows/
│   │   └── ci.yml
│   └── dependabot.yml
├── docs/
│   ├── configuration.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── .gitignore
├── CHANGELOG.md
├── CONTRIBUTING.md
├── SECURITY.md
├── main.py
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
```

## 说明

个人练习项目, 谨慎用于生产环境。
