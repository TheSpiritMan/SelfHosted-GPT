# Use the specified Python base image
FROM python:3.11-slim

# Set the working directory in the container
WORKDIR /app

# Install necessary packages
RUN apt-get update && apt-get install -y \
    git \
    build-essential

# Clone the private repository
RUN git clone https://github.com/imartinez/privateGPT

WORKDIR /app/privateGPT

# Install poetry
RUN pip install poetry && \
# Lock and install dependencies using poetry
     poetry lock && \
     poetry install --extras "ui llms-ollama embeddings-ollama vector-stores-qdrant"

ENV PGPT_PROFILES ollama

CMD ["make", "run"]
