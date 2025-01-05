# OKX API: Frequently Asked Questions (FAQ)

## What Does Passphrase Refer To?

The passphrase is the password you set when creating an APIKey. It is essential to remember it, as it cannot be retrieved. If forgotten, you will need to generate a new APIKey.

---

## How to Create a Demo Account APIKey?

To trade on the demo platform, you must create an APIKey specifically for the demo environment. Follow these steps:

1. Log in to your OKX account.
2. Navigate to **Trading > Demo Trading > Personal Center**.
3. Select **Create Demo Account APIKey**.
4. Start demo trading.

---

## Does the APIKey Expire?

APIKeys that are not bound to an IP and have transaction or withdrawal permissions will be automatically deleted after 14 days of inactivity. However, APIKeys used to access private or account-related functions, such as checking account balances or placing orders, will remain active.

**Note:** Read-only APIKeys bound to an IP or specific permissions will not expire.

---

🚀 **Unlock Your Crypto Journey with OKX!**  
Trade with zero fees, access cutting-edge Web3 features, and join millions of global traders. New users get an exclusive welcome bonus of up to 100 USDT!  

Click to view ☞ [OKX Welcome Limited-Time Offer, Claim Up to 100 USDT Reward](https://bit.ly/OKXe)

---

## Can Orders Be Placed in USDT or Currency Units via API?

No, for contract orders, the default is to place orders in terms of contracts. To convert between contracts and coin quantities, you can use the contract-to-coin conversion interface.  
☞ [Learn more here](https://bit.ly/OKXe)

---

## How to Calculate Fluctuation Rates via API?

The API does not provide direct price increase or decrease rates. You can calculate them using the following formula:

**(Last trade price - Opening price 24h ago) / Opening price 24h ago × 100%**

You can obtain relevant data from the market interface:
☞ [Get Market Data](https://bit.ly/OKXe)

---

## Why Does "51000 Parameter posSide Error" Occur?

This error happens due to mismatched account settings. Check your account mode (e.g., buy/sell mode, open/close mode). You can view and set your account configuration via the API.  
☞ [Learn more here](https://bit.ly/OKXe)

---

## How to Get Contract Face Value and Minimum Order Quantity?

Use the trading products' basic information interface to retrieve the data:

- **Contract face value:** `ctVal`  
- **Minimum order quantity:** `minSz`

☞ [Access Product Data Here](https://bit.ly/OKXe)

---

## What Is the Format of instId?

The `instId` format varies based on the product type:

- **Coin Leverage:** `BTC-USDT`
- **Perpetual Contracts:** `BTC-USD-SWAP`, `BTC-USDT-SWAP`
- **Settlement Contracts:** `BTC-USD-210326`
- **Options Contracts:** `BTC-USD-210326-2000-C` (Call), `BTC-USD-210326-2000-P` (Put)

---

## How to Set Stop Loss and Take Profit?

For orders with attached take-profit or stop-loss, use the order interface with the `attachAlgoOrds` parameter.  
☞ [Learn more here](https://bit.ly/OKXe)

For separate stop-loss or take-profit orders, refer to the strategy commission interface.  
☞ [Explore Strategy Settings](https://bit.ly/OKXe)

---

## Common API Errors and Solutions

### 1. **"50102 Timestamp Request Expired"**  
Synchronize your system time with the server's time to avoid timestamp expiration. Ensure the time difference is within 30 seconds.  

### 2. **"50101 APIKey Does Not Match Environment"**  
Ensure you're using the correct APIKey for the environment. Real accounts require real APIKeys, while simulated accounts require simulated APIKeys.

### 3. **"51010 Request Unsupported Under Current Account Mode"**  
Adjust your account mode to use leverage or contracts. This can be set via the web, app, or API.  
☞ [Learn more here](https://bit.ly/OKXe)

### 4. **"51121 Order Quantity Must Be a Multiple of the Lot Size"**  
Ensure the order quantity is a multiple of the currency pair's minimum lot size. This can be found in the `minSz` field of the product interface.

---

## Error: Withdrawal Address Is Not Whitelisted for Verification Exemption

For withdrawals via API, you must add the withdrawal address on the platform and select the "non-verified" option. Disabling allowlist verification on the page does not impact API functionality.

---

## What Is "50004 API Endpoint Request Timeout"?

This error indicates server pressure. Retry at a later time, as high-pressure periods, such as capital fee collection times (8 AM, 4 PM, 12 AM UTC), may cause delays. Always check the actual result of your request.

---

For more API-related inquiries, contact us via the OKX app or explore our detailed API documentation.  

☞ [Discover More at OKX](https://bit.ly/OKXe)
