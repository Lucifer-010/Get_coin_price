
<body>
    <h1>Get Coin Price from CoinGecko Using Python</h1>

    <p>This guide explores how to leverage Python's capabilities to retrieve real-time cryptocurrency price data from CoinGecko's public API.</p>

    <h2>Prerequisites</h2>
    <ul>
        <li>Python 3.x installed: <a href="https://www.python.org/downloads/">https://www.python.org/downloads/</a></li>
        <li>`requests` library: `pip install requests`</li>
        <li>CoinGecko API key (optional): <a href="https://www.coingecko.com/en/api">https://www.coingecko.com/en/api</a></li>
    </ul>

    <h2>Steps</h2>

    <ol>
        <li>Install the `requests` library:
            <pre>pip install requests</pre>
        </li>
        <li>Import necessary libraries:
            <pre>import requests</pre>
        </li>
        <li>Construct the API request URL:
            <pre>
                api_url = "https://api.coingecko.com/api/v3/simple/price"

                # Replace 'bitcoin' and 'usd' with your desired coin ID and currency
                params = {
                    "ids": "bitcoin",
                    "vs_currencies": "usd",
                    // Optional parameters:
                    // "include_market_cap": "true",
                    // "include_24h_vol": "true",
                    // "localization": "false",  // Set to "true" for localized prices
                }
            </pre>
        </li>
        <li>Make the API request:
            <pre>response = requests.get(api_url, params=params)</pre>
        </li>
        <li>Handle the response:
            <pre>
                if response.status_code == 200:
                    data = response.json()
                    # Access the coin price using its ID (e.g., data["bitcoin"]["usd"])
                    coin_price = data["bitcoin"]["usd"]
                    print(f"The current price of Bitcoin (BTC) in USD is: ${coin_price}")
                else:
                    print(f"Error: {response.status_code}")
            </pre>
        </li>
    </ol>

    <h2>Additional Considerations</h2>
    <ul>
        <li>Replace 'bitcoin' and 'usd' with the actual coin ID and currency of your choice.</li>
        <li>Consider error handling for unexpected API responses or invalid user input.</li>
        <li>For frequent use or production environments, explore obtaining a CoinGecko API key.</li>
    </ul>
</body>
