# C++ Binance API Connector

This is a simple C++ connector for the Binance API, using only C++ libraries. It allows you to make requests to the Binance API and receive the data in JSON format.

## Dependencies

- [cURL](https://curl.haxx.se/libcurl/)
- [nlohmann/json](https://github.com/nlohmann/json)

## Usage

To use the connector, you will need to set your Binance API key and secret in the code. Then, you can call the `make_request` function with the desired API endpoint and any additional parameters as needed. The function will return the data received from the Binance API in JSON format.

Here is an example of how to get the balance data for your Binance account:

```cpp
#include "binance_connector.h"

int main() {
  json data = make_request("/api/v3/account");
  std::cout << "Total BTC balance: " << data["balances"][0]["free"] << std::endl;
  return 0;
}

##Limitations

    The connector currently only supports GET requests.
    The connector does not handle errors or rate limits from the Binance API.

##Future Improvements

    Add support for POST, PUT, and DELETE requests.
    Implement error handling and rate limit handling.
    Add support for additional Binance API endpoints and features.
