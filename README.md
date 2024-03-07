<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>README: Get Coin Price from CoinGecko using Python</title>
</head>
<body>
    <h1>Get Coin Price from CoinGecko using Python</h1>

    <p>This script retrieves the current price of a specified cryptocurrency from CoinGecko using the Python programming language and the CoinGecko API.</p>

    <h2>Requirements</h2>

    <ul>
        <li>Python 3.6 or later</li>
        <li>requests library: `pip install requests`</li>
    </ul>

    <h2>Usage</h2>

    <p>1. Clone or download this repository.</p>
    <p>2. Install the required library: `pip install requests`.</p>
    <p>3. Replace `'bitcoin'` in the script with the desired cryptocurrency ID (e.g., `'ethereum'`, `'binance-coin'`).</p>
    <p>4. Run the script: `python get_coin_price.py`.</p>

    <h2>Example Output</h2>

    <pre>The current price of Bitcoin (BTC) is $42,345.67.</pre>

    <h2>Explanation</h2>

    <p>The script utilizes the `requests` library to send an HTTP GET request to the CoinGecko API endpoint for the specified cryptocurrency. The API response is then parsed to extract the current price and formatted for output.</p>
</body>
</html>
