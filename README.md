![Dynamic JSON Badge](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fgithub.com%2Fflurbudurbur%2Fkurosearch%2Fraw%2Fmain%2Fpackage.json&query=%24.version&style=flat&label=Version&link=https%3A%2F%2Fgithub.com%2Fflurbudurbur%2Fkurosearch%2Freleases%2Flatest)

<div style="display: flex; place-content: center; padding: 1rem">
    <img src=".github/brand/logo.svg" alt="logo" height="100px"/>
    <img src=".github/brand/cross.svg" alt="cross" height="80px">
    <img src=".github/brand/docker.svg" alt="docker" height="80px">
</div>

# KuroSearch X Docker

A Project that aims to containerize Kurosearch to jork it in privacy. Self-host it if you want!

## Tag explanation

| Tag            | Description                         |
| :------------- | :---------------------------------- |
| `latest`       | Latest stable release (recommended) |
| `canary`       | Latest development build            |
| `x.y.z[-rc.n]` | Specific release                    |

## Getting Started

Prerequisites:

- [Docker](https://docs.docker.com/get-started/)
- rule34 API credentials

1. Clone the repository
    - If storage is a concern, You only need `compose.yaml`, `Caddyfile` and `.env` (renamed from `.env.example`).
    - Alternatively, you can clone the repo with limited history:
        - Command: `git clone --depth 1 https://github.com/flur34/flur34-composer.git`
2. Edit the .env file. Every variable is required! Don't edit the existing ones unless you know what you're doing.
3. Run `docker compose up -d`

### Bring your own reverse proxy

> The below instructions only cover the project-specific changes.
> You need to configure your own reverse proxy.

For users who want to plug this container into an existing reverse proxy, do the following:

1. Remove anything related to Caddy from the `compose.yaml`.
2. Map the internal port 8080 to your desired host port. All traffic is http.
3. `docker compose up -d [--remove-orphans]`

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## Got Issues?

Open 'em up in the issues tab (preferably) or contact me. Info below.

Discord: `@flurbudurbur`
Server: https://discord.gg/AxUnC7n9ZP
