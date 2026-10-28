FROM python:3.13-slim-bookworm
ARG APP_VERSION=dev
ENV APP_VERSION=$APP_VERSION PYTHONUNBUFFERED=1
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY app.py .
RUN useradd -r -u 10001 appuser
USER appuser
CMD ["python", "app.py"]