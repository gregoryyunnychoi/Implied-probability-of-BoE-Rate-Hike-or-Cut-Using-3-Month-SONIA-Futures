## Implied probability of BoE Rate Hike or Cut Using 3-Month SONIA Futures

This project is inspired by the CME's [FedWatch Tool](https://www.cmegroup.com/articles/2023/understanding-the-cme-group-fedwatch-tool-methodology.html), which infers the probability of US Federal Reserve rate changes from Fed Funds futures. While there is no direct UK equivalent, the closest instrument is the Three-Month SONIA Index Futures. Implying Bank of England (BoE) rate change probabilities is more complex, however, as there is no SONIA futures contract that corresponds to a period without a Monetary Policy Committee (MPC) meeting, which is used in the FedWatch methodology as an "anchor" period.

This analysis adapts the FedWatch approach to the UK context, using quarterly SONIA futures (only four contracts per year). In the absence of a quarter without an MPC meeting, we relax the original assumption that an anchor period must be free of rate-setting meetings. Instead, we calculate probabilities under two scenarios:  
1. Using the **previous quarter as the anchor**, assuming the implied rate at the start of the quarter remains constant.  
2. Using the **following quarter as the anchor**, assuming the implied rate at the end of the quarter remains constant.

While this introduces some subjectivity, it's worth noting that even the CME FedWatch Tool assumes futures prices for months without FOMC meetings are independent of the month following, despite those months being adjacent to decision dates. This suggests that the assumption of a "no-meeting" anchor is not critical to the overall methodology.

This project presents a range of rate hike or cut probabilities based on both anchoring approaches, allowing users to interpret the results according to their preferred assumptions.

You can find the .xlsx model that detail the calculation named BoEwatch-calculation-examples.xlsx

**Note**: Currently, the market-implied interest rate in the UK, as provided by major data vendors, is derived from the Overnight Indexed Swap (OIS) rate. OIS rates are negotiated over-the-counter (OTC) rather than traded on a standardised exchange or through a central clearinghouse. Consequently, the rates may not consistently reflect real-time market sentiment on its view on the BoE's rate decision considering its low liquidity. Furthermore, OIS rates are subject to interpolation techniques, which can vary between data providers. In contrast, 3-month SONIA futures are exchange-traded instruments with standardised contracts and centralised clearing. They tend to have greater transparency and are less susceptible to interpolation discrepancies. As a result, the future market often provide a more liquid and accurate reflection of market expectations for short-term interest rates.

### Implied rate cut probability as of 22 May 2025

As of **22 May 2025**, the market-implied probabilities of Bank of England (BoE) rate cuts at the next two Monetary Policy Committee (MPC) meetings are as follows:

- **84% probability** of two 25bps rate cuts (totaling 50bps) when using the **Mar 2025 (Q2)** SONIA futures contract as the anchor.
- **37% probability** of two 25bps rate cuts when using the **Sep 2025 (Q4)** SONIA futures contract as the anchor.

![Rate Cut Probability Chart](https://github.com/user-attachments/assets/45e465fc-27ba-4e12-aceb-74d7f6a27307)

These probabilities suggest that the market expects **at least one rate cut** between June and September 2025. However, there is uncertainty over whether the MPC will implement **one or two cuts** during this period.
