# WagerBrain
A package containing the essential math and tools required for sports betting and gambling. Once you've scraped odds from Covers.com, Pinnacle, Betfair, or wherever, import WagerBrain and start hunting for value bets.

![Image of The Big Board](https://miro.medium.com/max/1312/1*bGOGcEPpsa0tetM5u-J9NA.jpeg)

**Phase 1 (_first iteration complete_):** 
 - Convert Odds between American, Decimal, Fractional
 - Convert Odds to Implied Win Probabilities and back to Odds
 - Calculate Profit and Total Payouts
 - Calculate Expected Value
 - Calculate Kelly Criterion
 - Calculate Parlay Odds, Total Payout, Profit
 - Calculate the Bookmaker's Vig
 
 **Phase 2 (_in progress_):**
 - Complex bankroll management on a multi-bet or portfolio scale
 - Calculate bookmaker spread/cost
 - Clean up functions into logical classes
 
 **Phase 3 (_not started_):**
 - Value Bets (take in sets of odds, probabilities and output the most effective betting implementation)
 - Arbitrage (search sets of odds, probabilities and return, if available, arbitrage opportunities)
 - Visualization (compare all wager opportunities, et al)
 
  **Phase 4 (_not started_):**
  - Automation and Intelligence (e.g., Using phases 1-3 as tools, develop ML and AI models to make predictions, manage bankroll, execute bets)

#**Examples**

Parlay 3 wagers from different sites offering different odds-styles:
```
odds = [1.91, -110, '9/10']
parlay_odds(odds)
6.92
```
No clue how to read decimal odds because you're American? (wager * decimals odds, though...super simple), then convert them back to American-style odds:
```
american_odds(6.92)
+592
```
What's the Vig on the Yankees vs Dodgers?
```
Yankees -115
Dodgers +105
Betting 115 to win 100 on Yankees
Betting 100 to win 205 on Dodgers

vig(115,215,100,205)
2.26%
```
