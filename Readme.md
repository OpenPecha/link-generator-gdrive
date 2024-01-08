
# Google Drive File Link Generator

## Overview
This Python script allows users to interact with Google Drive to find file IDs based on file names and paths, and generate shareable links for these files. It is particularly useful for managing and sharing multiple files efficiently.

## Features
- Search for Google Drive files by name.
- Generate shareable links for files.
- Update a catalog with Google Drive file IDs and shareable links.

## Prerequisites
Before you begin, ensure you have the following requirements:
- Python 3.x installed.
- `pandas` library installed (`pip install pandas`).
- Google Drive API enabled on your Google Cloud project.
- OAuth 2.0 Client IDs created in your Google Cloud project.
- `credentials.json` file downloaded from your Google Cloud project.

## Installation
1. Clone the repository or download the script.
2. Install required Python packages:
   ```bash
   pip install --upgrade google-auth google-auth-oauthlib google-auth-httplib2 google-api-python-client
   ```

## Usage
1. Place the `credentials.json` file in the same directory as the script.
2. Run the script:
   ```bash
   python link-create.py
   ```
3. The first time you run the script, a browser window will open asking you to log into your Google account and allow permissions. This will create a `token.json` file for subsequent uses.
4. The script reads from a CSV file (`summary.csv`) and updates it with Google Drive file IDs and shareable links.

## Input File Format
- The script expects a CSV file named `summary.csv` with at least the following columns: `Repository` and `Repository`. The `Repository` column should contain the names of the files you want to find in Google Drive.

## Output
- The script creates or updates a CSV file named `new catalog.csv` with Google Drive file IDs and shareable links.
- The script will print status updates and any errors encountered during execution.

## Troubleshooting
- Ensure that the `credentials.json` and `summary.csv` files are in the correct format and located in the same directory as the script.
- Check the Google Cloud Console to ensure that your API limits have not been exceeded.

## Contributing
Contributions to this project are welcome! Please feel free to submit issues or pull requests.

## License
Specify the license under which this project is available, if applicable.
