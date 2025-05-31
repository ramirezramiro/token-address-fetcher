# token-address-fetcher

# Crypto Platform Token Exporter

This Python script allows you to easily fetch and export cryptocurrency token information (CMC Rank, Coin Name, and Token Mint Address) for specific blockchain platforms from CoinMarketCap. You can choose which platform's tokens you want to retrieve, and the data will be saved to a CSV file for your convenience.

---
## Features

* **List Available Platforms**: Automatically fetches and displays a list of all major blockchain platforms recognized by CoinMarketCap.
* **Interactive Selection**: Prompts you to select a specific blockchain platform from the available list.
* **Live Data Preview**: Shows you the CMC Rank, Coin Name, and Token Mint Address directly in your console as the data is being fetched.
* **CSV Export**: Exports the collected data to a CSV file.
* **Dynamic Filenames**: The generated CSV file is named dynamically (e.g., `solana_tokens.csv`, `ethereum_tokens.csv`) based on your selected platform.
* **Token Mint Address Retrieval**: Attempts to retrieve the token mint address (or contract address) for each cryptocurrency on the chosen platform. If not available via CoinMarketCap's API, it will indicate "N/A".

---
## How to Use

### Prerequisites

* **Python 3**: Make sure you have Python 3 installed on your system.
* **`requests` library**: You'll need to install the `requests` library to make API calls. You can install it using pip:
    ```bash
    pip install requests
    ```

### Running the Script

1.  **Save the script**: Save the provided Python code as a `.py` file (e.g., `crypto_exporter.py`).
2.  **Open your terminal or command prompt**.
3.  **Navigate to the directory** where you saved the script.
4.  **Run the script** using the following command:
    ```bash
    python crypto_exporter.py
    ```

### Script Interaction

1.  The script will first **fetch and display a numbered list of available token platform names**.
2.  You will then be **prompted to enter the exact name of the token platform** you wish to query (e.g., `Solana`, `Ethereum`, `Binance Smart Chain`).
3.  As the script fetches data for your chosen platform, it will **print the CMC Rank, Coin Name, and Token Mint Address to your console in real-time**.
4.  Once the process is complete, a **CSV file** named after your chosen platform (e.g., `solana_tokens.csv`) will be **saved in the same directory** where you ran the script. The script will confirm the export and show the full path to the file.

---
## Example Output (Console)

Fetching available token platform names from CoinMarketCap API...

Available Token Platform Names:
  1. Arbitrum
  2. Avalanche
  3. BNB Smart Chain
  4. Base
  5. Celo
  ...
  15. Ethereum
  16. Fantom
  ...
  30. Solana
  ...

Enter the exact name of the token platform you want to query (or 'exit' to quit): Solana

Fetching 'Solana'-based cryptocurrencies...

--- Live Output for Solana Tokens ---
CMC Rank  | Coin Name                    | Token Mint Address
--------------------------------------------------------------------------------
11        | Solana                       | N/A (Not Available via CMC API)
46        | Render Token                 | 0x6de037ef95b14f8ef0f5f40391d8cf0...
48        | Bonk                         | N/A (Not Available via CMC API)
...
--------------------------------------------------------------------------------

Successfully exported 150 'Solana'-based cryptocurrencies to 'solana_tokens.csv'
File saved in: /path/to/your/script/solana_tokens.csv
