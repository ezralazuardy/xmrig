<a href="https://en.wikipedia.org/wiki/X86-64"><img src="https://img.shields.io/badge/platform-linux--64-blue" alt="license" target="_blank" rel="noopener noreferrer"></a>
<a href="https://github.com/ezralazuardy/xmrig/releases"><img src="https://img.shields.io/github/v/release/ezralazuardy/xmrig" alt="license" target="_blank" rel="noopener noreferrer"></a>
<a href="https://github.com/ezralazuardy/xmrig/blob/main/LICENSE.md"><img src="https://img.shields.io/github/license/ezralazuardy/xmrig" alt="license" target="_blank" rel="noopener noreferrer"></a>
<a href="https://github.com/ezralazuardy/xmrig/issues"><img src="https://img.shields.io/github/issues/ezralazuardy/xmrig?color=red" alt="issues" target="_blank" rel="noopener noreferrer"></a>

# 🪙 xmrig

A custom configured xmrig CPU cypto miner that work best in linux machine.

> This repository is based on the original xmrig [v6.15.0](https://github.com/xmrig/xmrig/releases/tag/v6.15.0) for linux.

## 👌 Requirements

- Cloud / VPS machine with `linux` operating system (Ubuntu 18+ is recommended).
- Having minimal 1 core vCPU (2 vCPU is recommended).
- Having minimal 4GB RAM (8GB is recommended if the machine is used for other process, e.g. web server).

## 📥 Installation

#### Automated

- Run `wget -O - https://raw.githubusercontent.com/ezralazuardy/xmrig/main/install | bash`

> Currently the script only support Ubuntu 18+ OS.<br/>
> The script will automatically reboot your machine after successfully executed.<br/>
> xmrig will be installed in `/etc/xmrig` directory.

#### Manual

- Install [git](https://command-not-found.com/git) and [msr-tools](https://command-not-found.com/wrmsr) on your operating system.
- Clone this repository to `/etc/xmrig/` directory (running `git clone` with `sudo` is recommended).
- Configure the miner by running `/etc/xmrig/config`.
- Run the boost script by running `/etc/xmrig/boost`.
- Run the 1GB pages enabler script by running `/etc/xmrig/enable_1gbp`.
- Run the clear cache script by running `/etc/xmrig/clear_cache`.
- Finally, start the miner by running `/etc/xmrig/start`.

> The current miner session can be viewed by running `/etc/xmrig/monitor`.

## 🔨 Commands

| Command                  | Description                                                                                                                        |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------- |
| `/etc/xmrig/install`     | Install the xmrig to `/etc/xmrig/` directory<br/>(this command will remove the previous xmrig installation).                       |
| `/etc/xmrig/config`      | Open the editor for miner configuration.                                                                                           |
| `/etc/xmrig/start`       | Start the miner in the linux screen session.                                                                                       |
| `/etc/xmrig/stop`        | Stop the current miner session.                                                                                                    |
| `/etc/xmrig/monitor`     | Display the current miner session.                                                                                                 |
| `/etc/xmrig/boost`       | Apply a CPU register patch for 15% more miner performace<br/>(works on a real machine only, virtual machine will not be affected). |
| `/etc/xmrig/enable_1gbp` | Apply a CPU 1GB pages patch for 30% more miner performace<br/>(works on the [supported CPUs] only).                                |
| `/etc/xmrig/clear_cache` | Clear the cache in current machine<br/>(not recommended to be used when the miner is running).                                     |

## ⚠️ Warning

Since many Cloud / VPS provider prohibit any cryptocurrency mining activity in their platform, it's recommended to only run 1 instance of this miner on a single machine.

Highly recommended to set the `max-threads-hint` miner configuration to `50`. For more details, check out [here](https://github.com/xmrig/xmrig/blob/beta/doc/CPU_MAX_USAGE.md). Configuring the script to run with delay or scheduler is also recommended to bypass the cloud platform anti-fraud system for suspicious activity (if cryptocurrency mining is not eligible by their term of services).

**I'm not responsible for any damage or loss as a result of using this tool.**

**This repository is open source and licensed with [MIT License](https://github.com/ezralazuardy/xmrig/blob/main/LICENSE.md).**

[supported CPUs]: https://itectec.com/superuser/which-cpus-support-1gb-pages/
