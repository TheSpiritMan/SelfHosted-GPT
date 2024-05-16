# Open WebUI
- Here I have tried to run `open-webui` and `ollama` in docker container.
- `Open WebUI` is more chatgpt friendly UI which allows us to manage LLM models directly through UI.
- For this, you do not need any models to be present by default. You can download and manage all the models from UI settings.
- Use `docker-compose.yaml` file to start `open-webui` and `ollama` in docker container.
- Wait until you see below log from privategpt container:
    ```
    INFO:     Application startup complete.
    INFO:apps.litellm.main:Subprocess started successfully.
    INFO:     Uvicorn running on http://0.0.0.0:8080 (Press CTRL+C to quit)
    ```

- And `ollama` logs must be:
    ```
    level=INFO source=images.go:704 msg="total blobs: 0"
    level=INFO source=images.go:711 msg="total unused blobs removed: 0"
    level=INFO source=routes.go:1054 msg="Listening on [::]:11434 (version 0.1.38)"
    ```

- Then visit `http://localhost:8080` in your browser to play with `privategpt` and `ollama`.

- You must create account to access Open Web UI portal. Just click in `Sign Up` option. The first created account is admin account which can be used to manage all LLM models. 


## More Details
- For more details, visit this [official page](https://openwebui.com/) of <b>Open WebUI</b>.