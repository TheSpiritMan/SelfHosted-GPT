# Ollama Only

- Here is a guide to run `ollama` only in docker container.
- You can expose this `ollama` container for application running in different servers.
- For that, you can simply `docker-compose.yaml` file.
- Command:
    ```
    docker exec ollama-only ollama pull nomic-embed-text:latest 
    docker exec ollama-only ollama pull mistral:latest
    ```

## More Details
- For more details, visit this [official page](https://ollama.com/) of <b>Ollama</b>.