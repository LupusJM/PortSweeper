## PortSweeper

PortSweeper is a lightweight Python tool designed for scanning open ports on a given target IP address or URL. It offers flexibility in scanning TCP, UDP, or both types of ports with options for speed adjustment and additional functionalities like banner grabbing and reverse DNS lookup.

### How it Works

PortSweeper utilizes Python's `socket` library to establish connections and scan for open ports. It employs multi-threading to enhance scanning speed, allowing simultaneous scanning of multiple ports.

### Features

- **Target Specification**: Users can specify the target IP address or URL as a command-line argument.
- **Port Selection**: PortSweeper provides flexibility in selecting ports to scan, either specifying individual ports or scanning a range.
- **Protocol Support**: Users can choose to scan TCP ports, UDP ports, or both.
- **Speed Control**: PortSweeper allows users to adjust the scanning speed on a scale from 1 to 5, enabling customization based on requirements.
- **Banner Grabbing**: Optionally, users can choose to grab banners from open TCP ports to gather additional information about services running on those ports.
- **Reverse DNS Lookup**: PortSweeper offers the functionality to perform reverse DNS lookup to translate IP addresses into domain names.

### Usage

To use PortSweeper, follow these steps:

1. Clone the PortSweeper repository from [GitHub](https://github.com/LupusJM).
2. Run the Python script `portsweeper.py` with appropriate command-line arguments.
    ```bash
    python portsweeper.py <target> [-p PORT [PORT ...]] [-t] [-u] [-a] [-s SPEED] [-r] [-b]
    ```

### Command-line Arguments

- `target`: Specify the target IP address or URL.
- `-p, --port`: Specify the port(s) to scan. Can be single or multiple ports.
- `-t, --tcp`: Scan TCP ports.
- `-u, --udp`: Scan UDP ports.
- `-a, --all`: Scan all ports (0-65535).
- `-s, --speed`: Adjust scan speed on a scale from 1 to 5 (1 being slowest and 5 being fastest).
- `-r, --reverse-dns`: Perform reverse DNS lookup.
- `-b, --banner`: Grab banners from open TCP ports.

### Example

To scan TCP ports 80, 443, and 8080 on the target IP address `192.168.1.1` with banner grabbing and reverse DNS lookup, the command would be:
```bash
python portsweeper.py 192.168.1.1 -p 80 443 8080 -t -r -b
```

### Contribution

Contributions to PortSweeper are welcome. Feel free to submit issues, feature requests, or pull requests on the [GitHub repository](https://github.com/LupusJM).

### License

PortSweeper is released under the [MIT License](LICENSE).
