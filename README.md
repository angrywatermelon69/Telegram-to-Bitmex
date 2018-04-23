# Global Settings
| Name | Description |
|----------- | ----------|
| symbol | Default symbol to use |
| volume | Default contract size to use |

Global settings allow the user to select symbol and position size to start trading quickly

# Commands
| Name  | Command | Description
| ------------- | ------------- | -------------|
| Account | /account | Show all user related information (channels, username, billing, etc)
| Exchange Setup  | /ex_setup key [string] secret [string] | Must be setup to allow private api calls|
| Global Setting  | /ex_global symbol [string] volume [number] | Default settings unless otherwise inputted|
| Show Global Settings | /global | Displays all the users settings |
| Buy Order  | /buy _sym[string] _v[number]  or Buy| Creates a buy market order for specific symbol or default symbol|
| Sell Order  | /sell _sym[string] _v[number] or Sell| Creates a sell market orderfor specific symbol or default symbol |
| Limit Buy Order  | /bid _sym[string] _p[number] _v[number] | Creates a buy limit order |
| Limit Sell Order  | /ask _sym[string] _p[number] _v[number] | Creates a sell limit order |
| Get Price  | /p_sym[string] or Price | Gets price for specific symbol or Gets price for default symbol |
| Get OrderBooks  | /book_sym[string] or Book | Gets orderbook for specific symbol or Gets orderbook for default symbol |
| Show Orders | /orders or Orders | Show orders for all symbols |
| Cancel Orders | /cancel or Cancel|  Cancels all orders for all symbols |
| Show Position | /pos_sym[string] or POS | Show open position for specific symbol or Show open position for default symbol|
| Close Position | /close_sym[string] or Close| Closes a position for specific symbol or Closes a position for default symbol |
| Profit and Loss | /pnl_sym[string] or PNL | Show profit/loss for specific symbol or Show profit/loss for default symbol |
| Balance | /wallet | Shows wallet balance|

# Advanced Commands
| Name  | Command | Description
| ------------- | ------------- | -------------|
| Adjust Leverage | /leverage_sym[string] [number]x or Leverj| Change contract leverage for specific symbol or default symbol |
| Buy Grid | /gridbuy_sym[string]_offset[number]_v[number]_level[number]_space[number] | Buy Limit Order scaling with options to adjust the volume, symbol, offset from currect price to place the first order, how many levels(orders), and the order spacing|
| Sell Grid | /gridsell_sym[string]_offset[number]_v[number]_level[number]_space[number] | Sell Limit Order scaling with options to adjust the volume, symbol, offset from currect price to place the first order, how many levels(orders), and the order spacing|




