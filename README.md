
# WireVPN - Simplified WireGuard Connection Management

WireVPN is a script designed to simplify the process of managing WireGuard VPN connections on Linux systems.

## Main Goal
The primary objective of WireVPN is to provide a streamlined interface for connecting and disconnecting to WireGuard VPNs with minimal command-line input.

## Requirements
- Operating System: Linux (Tested on Ubuntu 22.04 LTS)
- Dependencies: WireGuard must be installed and configured on the system.
- Additional Requirements: `wg-quick` should be available for managing connections.

## Installation
To install the WireVPN script, you can either copy the file directly into `/usr/local/bin` for global access or add the script's repository folder to your `PATH`.

### Copying to /usr/local/bin
```bash
sudo cp wirevpn /usr/local/bin/wirevpn
sudo chmod +x /usr/local/bin/wirevpn
```

### Adding to PATH
If you prefer not to copy the script, you can add the directory containing `wirevpn` to your `PATH` by editing your `~/.bashrc` or `~/.profile` and adding:
```bash
export PATH="$PATH:/path/to/your/wirevpn/directory"
```
Remember to replace `/path/to/your/wirevpn/directory` with the actual directory path where the script is located.

## Usage
To manage your WireGuard connections, use the following commands:

- To connect to a VPN using a specific configuration file:
  ```bash
  sudo wirevpn connect [config_name]
  ```
  If no configuration is specified, it will attempt to use the last successful configuration.

- To disconnect from the current WireGuard VPN:
  ```bash
  sudo wirevpn disconnect
  ```

- To list all available VPN configurations:
  ```bash
  sudo wirevpn list
  ```

- For help and a list of commands:
  ```bash
  sudo wirevpn help
  ```
  You can also use `sudo wirevpn --help` or `sudo wirevpn -h` to view the help information.

## Support
This script is a third-party tool and is not officially associated with the WireGuard project. Please ensure that you have a working WireGuard setup before using WireVPN.