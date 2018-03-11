# Global Settings
| Name | Description |
|----------- | ----------|
| exchange |  Use a particular exchange by default |
| symbol | Default symbol to use |

# Channel Settings
| Name | Description |
|----------- | ----------|
| exchange  |  Use a particular exchange for a given channel (eg. Telegram) |
| symbol | Default symbol to use  |

Each channel is a communication channel with the user.  telegram, line, CLI, facebook messenger, etc.

# Exchange Settings
| Name | Description |
|----------- | ----------|
| symbol | Default symbol to use for this exchange |
| market_type | margin, exchange, funding |
| volume | Default position size to use 

Each exchange can include your default market type symbol and position size to start trading quickly

# Plugin Settings
| Name | Description |
|----------- | ----------|

# User Setting Hieracrchy
Global <- Channel <- Exchange <- Plugin <- Command

Command-setting override the Default Plugin setting when used. Plugin-settings override Exchange-setting when filled in. 
Exchange-setting override the Channel-settings once defaults are saved. 
Channel-settings override the Global-setting once defaults are saved


# Plugin Commands
| Name  | Command | Description
| ------------- | ------------- | -------------|
| Exchange Setup  | /ex_setup key [string] secret [string] | |
| Account | /account | Show all user related information (channels, username, billing, etc)
| Show Settings | /settings | Displays all the users settings |
| Create setting | /setting [string] [value] |  Allows creating of settings.  /setting global.exchange bitmex |
| Limit Orders  | /limit symbol [string,setting] price [number] vol [number] | Creates a limit order |
| Get Price  | /price symbol [string,setting] exchange [string,setting] | Gets price on a exchange |
| Show orders | /orders symbol [string,setting] exchange [string,setting] | Show orders for a symbol and exchange |
| Show all orders | /orders_all |  Query all exchanges that user has api keys and show orders|
| Cancel order | /orders cancel [string, id] | Cancels an order based on ID |
| Cancel orders | /orders_cancel symbol [string,setting] exchange [string,setting] |  Cancels all orders based on symbol, exchange |
| Cancel all orders | /orders_cancel_all | Query all exchanges that user has api keys and cancel those orders |
| Show Positions | /positions symbol [string,setting] exchange [string,setting] | Show all positions for a given exchange and symbol |
| Show all positions | /positions_all |  Query all exchanges that user has api keys  |
| Close position | /position_close symbol [string,setting] exchange [string,setting] | Closes a position on a given pair and exchange |
| Profit and Loss | /pnl exchange [string,setting] | Show profit/loss on an exchange |
| Balances | /wallet exchange [string,setting] | Shows wallet balances for a given exchange |
| All balances | /wallets | Shows balances for all exchanges |
| History | /history | Shows a list of commands that were previously ran, allows them to be ran with one click |



