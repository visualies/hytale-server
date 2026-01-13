### Quick start

You need the official server files before starting. Choose one:

- **Manually copy** from your Launcher installation:
  ```
  Windows: %appdata%\Hytale\install\release\package\game\latest
  Linux: $XDG_DATA_HOME/Hytale/install/release/package/game/latest
  MacOS: ~/Application Support/Hytale/install/release/package/game/latest
  ```
- **Use the Hytale Downloader CLI**

Copy the downloaded `Server/` directory and `Assets.zip` into your mapped `/data` folder, then start the container. You'll be prompted to log in.

Enjoy


### Docker compose

```yaml
services:
  hytale:
    image: ghcr.io/visualies/hytale-server:latest
    environment:
      MAX_MEMORY: 8G
    volumes:
      - ./server-data:/data
    ports:
      - "5520:5520/udp"
    restart: unless-stopped
```
