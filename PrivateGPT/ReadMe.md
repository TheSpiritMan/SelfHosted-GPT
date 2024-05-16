# Private GPT
- Here I have tried to run `PrivateGPT` and `ollama` in docker container.
- Before Running PrivateGPT, you will have to download `mistral:latest` and `nomic-embed-text:latest` ollama models so it can be used by privategpt docker container.
- For that, follow [Ollama-only]() guide.
- Use `docker-compose.yaml` file to start `privategpt` and `ollama` in docker container.
- Wait until you see below log from privategpt container:
    ```
    [INFO    ] llama_index.core.indices.loading - Loading all indices.
    [INFO    ] private_gpt.components.ingest.ingest_component - Creating a new vector store index
    Parsing nodes: 0it [00:00, ?it/s]
    Generating embeddings: 0it [00:00, ?it/s]
    [INFO    ]   matplotlib.font_manager - generated new fontManager
    [INFO    ]         private_gpt.ui.ui - Mounting the gradio UI, at path=/
    [INFO    ]             uvicorn.error - Started server process [7]
    [INFO    ]             uvicorn.error - Waiting for application startup.
    [INFO    ]             uvicorn.error - Application startup complete.
    [INFO    ]             uvicorn.error - Uvicorn running on http://0.0.0.0:8001 (Press CTRL+C to quit)
    ```

- And `ollama` logs must be:
    ```
    level=INFO source=images.go:704 msg="total blobs: 0"
    level=INFO source=images.go:711 msg="total unused blobs removed: 0"
    level=INFO source=routes.go:1054 msg="Listening on [::]:11434 (version 0.1.38)"
    ```

- Then visit `http://localhost:8080` in your browser to play with `privategpt` and `ollama`.

## More Details
- For more details, visit this [official page](https://docs.privategpt.dev/) of <b>PrivateGPT</b>.