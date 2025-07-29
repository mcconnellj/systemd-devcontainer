# A Simple Systemd Devcontainer

[![Open in Dev Containers](https://img.shields.io/static/v1?label=Dev%20Containers&message=Open&color=blue&style=flat)](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/Chuxel/systemd-devcontainer)
![GitHub Stars](https://img.shields.io/github/stars/chuxel/systemd-devcontainer?style=flat)


![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat) 
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=flat&logo=ubuntu&logoColor=white) 

Devcontainers provide preconfigured development environments so you can start coding right away without extra setup. This repository is an example of a lightweight devcontainer setup that boots with systemd as PID 1 — ideal for running or testing services that require a real init system.

## Quickstart

Assuming you have VS Code and Docker installed you can click [here](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/Chuxel/systemd-devcontainer) to automaticaly: 
- Install the Dev Containers extension if necessary
- Clone this repo into a container [volume](https://code.visualstudio.com/remote/advancedcontainers/improve-performance#_use-clone-repository-in-container-volume)
- Start the dev container

## Manual Installation

1. Install the code editor application [VS Code](https://code.visualstudio.com/)
2. Use the VS Code extensions tab to install the [Dev Containers Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers).
3. Install and configure [Docker](https://www.docker.com/get-started) for your operating system:
    - Windows & macOS: Install [Docker Desktop for Mac/Windows](https://www.docker.com/products/docker-desktop).
    - Linux: Install [Docker CE/EE for Linux](https://docs.docker.com/install/#supported-platforms) use `sudo usermod -aG docker $USER` to authorize your user before logging out and back in.

## Usage

```bash
# Clone the repository
git clone https://github.com/Chuxel/systemd-devcontainer.git

# Open the folder in VS Code
code systemd-devcontainer

# Press F1 and "Reopen In Container"
```

Run inside the container!

```bash
# Confirm systemd is PID 1
ps -p 1 -o comm=
```

## License

The MIT License lets you use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the project — for personal or commercial use. Just keep the original license text included. No warranties are provided.

## Credits

Created by [@Chuxel](https://github.com/Chuxel).

His work on this repo is simple and effective. As if crafted by a true wizard! Please ⭐ star the repo to show your support. — README author [@mcconnellj](https://github.com/mcconnellj)