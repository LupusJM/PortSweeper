## PortSweeper

PortSweeper is a lightweight Python tool designed for scanning open ports on a given target IP address (IPv4, IPv6) or URL. It offers flexibility in scanning TCP, UDP, or both types of ports with options for speed adjustment and additional functionalities like banner grabbing and reverse DNS lookup.

### How it works

PortSweeper utilizes Python's `socket` library to establish connections and scan for open ports. It employs multi-threading to enhance scanning speed, allowing simultaneous scanning of multiple ports.

### Features

- **Target Specification**: Users can specify the target IP address or URL as a command-line argument.
- **Port Selection**: PortSweeper provides flexibility in selecting ports to scan, either specifying individual ports or scanning a range.
- **Protocol Support**: Users can choose to scan TCP ports, UDP ports, or both.
- **Speed Control**: PortSweeper allows users to adjust the scanning speed on a scale from 1 to 5, enabling customization based on requirements.
- **Banner Grabbing**: Optionally, users can choose to grab banners from open TCP ports to gather additional information about services running on those ports.
- **Reverse DNS Lookup**: PortSweeper offers the functionality to perform reverse DNS lookup to translate IP addresses into domain names.

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/LupusJM/PortSweeper.git
    ```

3. Install Dependencies:

   ```bash
   pip install argparse
   ```

2. Run the Python script `main.py` with appropriate command-line arguments.
    ```bash
    python main.py <target> [-p PORT [PORT ...]] [-t] [-u] [-a] [-s SPEED] [-r] [-b]
    ```

## Command-line Arguments

- `target`: Specify the target IP address (IPv4, IPv6) or URL.
- `-p, --port`: Specify the port(s) to scan. Can be single or multiple ports.
- `-t, --tcp`: Scan TCP ports.
- `-u, --udp`: Scan UDP ports.
- `-a, --all`: Scan all ports (0-65535).
- `-s, --speed`: Adjust scan speed on a scale from 1 to 5.
- `-r, --reverse-dns`: Perform reverse DNS lookup.
- `-b, --banner`: Grab banners from open TCP ports.

## Example

To scan TCP/UDP ports 20 to 80 on the target URL example.com with banner grabbing and reverse DNS lookup, the command would be:
```bash
python main.py example.com -p 20 80 -t -u -r -b
```

Scan all TCP ports on the target IP 10.10.110.28 example.com with speed 1:
```bash
python main.py 10.10.110.28 -t -a
```

>python main.py --help
## Notes
- Tested and verified in Linux & Windows OS.
- PortSweeper is intended for legitimate security testing purposes only. Unauthorized scanning may violate laws and regulations. Ensure proper authorization before use. Creators are not responsible for misuse.

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/lupusjm/PortSweeper/blob/main/LICENSE)

