# WiFi Network Scanner

A standalone Windows application for analyzing nearby WiFi networks and generating detailed reports. Built with Python and compiled to a single executable file.

## Features

- **Network Discovery**: Scans all visible WiFi networks using Windows netsh API
- **Signal Analysis**: Measures and categorizes signal strength (Strong/Good/Weak)
- **Security Assessment**: Identifies open networks vs secured networks
- **Device Identification**: Basic vendor lookup through MAC address analysis
- **Network Classification**: Distinguishes between regular WiFi, mobile hotspots, and hidden networks
- **Data Export**: Saves results to JSON and CSV formats
- **Portable**: Single executable file, no Python installation required

## Download

**Latest Release**: [Download WiFi_Scanner.exe](../../releases/ )

File size: ~ 7MB (includes Python runtime)

## System Requirements

- Windows 10 or Windows 11
- WiFi adapter enabled
- No additional software required

## How to Use

1. Download `WiFi_Scanner.exe` from the releases section
2. Place the file in any folder
3. Double-click to run (no installation needed)
4. The scan will start automatically and display results in the console
5. Results are saved to `wifi_results.json` and `wifi_results.csv` in the same folder

## Sample Output

```
WIFI NEIGHBORHOOD SCAN

NETWORKS DETECTED: 12
Your area shows normal WiFi activity.

NETWORK BREAKDOWN:
- Regular WiFi Networks: 9
- Mobile Phone Hotspots: 2
- Hidden Networks: 1

SIGNAL STRENGTH ANALYSIS:
- Strong Signal (70%+): 4 networks
- Good Signal (50-69%): 6 networks
- Weak Signal (<50%): 2 networks

SECURITY STATUS:
- Password Protected: 11 networks
- Open Networks: 1 network

TOP DEVICE VENDORS:
- Netgear: 3 devices
- TP-Link: 2 devices
- Unknown: 7 devices
```

## Technical Details

- **Language**: Python 3.8+
- **Compiler**: PyInstaller
- **APIs Used**: Windows netsh wlan commands
- **Output Formats**: Console display, JSON, CSV
- **Architecture**: Single-threaded with retry logic for reliability

## Use Cases

- Network site surveys for small businesses
- WiFi environment analysis before router placement
- Connectivity assessment for real estate evaluation
- Basic network security awareness
- IT troubleshooting and planning

## Troubleshooting

**No networks found:**
- Ensure WiFi adapter is enabled
- Try running as Administrator
- Restart Windows WiFi service

**Permission errors:**
- Right-click the executable and select "Run as administrator"

**Antivirus warnings:**
- This is normal for PyInstaller executables
- The tool only reads network information, no data is transmitted
- Add exception in your antivirus if needed

## About This Project

This tool demonstrates practical system programming skills including:
- Windows API integration
- Data parsing and validation
- Error handling and retry mechanisms
- Cross-locale compatibility
- Professional software distribution

Built as a portfolio project showcasing real-world application development beyond typical coding exercises.

## Privacy & Security

- No data is transmitted or stored remotely
- Only scans publicly broadcast WiFi beacon information
- Creates local files only in the execution directory
- No network connections are established

## License

MIT License - See LICENSE file for details