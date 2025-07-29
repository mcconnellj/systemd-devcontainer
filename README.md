# A Simple Systemd Devcontainer

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat) 
![GitHub Stars](https://img.shields.io/github/stars/chuxel/systemd-devcontainer?style=flat) 
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=flat&logo=ubuntu&logoColor=white) 
[![Open in Dev Containers](https://img.shields.io/static/v1?label=Dev%20Containers&message=Open&color=blue&style=flat)](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/Chuxel/systemd-devcontainer)

Devcontainers provide preconfigured development environments so you can start coding right away without extra setup. This repository is an example of a lightweight devcontainer setup that boots with systemd as PID 1 — ideal for running or testing services that require a real init system.

## Quickstart

Assuming you have installed VS Code and Docker installed you can click [here](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/Chuxel/systemd-devcontainer) to automaticaly: Install the Dev Containers extension if necessary, clone the repo into a container [volume](https://code.visualstudio.com/remote/advancedcontainers/improve-performance#_use-clone-repository-in-container-volume), and start the dev container.

## Manual Installation

- Install the code editor application [VS Code](https://code.visualstudio.com/)
- Use the VS Code extensions tab to install the [Dev Containers Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers).
- Install and configure [Docker](https://www.docker.com/get-started) for your operating system:
    - Windows & macOS: Install [Docker Desktop for Mac/Windows](https://www.docker.com/products/docker-desktop).
    - Linux: Install [Docker CE/EE for Linux](https://docs.docker.com/install/#supported-platforms) use `sudo usermod -aG docker $USER` to authorize your user before logging out and back in.

## Usage

VS Code commands manage your editor. The Dev Containers extension adds to the existing list of commands, allowing for the creation and management of your development containers.

You can access commands two ways:

- Press F1 (or Ctrl+Shift+P / Cmd+Shift+P on Mac) to open the Command Palette  
- Or type `>` in the command bar, then type Dev Containers to see available commands in the search bar

Common commands include:

- Dev Containers: Open Folder in Container  
- Dev Containers: Rebuild Container  
- Dev Containers: Open Container Configuration File  
- Dev Containers: Clone Repository in Container Volume  
- Dev Containers: Open in Container from URL

To verify that systemd is running as PID 1 inside the container, run:

```bash
ps -p 1 -o comm=
