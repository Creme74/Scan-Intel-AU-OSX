# Scan Intel AU V1.1 [Creme]

## Overview
**Scan Intel AU V1.1 [Creme]** is a macOS Automator application designed to identify Audio Unit (AU) components that are **Intel-only** and not natively compatible with Apple Silicon (ARM64). This tool helps users of Logic Pro and other DAWs on Apple Silicon Macs to manage and optimize their plugin libraries.

## Features
- Scans the `/Library/Audio/Plug-Ins/Components` directory.
- Detects AU components that only have Intel binaries.
- Excludes components that support native ARM64 binaries.
- Outputs a detailed report in `intel_only_plugins_report.txt`.

## How It Works
The app:
1. Recursively scans each `.component` folder for binary files.
2. Uses the `file` command to determine the architecture of each binary.
3. Flags components as **Intel-only** if no ARM64 binaries are found.

## Installation
1. Download the app.
2. Unzip the file.
3. Move the `.app` file to your desired location (e.g., `Applications` folder or Desktop).

## Usage
1. Double-click the app to run it. (You might need to right click the very first time you open the Application to pass gatekeeper)
2. The app will scan the `Components` directory and generate a report. (you'll see a little wheel on the top right of your screen)
3. Upon completion, the report `intel_only_plugins_report.txt` will open automatically. (it may take more or less time considering the number of components)

## Requirements
- Tested on macOS Sierra and macOS Sonoma but should work on any macOS above.

## Acknowledgments
Special thanks Vito De Luca my one and only Beta Tester (Team Comics)
