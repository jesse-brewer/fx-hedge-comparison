# The purpose of this script
The business pays AUD suppliers from CNH holdings, so every month we're exposed to the exchange rate on the day. If AUD strengthens, the same bill costs more CNH.

Banks offer forwards to fix the rate ahead of time, but the quotes come in different shapes and it isn't obvious which is cheaper until you see how each behaves as the rate moves. 

This model supports the decision with real outcome analyses.

# Real workplace application
Full case study: [FX_Hedging_Case_Study.pdf](FX_Hedging_Case_Study.pdf)

----------------------
# How the forwards work
Par forward: Agree to a fixed rate today and pay that regardless of where the market ends up. The bank sets it close to current spot. Outcome is certain. The downside is if AUD weakens, it is more expensive than buying at spot.

Capped forward: Agree to a lower rate than the par forward that applies so long as spot stays at or below a cap. If spot is above the cap at maturity, you buy at spot and receive a fixed rebate of (cap − strike) instead.

# The three options
Do nothing      -  Buy AUD at spot on the day
Par forward     -  Fix one rate for the full amount
Capped forward  -  Fix a better rate, but give up protection above a cap

----------------------
# Required libraries
`pip install yfinance pandas numpy matplotlib`