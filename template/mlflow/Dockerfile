# Start from a slim python base image to keep the container size as small as possible.
FROM python:3.13-slim
COPY --from=ghcr.io/astral-sh/uv:latest /uv /uvx /bin/

# Set the working directory to copy uv project files.
WORKDIR /workdir

# Increase the HTTP request timeout to prevent issues for large experiments.
ENV MLFLOW_HTTP_REQUEST_TIMEOUT=3600

# Set the shell to bash instead of sh, using pipefail to identify silent pipe errors.
SHELL ["/bin/bash", "-o", "pipefail", "-c"]

# Expose port 5000 to expose the MLflow web interface.
EXPOSE 5000

# Copy uv project files so uv knows to install MLflow.
COPY pyproject.toml /workdir/
