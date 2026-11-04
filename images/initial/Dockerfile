FROM ghcr.io/astral-sh/uv:bookworm AS builder

ENV UV_COMPILE_BYTECODE=1 UV_LINK_MODE=copy
ENV UV_PYTHON_INSTALL_DIR=/python
ENV UV_PYTHON_PREFERENCE=only-managed


WORKDIR /app

COPY requirements.txt .

RUN uv venv --python 3.12

RUN uv pip install -r requirements.txt

FROM debian:bookworm

COPY --from=builder /python /python
COPY --from=builder /app /app

ENV PATH="/app/.venv/bin:$PATH"

WORKDIR /app

COPY . .

ENTRYPOINT []

