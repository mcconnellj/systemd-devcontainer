# A Simple Systemd Devcontainer

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat) 
![GitHub Stars](https://img.shields.io/github/stars/chuxel/systemd-devcontainer?style=flat) 
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=flat&logo=ubuntu&logoColor=white) 
[![Open in Dev Containers](https://img.shields.io/static/v1?label=Dev%20Containers&message=Open&color=blue&style=flat)](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/Chuxel/systemd-devcontainer)

Devcontainers provide preconfigured development environments so you can start coding right away without extra setup. This repository is an example of a lightweight devcontainer setup that boots with systemd as PID 1 — ideal for running or testing services that require a real init system.

## Quickstart

If you already have VS Code and Docker installed, you can click the badge above or [here](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/microsoft/vscode-remote-try-java) to get started.  
It will install the Dev Containers extension if necessary, clone the repo into a container [volume](https://code.visualstudio.com/remote/advancedcontainers/improve-performance#_use-clone-repository-in-container-volume), and start up the dev container.

## Installation

1. Install [VS Code](https://code.visualstudio.com/) or [VS Code Insiders](https://code.visualstudio.com/insiders/) and this extension.

2. Install and configure [Docker](https://www.docker.com/get-started) for your operating system, using one of the paths below or an [alternative Docker option](https://code.visualstudio.com/remote/advancedcontainers/docker-options), like Docker on a remote host or Docker compliant CLI.

   **Windows / macOS:**

   1. Install [Docker Desktop for Mac/Windows](https://www.docker.com/products/docker-desktop).
   2. If not using WSL2 on Windows, right-click on the Docker task bar item, select **Settings / Preferences** and update **Resources > File Sharing** with any locations your source code is kept. See [tips and tricks](https://aka.ms/vscode-remote/containers/troubleshooting) for troubleshooting.
   3. To enable the [Windows WSL2 back-end](https://aka.ms/vscode-remote/containers/docker-wsl2): Right-click on the Docker taskbar item and select **Settings**. Check **Use the WSL2 based engine** and verify your distribution is enabled under **Resources > WSL Integration**.

   **Linux:**

   1. Follow the [official install instructions for Docker CE/EE](https://docs.docker.com/install/#supported-platforms). If you use Docker Compose, follow the [Docker Compose install directions](https://docs.docker.com/compose/install/).
   2. Add your user to the `docker` group by using a terminal to run: `sudo usermod -aG docker $USER` Sign out and back in again so this setting takes effect.

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
