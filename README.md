## Probability of BoE Rate Hike or Cut Using 3-Month SONIA Futures

This project is inspired by the CME's [FedWatch Tool](https://www.cmegroup.com/articles/2023/understanding-the-cme-group-fedwatch-tool-methodology.html), which infers the probability of US Federal Reserve rate changes from Fed Funds futures. While there is no direct UK equivalent, the closest instrument is the Three-Month SONIA Index Futures. Estimating Bank of England (BoE) rate change probabilities is more complex, however, as there is no SONIA futures contract that corresponds to a period without a Monetary Policy Committee (MPC) meeting—commonly used in the FedWatch methodology as a "neutral" or "anchor" period.

This analysis adapts the FedWatch approach to the UK context, using quarterly SONIA futures (only four contracts per year). In the absence of a quarter without an MPC meeting, we relax the original assumption that an anchor period must be free of rate-setting meetings. Instead, we calculate probabilities under two scenarios:  
1. Using the **previous quarter as the anchor**, assuming the implied rate at the start of the quarter remains constant.  
2. Using the **following quarter as the anchor**, assuming the implied rate at the end of the quarter remains constant.

While this introduces some subjectivity, it's worth noting that even the CME FedWatch Tool assumes futures prices for months without FOMC meetings are independent of the month following, despite those months being adjacent to decision dates. This suggests that the assumption of a "no-meeting" anchor is not critical to the overall methodology.

This project presents a range of rate hike or cut probabilities based on both anchoring approaches, allowing users to interpret the results according to their preferred assumptions.
