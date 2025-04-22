FROM python:3.12-slim

RUN pip install --no-cache-dir uv mcp-server-time mcp-proxy

ENV TZ=Europe/Paris \
    # mcp-proxy listens on 0.0.0.0:8080 and spawns the stdio server
    PROXY_CMD='mcp-proxy --sse-host 0.0.0.0 --sse-port 8080 -- \
                 uvx mcp-server-time --local-timezone=Europe/Paris'

EXPOSE 8080
ENTRYPOINT [ "sh", "-c", "$PROXY_CMD" ]
