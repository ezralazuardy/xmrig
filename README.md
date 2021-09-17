# 🪙 xmrig

A custom configured xmrig cypto miner that work best in cloud.

### Requirements

- Cloud / VPS with `linux` operating system
- Having minimal 1 core vCPU (2 vCPU is recommended)
- Having minimal 4GB RAM (8GB is recommended if the server is used for other process, e.g. web server)

### Installation

- Clone this repository to your Cloud / VPS in `/etc/xmrig/` directory (running `git clone` with `sudo` is recommended)
- Run `sudo chown -R <user>:<user> /etc/xmrig`, make sure to change the `<user>` with your username
- Configure the miner by running `./config`
- Run the boost script (usage read below) by running `./boost`
- Run the 1GB pages enabler script (usage read below) by running `./enable_1gbp`
- Run the clear cache script (usage read below) by running `./clear_cache`
- Finally, start the miner by running `./start`

> The current miner session can be viewed by running `./monitor`

### Usage

- './config` will open the editor for miner configuration
- `./start` will start the miner in linux screen session
- `./monitor` will monitor the current miner session
- `./boost` will apply a CPU register patch for your device (works on machine host only, virtual machine will not be affected)
- `./enable_1gbp` will apply a CPU 1GB pages patch (works on supported CPU only)
- `./clear_cache` will clear the cache in current machine (not recommended to be used when miner is running)

> This repository is based on the original xmrig [v6.15.0](https://github.com/xmrig/xmrig/releases/tag/v6.15.0) for linux
