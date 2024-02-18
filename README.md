# Forex Gump Gold

This code is a trading robot developed by the Forex Robot Easy Team. It is designed to trade on the Forex market using the Gold instrument.

## How It Works

### Libraries Used

The code includes two necessary libraries: Trade.mqh and MovingAverages.mqh. These libraries provide functions and classes for trading and calculating moving averages.

### Constants

There are two constants defined in the code:

- `stopLossMultiplier`: This constant is used to calculate the stop loss level for opening a new position. It is multiplied by the current symbol's point value.
- `profitFactorTarget`: This constant represents the target profit factor. If the calculated profit factor meets or exceeds this value, all positions will be closed.

### Initializing the Trading Robot

The code initializes the trading robot by creating an instance of the CTrade class and setting some initial parameters. The expert magic number is set to 123456 for identification, and the maximum allowed deviation in points is set to 10.

### OnTick Function

The OnTick function is executed on each tick of the market. It performs the following actions:

1. Gets the current market price of the symbol.
2. Checks if there are any open positions.
3. If there are no open positions:
   - Calculates the stop loss level based on the stopLossMultiplier and the symbol's point value.
   - Opens a new position using the PositionOpen function of the CTrade class.
   - Prints a message indicating the opening of the position.
4. If there are open positions:
   - Calculates the profit factor by dividing the total profit by the total loss.
   - Checks if the profit factor meets or exceeds the profitFactorTarget.
   - If it does, closes all positions using the PositionCloseAll function of the CTrade class.
   - Prints a message indicating the closing of the positions.

### OnDeinit Function

The OnDeinit function is executed when the code is deinitialized. It simply prints a deinitialization message.

## Product Description

Forex Gump Gold is a trading robot developed by the Forex Robot Easy Team. It is designed to trade on the Forex market, specifically using the Gold instrument. 

This robot uses a no-risk strategy and aims to achieve a profit factor of at least 4. It opens positions based on the current market price and sets a stop loss level calculated using a multiplier. When the profit factor target is met, all positions are closed.

Please note that ForexRobotEasy is not the official developer of this product. We are only providing a sample code that can work as described in the product. To find the official developer of this product, please use MQL5.

For detailed reviews and trading results of this product, please visit the official developer's website: [Forex Gump Gold Review - No-Risk Strategy for Real Results](https://forexroboteasy.com/forex-robot-review/forex-gump-gold-review-no-risk-strategy-for-real-results/)
