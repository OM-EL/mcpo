# ./mcpo/Dockerfile
FROM python:3.12-slim
RUN pip install --no-cache-dir uv mcpo
WORKDIR /app
COPY config.json .
EXPOSE 8000
CMD ["uvx", "mcpo", "--host", "0.0.0.0", "--port", "8000", "--config", "/app/config.json"]
