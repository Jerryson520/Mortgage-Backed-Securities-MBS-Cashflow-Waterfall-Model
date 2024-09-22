# Mortgage-Backed-Securities-MBS-Cashflow-Waterfall-Model

Implement a cashflow waterfall model for a hypothetical Mortgage-Backed Security using provided mortgage data.


Given:
- A file containing data for 15 mortgages ($100million total balance), including their respective unpaid principal balances, interest
rates (annual), and terms (in months).

Bond Structure Description:
- Three classes of bonds: A, B, and C
- Principal paid sequentially: Class A gets ALL aggregated principal from the collateral paid each period until its balance has reached 0.
Then, once Class A is paid oﬀ, Class B begins to get ALL principal each period until its balance has reached 0.
Then, once Class A and Class B are paid oﬀ, Class C is paid the ALL remaining principal each period until its balance has reached 0.
- Interest paid sequentially to all bonds in every period (A, then B, then C): Unlike principal payments, each bond will get its interest
payments in every period based on their then current balance.
- Initial principal balances:
  * Class A: $70,000,000

  * Class B: $20,000,000

  * Class C: $10,000,000
- Interest rates for all bonds: Equal to the gross weighted average interest rate of the collateral (weighted by then current collateral
balance)

Tasks:
1. Design and implement the waterfall mechanism to distribute the aggregated cashflows to the bonds according to the
specified structure:
* Payment Sequence:
  * Pay interest to all bonds sequentially (A, then B, then C) in each period from the period’s aggregate interest.
  * Pay principal to Class A bond from the period’s aggregate principal, until fully paid oﬀ.
  * Once Class A is paid oﬀ, pay principal to Class B bond from the period’s aggregate principal, until fully paid oﬀ.
  * Once Class B is paid oﬀ, pay principal to Class C bond from the period’s aggregate principal, until fully paid oﬀ.
