# AutoTor - Simple Tor Hidden Service Tool

## Overview

AutoTor is a lightweight Electron app that makes it easy to set up and manage a Tor hidden service. It provides a simple interface to start hosting a hidden service, view your `.onion` address, launch the Tor Browser, update the port, and reset the configuration.

### Features
- Automatically configures a Tor hidden service on launch (default port: 3000).
- Start or stop the Tor hidden service with one click.
- Display the `.onion` address of your hidden service.
- Launch the Tor Browser to access your hidden service.
- Update the port or reset the configuration as needed.

## Installation

1. **Clone the Repository** (if not already done):
   ```bash
   git clone https://github.com/your-username/autotor.git
   cd autotor
   ```

2. **Install Dependencies**:
   ```bash
   npm install
   ```

## Usage

1. **Run the App**:
   ```bash
   npm start
   ```

2. **Main Interface**:
   - The app opens directly to the configuration screen.
   - **Port Input**: Shows the current port (default: 3000). Update it if needed.
   - **Update Port**: Change the port (must be between 1024 and 65535).
   - **Start Hosting**: Start the Tor hidden service.
   - **Show Onion Link**: Display the `.onion` address.
   - **Launch Tor Browser**: Open the Tor Browser to access your hidden service.
   - **Reset Configuration**: Reset and reinitialize the Tor configuration.

3. **Access Your Hidden Service**:
   - Click "Start Hosting" to start the service.
   - Click "Show Onion Link" to see the `.onion` address.
   - Click "Launch Tor Browser" and enter the `.onion` address in the browser.

## Troubleshooting

- **Buttons Are Disabled**:
  - Check the terminal for errors. Ensure `tor.exe` is in `services/tor/`.
  - Verify the port (default: 3000) is free:
    ```bash
    netstat -aon | findstr :3000
    ```
    If the port is in use, update it using "Update Port".

- **Tor Service Fails to Start**:
  - Look for `Tor:` or `Tor Error:` messages in the terminal.
  - Ensure `tor.exe` is running (check Task Manager).

- **Tor Browser Fails to Launch**:
  - Ensure `firefox.exe` is in `assets/tor_browser/Tor Browser/Browser/`.
  - Test launching manually:
    ```bash
    "D:\autotor\assets\tor_browser\Tor Browser\Browser\firefox.exe"
    ```

## Notes

- This app assumes `tor.exe` and Tor Browser are pre-installed in the correct directories:
  - `services/tor/tor.exe`
  - `assets/tor_browser/Tor Browser/Browser/firefox.exe`
- If you need to update these dependencies, download them from [torproject.org](https://www.torproject.org/download/).

## License

MIT License. See the [LICENSE](LICENSE) file for details.

---

For issues, open a ticket on the [GitHub repository](https://github.com/your-username/autotor/issues).