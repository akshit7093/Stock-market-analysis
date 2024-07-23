# Stock-market-analysis
Here's a detailed `README.md` file for your project. This file will include sections for project description, setup instructions, code explanations, and usage examples.

---

# Stock Trading Simulation Project

## Project Description

This project simulates stock trading using historical stock data. It loads and preprocesses stock data, calculates statistical metrics, identifies trading signals, simulates trades based on these signals, and generates both JSON and text reports summarizing the trading activity and final portfolio status.

## Features

- **Load and preprocess stock data** from a CSV file.
- **Calculate statistics** such as price changes and moving averages.
- **Identify trading signals** for buying and selling.
- **Simulate trades** based on trading signals.
- **Generate reports** in JSON and text formats.

## Project Structure

- `stock_trading_simulation.py`: Main script for running the project.
- `portfolio_report.json`: JSON file containing the trading history and final portfolio status.
- `portfolio_report.txt`: Text file summarizing the trading activity and portfolio status.

## Prerequisites

- Python 3.x
- Pandas library

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/stock-trading-simulation.git
cd stock-trading-simulation
```

### 2. Install Dependencies

Ensure you have Python 3.x installed. Install the required Python library using pip:

```bash
pip install pandas
```

### 3. Update File Path

The script uses a sample CSV file from Google Sheets. If you have a different file or location, update the `file_path` variable in the script:

```python
file_path = 'https://docs.google.com/spreadsheets/d/e/2PACX-1vSt2Y9xvGE-fIGK4Bgqgj86QlKVkVr7a-DESPYea7QRYvjFNZuf5w5I59RDKRTbS0eh61Qmq45M-C4X/pub?output=csv'
```

### 4. Run the Script

Execute the script to perform the stock trading simulation and generate reports:

```bash
python stock_trading_simulation.py
```

## Code Explanation

### `load_and_preprocess_data(file_path)`

- **Purpose:** Load and preprocess stock data.
- **Details:** Converts the 'Date' column to datetime, sorts by 'Company' and 'Date', removes dollar signs from price columns, and converts them to float.

### `calculate_statistics(stock_data)`

- **Purpose:** Calculate price changes and moving averages.
- **Details:** Computes daily price changes and 5-day moving averages for each company.

### `identify_trends(stock_data)`

- **Purpose:** Identify buy and sell signals based on price and moving average.
- **Details:** Generates buy signals when the closing price crosses above the moving average and sell signals when it crosses below.

### `simulate_trades(stock_data, initial_cash=10000)`

- **Purpose:** Simulate stock trades based on identified signals.
- **Details:** Manages portfolio by buying or selling stocks according to the signals, tracking cash and stock quantities.

### `generate_reports(stock_data, portfolio, json_file_path='portfolio_report.json', txt_file_path='portfolio_report.txt')`

- **Purpose:** Generate JSON and text reports of trading activities and final portfolio status.
- **Details:** Writes trade history and final portfolio details to the specified JSON and text files.

## Usage

1. **Load and preprocess data:** The script fetches stock data from the specified CSV file.
2. **Calculate statistics:** It computes relevant statistics like price changes and moving averages.
3. **Identify trends:** It determines buy and sell signals based on the calculated statistics.
4. **Simulate trades:** The script simulates buying and selling of stocks based on identified signals.
5. **Generate reports:** Two reports are generated - one in JSON format and one in plain text format, summarizing the trades and final portfolio status.

## Example Output

### JSON Report

```json
{
    "trades": [
        {"date": "2024-07-01", "company": "AAPL", "action": "BUY", "price": 150.00},
        {"date": "2024-07-10", "company": "AAPL", "action": "SELL", "price": 155.00}
    ],
    "final_portfolio": {
        "cash": 10050.00,
        "stocks": {"AAPL": 0}
    }
}
```

### Text Report

```
Simulated Trades
Date | Company | Action | Price
2024-07-01 | AAPL | BUY | $150.00
2024-07-10 | AAPL | SELL | $155.00

Final Portfolio Status
Cash remaining: $10050.00
Stocks:
AAPL: 0 shares
```

## Contributing

Feel free to fork the repository and submit pull requests with improvements or bug fixes.


## Contact

For any questions or feedback, please contact [akshitsharma7093@gail.com](mailto:your-email@example.com).

---

