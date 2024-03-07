<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Get Coin Price from CoinGecko Using Python</title>
</head>
<body>
    <h1>Get Coin Price from CoinGecko Using Python</h1>

    <p>This guide explores how to leverage Python's capabilities to retrieve real-time cryptocurrency price data from CoinGecko's public API.</p>

    <h2>Prerequisites</h2>

    <ul>
        <li>Python 3.x installed: <a href="https://www.python.org/downloads/">https://www.python.org/downloads/</a></li>
        <li><code>requests</code> library: Install using pip: <code>pip install requests</code></li>
        <li>Optional: CoinGecko API key (for higher request limits): <a href="https://www.coingecko.com/en/api">https://www.coingecko.com/en/api</a></li>
    </ul>

    <h2>Steps</h2>

    <ol>
        <li>Install the <code>requests</code> library:</li>
        <pre><code>pip install requests</code></pre>
        <li>Import necessary libraries:</li>
        <pre><code>import requests</code></pre>
        <li>Construct the API request URL:</li>
        <pre><code>api_url = "https://api.coingecko.com/api/v3/simple/price"

params = {
    "ids": "bitcoin",
    "vs_currencies": "usd",
    // Optional parameters:
    // "include_market_cap": "true",
    // "include_24h_vol": "true",
    // "localization": "false",  // Set to "true" for localized prices
}</code></pre>
        <li>Make the API request:</li>
        <pre><code>response = requests.get(api_url, params=params)</code></pre>
        <li>Handle the response:</li>
        <pre><code>if response.status_code == 200:
    data = response.json()
    coin_price = data["bitcoin"]["usd"]
    print(f"The current price of Bitcoin (BTC) in USD is: ${coin_price}")
else:
    print(f"Error: {response.status_code}")</code></pre>
    </ol>

    <h2>Explanation</h2>

    <p>The code imports the <code>requests</code> library for making HTTP requests to the CoinGecko API. The API URL is constructed, and parameters are specified. The <code>requests.get()</code> function sends a GET request. The response is handled, and the coin price is extracted and printed.</p>

    <h2>Additional Considerations</h2>

    <ul>
        <li>Replace 'bitcoin' and 'usd' with your desired coin ID and currency.</li>
        <li>Consider error handling.</li>
        <li>For frequent use, obtain a CoinGecko API key.</li>
    </ul>
</body>
</html>
