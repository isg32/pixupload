# pixupload
Pixeldrain Upload Script for Personal Use

> This bash script provides a simple command-line tool to upload files to Pixeldrain and get a clean, formatted output with the direct download link and other file details. It is designed for personal use and automates the API interaction with Pixeldrain.
Features

    Simple Command: Upload files with a single command: pixdupload <filename>.
    Secure API Key: Reads the API key from a local file (~/.pdrainapi) to avoid exposing it in the script itself.
    Dependencies Check: Automatically checks if curl and jq are installed on your system.
    Clean Output: Formats the API response into a human-readable summary.

## Prerequisites

This script is designed for Debian-based Linux systems and requires curl and jq to be installed. If you don't have them, you can install them with the following commands:
```bash
sudo apt update
sudo apt install curl jq
```

## Installation

To install the script, you can use the following commands:

```bash
wget https://raw.githubusercontent.com/isg32/pixupload/refs/heads/main/pixupload
chmod +x pixupload
sudo cp pixupload /usr/local/bin/
```

> Note: Using /usr/local/bin/ is generally preferred over /bin/ for user-added scripts.
Configuration

## Before using the script, you must set up your Pixeldrain API key.

    Obtain your API key from your Pixeldrain account page.
    Create a file named .pdrainapi in your home directory:
    touch ~/.pdrainapi
    Open the file with a text editor and paste your API key inside. The file should only contain the key, with no extra spaces or newlines.
    echo "your_api_key_here" > ~/.pdrainapi

## Usage

After installation and configuration, you can use the script by simply running the command with your filename.
```bash
pixdupload your_project_file.zip
```
## Example Output:
> A successful upload will produce output similar to this:
```bash
Uploading your_project_file.zip to Pixeldrain...
Filename: your_project_file.zip
Link: https://pixeldrain.com/u/2jzYctem
Size: 2522859792
hash sha256: a7860da10c713f1d6cf6077f2901486cdb53892d8735ccffd4102e1001676858
```
