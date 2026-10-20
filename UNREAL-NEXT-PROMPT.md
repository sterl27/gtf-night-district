# Prompt — Grand Theft Family, Unreal first milestone

You are implementing the first playable slice of Grand Theft Family in Unreal Engine 5.4 or 5.5. This is a night mob district, Sopranos and Godfather tone, GTA loop. It is not a city. Do not build Liberty City. Do not port the browser fog ray march.

## Source

District name: North Jersey night.
Block size: 32 m. Road width: 12 m. Span: 3 blocks each way from origin.
Player start: x 0, z 18. Name on the HUD: Big Sal.
Satriale’s: -32, -24. Line: “Gabagool is in the back. Do not touch the case.”
The Bing: 32, 26. Line: “Tony is not here. Leave the envelope and go.”
Genco: 64, -32. Do not build this interior in this milestone.
Envelopes: (16,-12), (-22,22), (44,-8), (60,-28). Payout 2500 each.
Gold door payout: 10000. Bing sit-down payout: 8000, plus 15 loyalty.
Heat: Fed chase starts above 32. Objective panic line above 70. Do not implement chase in this milestone. Store the heat value only.

## Done when

From a cold start you can drive the avenue, pick up one envelope, enter Satriale’s on foot, hear the line, exit to the same car, and see ziti change. The Bing door swaps. Save and load restore position and cash. Nothing else is required.
