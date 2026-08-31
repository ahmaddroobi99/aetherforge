# aetherforge

**Scaffold only.** `pyproject.toml` describes an “enterprise AI control plane” (FastAPI, uvicorn, a CLI entry point `aetherforge.cli:main`) and `docker-compose.yml` tries to `pip install -e .` and serve on port 8080.

There is **no `src/` tree** in this repository. The declared 12 products, gateway, RAG, flags, and forensics are intent — they are not implemented here.

Until the package exists, `docker compose up` will fail on the missing module. Treat this as a name-holder, not a platform.
