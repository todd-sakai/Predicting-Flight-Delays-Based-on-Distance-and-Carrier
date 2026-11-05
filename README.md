# Predicting Flight Delays Based on Distance and Carrier

This project answers two questions about 1,993,500 domestic American Airlines and Delta Air Lines flights in 2024, using U.S. Bureau of Transportation Statistics data:
1. does flight distance predict arrival delay?
2. Does one carrier have longer delays than the other?

I used summary statistics, simple linear regression with a slope test, and a Welch two-sample t-test, all in R.

| Question | Result |
|---|---|
| Does distance predict delay? | Barely. The slope is significant (p < 2.2e-16), but distance explains less than 0.05% of the variation (adjusted R² = 0.0005). Each extra 1,000 miles goes with about 2.5 fewer minutes of delay. |
| Do the carriers differ? | Yes. American Airlines averaged 15.3 minutes late and Delta 3.7 minutes. The 95% confidence interval for the difference is 11.5 to 11.8 minutes. |

Files:
- `Predicting Flight Delays Based on Distance and Carrier.Rmd`: Code and text
- `Research_Project_Dataset.csv`: The data, with columns Carrier, Delay in minutes, and Distance in miles
