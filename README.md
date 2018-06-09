# Try it out on Bitmex TestNet

Open a Demo account at [Bitmex TestNet](https://testnet.bitmex.com/register), once you are logged in, click on Account Tab , then API Keys on the left menu bar. Give your API Keys a name, don't worry about the CIDR for now, and adjust Key Permissions to "Order". Don't checkbox "Withdraw", Click Create API Keys: and Bitmex will return some strings like the one you see below. These are real api keys that you can use on the testnet exchange to simplify testing the application today. 

ID: oVbXpx0R0SYd47CTz1GKxv2X
Secret:	vFN3ti8O0FXKRx0oPMBB_MU5uWlMpWXOG0vfD89Pl70vMnFt

Open your Telegram Application, or download the [application](https://telegram.org),
Click [here](http://t.me/bitmextestnet_bot) to access the telegram bot or type in **@bitmexTestNet_bot** in the telegram search box. Then click the start button.

# Test Net Bitcoins
You will need to fund your bitmex testnet account with some Testnet bitcoins Follow the instructions on the [Deposit page](https://testnet.bitmex.com/app/deposit)

After you have tested the application proceed with your Live account API Keys with the **Official** [Bitmex_Xchange_bot](http://t.me/bitmex_xchange_bot) or type in @bitmex_xchange_bot in the telegram search box. **Demo API Keys do not work with the Official Bitmex_Xchange_Bot.**

# Telegram User Name
You must have a telegram username setup before submitting your api keys!

# Telegram Bot
| Name | Echange | Telegram Link |
|----------- | ----------| ----------|
| @bitmextestnet | Bitmex Testnet | [Demo](http://t.me/bitmextestnet_bot) |
| @bitmex_xchange_bot | Bitmex Live | [Live](http://t.me/bitmex_xchange_bot) |

# Step One: Login
| Example | Real Login | 
|----------- | ----------|
| /ex_setup [API_Token] [API_Secret] | /ex_setup oVbXpx0R0SYd47CTz1GKxv2X vFN3ti8O0FXKRx0oPMBB_MU5uWlMpWXOG0vfD89Pl70vMnFt |
| /apitoken [api token] | /apitoken oVbXpx0R0SYd47CTz1GKxv2X |
| /apisecret [api secret]| /apisecret vFN3ti8O0FXKRx0oPMBB_MU5uWlMpWXOG0vfD89Pl70vMnFt |

You can use either method above to submit the api keys. The difference is one command versus two commands. 


**You must setup the login before setting up the Global Setting**

# Step Two: Global Settings
| Name | Description | Example |
|----------- | ----------| ----------|
| symbol | Default symbol to use | /symbol XBTUSD |
| volume | Default contract size to use | /volume 100 |
| /ex_global [Symbol] [Contract Size] | Setup both Symbol and Volume within one command |/ex_global XBTUSD 5000 |
| Global | View your global setting | /global |

You must setup the Global settings after running "/ex_setup [api_ID] [api_secret]"

Global settings allow the user to select symbol and position size to start trading quickly by typing in "/ex_global [symbol] [volume]

# Commands
| Name  | Command | Description
| ------------- | ------------- | -------------|
| Exchange Setup  | /ex_setup key [string] secret [string] | Must be setup to allow private api calls|
| Global Setting  | /ex_global symbol [string] volume [number] | Default settings unless otherwise inputted|
| Show Global Settings | /global | Displays all the users settings |
| Buy Order  | /buy _sym[string] _v[number]  or Buy| Creates a buy market order for specific symbol or default symbol|
| Sell Order  | /sell _sym[string] _v[number] or Sell| Creates a sell market orderfor specific symbol or default symbol |
| Limit Buy Order  | /bid _sym[string] _p[number] _v[number] | Creates a buy limit order |
| Limit Sell Order  | /ask _sym[string] _p[number] _v[number] | Creates a sell limit order |
| Get Price  | /p_sym[string] or Price | Gets price for specific symbol or Gets price for default symbol |
| Get OrderBooks  | /book _sym[string] or Book | Gets orderbook for specific symbol or Gets orderbook for default symbol |
| Trade from OrderBook  | /bookt _sym[string] or Bookt| Gets orderbook for specific symbol or Gets orderbook for default symbol |
| Show Orders | /orders or Orders | Show orders for all symbols |
| Cancel Orders | /cancel or Cancel|  Cancels all orders for all symbols |
| Show Position | /pos _sym[string] or Pos | Show open position for specific symbol or Show open position for default symbol|
| Close Position | /close _sym[string] or Close| Closes a position for specific symbol or Closes a position for default symbol |
| Profit and Loss | /pnl _sym[string] or Pnl | Show profit/loss for specific symbol or Show profit/loss for default symbol |
| Balance | /wallet | Shows wallet balance|
| Adjust Leverage | /leverj _sym[string] _lev[number] or Leverj or [number]x| Change contract leverage for specific symbol or default symbol |

# Grid and Scaling Positions Commands
| Name  | Command | Description
| ------------- | ------------- | -------------|
| Buy Grid | /gridbuy_sym[string]_offset[number]_v[number]_level[number]_space[number] | Buy Limit Order scaling with options to adjust the volume, symbol, offset from currect price to place the first order, how many levels(orders), and the order spacing|
| Sell Grid | /gridsell_sym[string]_offset[number]_v[number]_level[number]_space[number] | Sell Limit Order scaling with options to adjust the volume, symbol, offset from currect price to place the first order, how many levels(orders), and the order spacing|
| Bulk Buy | /bulkbuy_sym[string]_offset[number]_v[number]_level[number]_space[number] | Buy Limit Order scaling with options to adjust the volume, symbol, offset from currect price to place the first order, how many levels(orders), and the order spacing using Bitmex BulkOrder API|
| Bulk Sell | /bulksell_sym[string]_offset[number]_v[number]_level[number]_space[number] | Sell Limit Order scaling with options to adjust the volume, symbol, offset from currect price to place the first order, how many levels(orders), and the order spacing using Bitmex BulkOrder API|

# Calculated Risk Per Trade Commands
| Name  | Command | Description
| ------------- | ------------- | -------------|
| Risk % Per Trade | /rptbuy_r[number]_b[number]_s[number]| Market Order Buy with automatic volume size dependent on three variables: r = Risk Percentage, b = Balance to contribute, s = Stoploss input |
| Risk % Per Trade | /rptsell_r[number]_b[number]_s[number]| Market Order Sell with automatic volume size dependent on three variables: r = Risk Percentage, b = Balance to contribute, s = Stoploss input |

Risk Per Trade commands allow the trader to automatically calculate their contract size based on the balance/wallet , stoploss value from their technical analysis, and risk percentage that they would like to risk. With these three parameters ( balance, stoploss, and risk percentage) the command will place a market order with the correct contract size. The return message will also include a command for you to place a stoploss ( Stop Order ) at your defined values. Learn more about using the Stoploss Commands below. 

# Stoploss Commands
| Name  | Command | Description
| ------------- | ------------- | -------------|
| Set Stop Order | /stop_typesell_sym[string]_p[number]_v[number]| A Stop Order **Sell** can be used to lock in profit on a Buy position or can be used for a stoploss value to limit risk on your buy position |
| Set Stop Order | /stop_typebuy_sym[string]_p[number]_v[number]| A Stop Order **Buy** can be used to lock in profit on a Sell position or can be used for a stoploss value to limit risk on your sell position |

If you have a position in the market and you want to protect your profits or set a stoploss , you can place a **STOP** order type. When you have a Buy Position in the market you will want to use a /stop_typesell for a stoploss. When you have a Sell Position in the market you will want to use a /stop_typebuy for a stoploss. 


# User Interface
![Telegram Keyboard A](https://preview.ibb.co/hO9SBx/bitmex_xchange_bot.png)

# Keyboard
| Name  | Command | Description
| ------------- | ------------- | -------------|
| Default Keyboard | /keyboard or "Keyboard" | Trade from Push buttons within the Telegram application |
| Home Keyboard | /keyboardhome or "Home" | Learn through the Tutorial, Check Wallet, Change Keybaords |

# CryptoCoinCopy 
| Name  | Telegram Group | Description
| ------------- | ------------- | -------------|
|BITCOIN | @cryptocopy | Trading room for Bitcoin |
|ETHER | @cryptocopyETH | Trading room for ETH/BTC |
|LITECOIN | @cryptocopyLTC | Trading room for LTC/BTC |
|BCASH | @cryptocopyBCH | Trading room for BCH/BTC |
|ALTS | @cryptocopyALT | Trading room for other Bitmex contracts |

To learn more about the trading groups, please read the information on CryptoCoinCopy
[Readme](https://github.com/fx4btc/CryptoCoinCopy)



