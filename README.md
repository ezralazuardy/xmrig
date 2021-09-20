# 🪙 xmrig

A custom configured xmrig CPU cypto miner that work best in linux cloud.

> This repository is based on the original xmrig [v6.15.0](https://github.com/xmrig/xmrig/releases/tag/v6.15.0) for linux.

## 👌 Requirements

- Cloud / VPS machine with `linux` operating system (Ubuntu 18+ is recommended).
- Having minimal 1 core vCPU (2 vCPU is recommended).
- Having minimal 4GB RAM (8GB is recommended if the machine is used for other process, e.g. web server).

## 📥 Installation

### Automated

- Run `wget -O - https://raw.githubusercontent.com/ezralazuardy/xmrig/main/install | bash`

> Currently the script only support Ubuntu 18+ OS.<br/>
> The script will automatically reboot your machine after successfully executed.<br/>
> xmrig will be installed in `/etc/xmrig` directory.

### Manual

- Install [git](https://command-not-found.com/git) and [msr-tools](https://command-not-found.com/wrmsr) on your operating system.
- Clone this repository to `/etc/xmrig/` directory (running `git clone` with `sudo` is recommended).
- Configure the miner by running `./config`.
- Run the boost script by running `./boost`.
- Run the 1GB pages enabler script by running `./enable_1gbp`.
- Run the clear cache script by running `./clear_cache`.
- Finally, start the miner by running `./start`.

> The current miner session can be viewed by running `./monitor`.

## 🔨 Command Usage

| Command         | Description                                                                                                                        |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| `./install`     | Install the xmrig to `/etc/xmrig/` directory<br/>(this command will remove the previous xmrig installation).                       |
| `./config`      | Open the editor for miner configuration.                                                                                           |
| `./start`       | Start the miner in the linux screen session.                                                                                       |
| `./stop`        | Stop the current miner session.                                                                                                    |
| `./monitor`     | Display the current miner session.                                                                                                 |
| `./boost`       | Apply a CPU register patch for 15% more miner performace<br/>(works on a real machine only, virtual machine will not be affected). |
| `./enable_1gbp` | Apply a CPU 1GB pages patch for 30% more miner performace<br/>(works on the [supported CPUs] only). |
| `./clear_cache` | Clear the cache in current machine (not recommended to be used when miner is running).                                             |

## ⚠️ Warning

Since many Cloud / VPS provider prohibit any cryptocurrency mining activity in their platform, it's recommended to only run 1 instance of this miner on a single machine.

Highly recommended to set the `max-threads-hint` configuration to `50`. For more details, check out [here](https://github.com/xmrig/xmrig/blob/beta/doc/CPU_MAX_USAGE.md). Configuring the script to run with delay or scheduler is also recommended to bypass the cloud platform anti-fraud system for suspicious activity (if cryptocurrency mining is not eligible by their term of services).

**I'm not responsible for any damage or loss as a result of using this tool.**

**This repository is open source and licensed with [MIT License](https://github.com/ezralazuardy/xmrig/blob/main/LICENSE.md).**

[supported CPUs]: https://itectec.com/superuser/which-cpus-support-1gb-pages/
