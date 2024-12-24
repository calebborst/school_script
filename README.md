# Remote Exploitation Batch Script - README

## Overview
This script was created as a response to an incident where someone remotely caused a Blue Screen of Death (BSOD) on my PC in a computer lab environment. To level the playing field, I developed this batch file to allow similar remote commands, including causing a BSOD, querying system information, managing processes, and more.
I wanted to ensure that the user didn’t need to run anything on their system for me to gain access. Instead, I aimed to rely solely on the tools and resources already available to me. For example, some wmic commands need the user to run a powershell command to allow remote users to run commands against their machine.

## Features
The script includes the following functionalities:

1. **Send Hello Message**: A theoretical demonstration to test communication with the target system.
2. **Send Custom Command**: Allows you to execute custom commands remotely.
3. **Cause BSOD**: Forces a Blue Screen of Death on the target system.
4. **Retrieve System Information**: Fetches detailed system information from the remote PC.
5. **Shutdown Remote PC**: Initiates a remote shutdown of the target system.
6. **Restart Remote PC**: Restarts the remote PC.
7. **Query Logged-in Users**: Retrieves a list of users logged into the remote system.
8. **Attempt to Disable Antivirus**: Tries to disable the antivirus software on the remote PC.
9. **Query Services**: Lists services running on the target system.
10. **Kill Explorer.exe**: Terminates the explorer process on the remote PC.
11. **Start Process (Hidden)**: Runs a process on the remote system without UI visibility.
12. **Start Process with UI**: Executes a process with UI on the remote system.
13. **Start Process with UI Infinitely**: Continuously starts a process with UI on the remote system.

## How It Works
### Target Selection
The script uses a naming convention to identify PCs in the lab (e.g., 'E110-01'). You can:
- Specify a target PC by its number.
- Target all PCs in the lab.
- Use 'test mode' for local testing.

### Authentication
The script leverages pre-configured credentials ('student' user with 'router' password) to connect to the target systems.

### Command Execution
The script uses Windows command-line utilities such as:
- 'taskkill' for process termination.
- 'shutdown' for power management.
- 'systeminfo' for system information retrieval.
- 'wmic' and 'schtasks' for remote process management.

### Menu-Driven Interface
A simple text-based menu allows you to select exploits or return to the main menu.

## Usage Instructions
1. Copy the script ('start.bat') to your local system.
2. Open a command prompt and navigate to the script's directory.
3. Run the script using the command: 'start.bat'.
4. Follow the menu prompts to select and execute commands.

## Disclaimer
This script is intended for educational purposes and personal testing only. Unauthorized use against systems or individuals is unethical and may be illegal. Use responsibly and ensure you have appropriate permissions before executing any actions.

## Development Motivation
This project was motivated by a personal incident in a computer lab where my system was BSODed remotely. The goal was to understand remote exploitation techniques and protect against similar attacks in the future.
