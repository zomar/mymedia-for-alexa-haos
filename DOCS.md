# My Media for Alexa - Home Assistant Add-on

Stream your personal music library to Amazon Alexa devices.

## About

My Media for Alexa is a media server that allows you to play your personal music
collection through Amazon Alexa-enabled devices. This add-on runs the My Media
for Alexa service inside Home Assistant OS using the official Docker images hosted
on Docker Hub.

## Installation

1. Navigate to **Settings → Add-ons → Add-on Store** in Home Assistant.
2. Click the menu (⋮) and select **Repositories**.
3. Add this repository URL and click **Add**.
4. Find **My Media for Alexa** in the store and click **Install**.

## Configuration

### Options

| Option | Type | Default | Description |
|--------|------|---------|-------------|
| `log_to_console` | bool | `true` | Enable logging to the add-on log output |
| `ffmpeg_tmp_dir` | str | `/tmp` | Temporary directory used by ffmpeg for transcoding |

### Media Library

Your music files should be placed (or bind-mounted) under `/share/mymedia/medialibrary`
on your Home Assistant host. This maps to `/medialibrary` inside the container.

## Ports

| Port | Protocol | Description |
|------|----------|-------------|
| 52050 | TCP | HTTP |
| 52051 | TCP | HTTPS |

Once running, access the My Media for Alexa web interface at:

```
http://<your-ha-ip>:52050
```

## Support

- Website: https://www.mymediaforalexa.com
- GitHub: https://github.com/bizmodeller/mymedia-for-alexa-haos
