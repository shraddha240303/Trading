# Trading
What is the Fear & Greed Index?
Imagine the stock market is like a crowd at a sale. When everyone is excited and rushing to buy, that is "Greed." When everyone is scared and running away, that is "Fear." The Fear & Greed Index is a number from 0 to 100 that measures this crowd mood for Bitcoin every single day.
Analogy: Think of it like a "panic meter" at a cricket match. If India is winning, everyone is happy (Greed = 80+). If India is losing badly, everyone panics (Fear = 20-).
What is Hyperliquid trader data?
Hyperliquid is a crypto trading platform. The data shows every single buy and sell trade made by 32 real traders — like a full transaction ledger. It tells you who traded, what they traded, how much they made or lost, and when.
Analogy: Imagine you have the complete bank statement of 32 people for 6 months. You can see every rupee they spent and earned.
What is your goal?
You want to find out: Does the crowd mood (Fear/Greed) affect how much profit traders make? For example — do traders earn more when Bitcoin sentiment is "Extreme Greed"? Do they make mistakes when everyone is panicking? This is what you will prove with data.

Column-by-column explanation

Fear & Greed CSV
timestamp - A Unix timestamp — the number of seconds since Jan 1, 1970. It is a universal way computers store time. You will convert this to a readable date in Python.
value - A number from 0 to 100. The actual sentiment score for that day. 0 = pure panic, 100 = pure euphoria. This is the raw signal you will use for analysis.
classification - The human-readable label for the value. There are 5 categories: Extreme Fear (0–24), Fear (25–44), Neutral (45–55), Greed (56–74), Extreme Greed (75–100). This is what you will use to group your trader data.
date - The date in YYYY-MM-DD format. You will use this as the key to join with your trader dataset — matching each trade to the sentiment of that day.

Historic CSV
Account - A wallet address — a unique ID for each trader on the blockchain. Like an anonymous bank account number. You have 32 unique traders.
Coin - Which cryptocurrency was traded. Examples: BTC (Bitcoin), ETH (Ethereum), HYPE, SOL. The "@107" is an internal Hyperliquid token ID.
Execution Price - The actual price at which the trade happened. Not the price you wanted — the price you got. Important for slippage analysis.
Size Tokens & Size USD - How many coins were traded (Size Tokens) and what that was worth in dollars (Size USD). Size USD is more useful for comparison across different coins. Buying 100 DOGE is different from buying 100 BTC. Size USD tells you the real dollar value of each trade.
Side - BUY or SELL. Simple — did the trader open a long position (expecting price to rise) or short (expecting fall)?
Timestamp IST - Date and time of the trade in Indian Standard Time. Format: DD-MM-YYYY HH:MM. You will parse this and extract just the date to match with the sentiment data.

