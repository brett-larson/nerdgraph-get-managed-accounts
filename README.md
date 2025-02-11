# nerdgraph-get-managed-accounts

## Overview
`nerdgraph-get-managed-accounts` is a Python-based application designed to interact with the New Relic GraphQL API. It retrieves account data and processes it into CSV files for further analysis and utilization.

## Features
- Fetches account data from New Relic using NerdGraph (GraphQL).
- Processes and writes data to CSV files in chunks.
- Utilizes environment variables for configuration.

## Requirements
- Python 3.12+
- `pip` for managing Python packages

## Installation
1. Clone the repository:
    ```sh
    git clone https://github.com/brett-larson/nerdgraph-get-managed-accounts.git
    cd nerdgraph-get_managed_accounts
    ```

2. Create and activate a virtual environment:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

4. Create a `.env` file in the root directory and add your New Relic API key:
    ```env
    NEW_RELIC_API_KEY=your_api_key_here
    ```

## Usage
1. Run the main script:
    ```sh
    python src/main.py
    ```

2. The application will fetch the account data and write it to a CSV file named `active_accounts.csv` or `canceled_accounts.csv` in the `src/data/csv` directory.

## Project Structure
- `src/api/client.py`: Contains the client for interacting with the New Relic GraphQL API.
- `src/data/csv_handlers.py`: Contains classes for handling CSV data.
- `src/main.py`: Main script to execute the core logic of the application.
- `src/utils.py`: Utility functions, including the logger setup.

## Logging
The application uses a logger to provide information about its execution. Logs are printed to the console.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request.

## License
This project is licensed under the MIT License.
