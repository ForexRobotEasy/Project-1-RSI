# Project 1 RSI Expert Advisor

This is the code for the Project 1 RSI Expert Advisor developed by the Forex Robot Easy Team. The Expert Advisor is designed to trade based on the Relative Strength Index (RSI) indicator.

## Expert Advisor Input Parameters

- RSI_Period: The period used for calculating the RSI indicator (default: 14).
- RSI_Buy_Level: The buy level for the RSI indicator (default: 30.0).
- RSI_Sell_Level: The sell level for the RSI indicator (default: 70.0).
- Use_Volatility_Control: Enable or disable volatility control (default: true).
- Volatility_Threshold: The threshold for volatility control (default: 0.5).

## Global Variables

- RSI_Buffer: An array used to store RSI values.
- prev_volatility: The previous volatility value.

## Initialization Function

The OnInit() function is responsible for initializing the Expert Advisor. It preallocates memory for the RSI buffer using the ArrayResize() function.

## Tick Function

The OnTick() function is called on every tick of the price. It calculates the RSI using the iRSI() function and checks if the calculation is successful. If successful, it retrieves the current RSI value.

The function then checks for buy and sell signals based on the RSI levels. If the current RSI is below or equal to the buy level and volatility control is disabled or the previous volatility is below the volatility threshold, a buy order is placed using the OrderSend() function.

Similarly, if the current RSI is above or equal to the sell level and volatility control is disabled or the previous volatility is below the volatility threshold, a sell order is placed.

The previous volatility value is then updated using the iATR() function.

## Deinitialization Function

The OnDeinit() function is called when the Expert Advisor is being shut down. It frees the memory allocated for the RSI buffer using the ArrayFree() function.

Please note that Forex Robot Easy is not the official developer of this product. We only provide a sample code that can work as described in this product. To find the official developer of this product, please refer to MQL5.

For detailed reviews and trading results of this product, please visit [Forex Robot Easy - Project 1 RSI Review](https://forexroboteasy.com/forex-robot-review/project-1-rsi-review-enhance-trading-with-data-driven-tool/).
