# NerdGraph: Get Active & Canceled Managed Accounts

## Overview
`nerdgraph-get-managed-accounts` is a Python application designed to interact with the New Relic GraphQL API. It retrieves account data and stores it in CSV files for further analysis and utilization.

## Features
- Fetches account data from New Relic using NerdGraph (GraphQL).
- Processes and writes data to CSV files in chunks.
- Utilizes environment variables for configuration.

## Requirements
- Python 3.12+
- `Poetry` for dependency management

## Installation
1. Install Poetry if you haven't already:
   ```sh
    # On Mac with Homebrew
    brew install poetry

    # Or using the official installer
    curl -sSL https://install.python-poetry.org | python3 -
    ```
   
2. Clone the repository:
    ```sh
    git clone https://github.com/brett-larson/nerdgraph-get-managed-accounts.git
    cd nerdgraph-get_managed_accounts
    ```

3. Create a `.env` file in the root directory and add your New Relic API key:
    ```env
    NEW_RELIC_API_KEY=your_api_key_here
    ```

4. Install dependencies using Poetry:
    ```sh
    poetry install
    ```

## Usage
1. Run the application using Poetry:
    ```sh
    poetry run get-accounts
    ```

2. The application will fetch the account data and write it to a CSV file named `active_accounts.csv` or `canceled_accounts.csv` in the `src/data/csv` directory.

## Project Structure
- `src/get_managed_accounts/api/client.py`: Contains the client for interacting with the New Relic GraphQL API.
- `src/get_managed_accounts/data/csv_handlers.py`: Contains classes for handling CSV data.
- `src/get_managed_accounts/main.py`: Main script to execute the core logic of the application.
- `src/get_managed_accounts/utils.py`: Utility functions, including the logger setup.

## Logging
The application uses a logger to provide information about its execution. Logs are printed to the console.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request.

## License
This project is licensed under the MIT License.
