# Predicting Flight Delays Based on Distance and Carrier

Individual research project for M 358K Applied Statistics (UT Austin, Spring 2026), by Todd Sakai.

The project asks two questions about 1,993,500 domestic American Airlines and Delta Air Lines flights in 2024, using U.S. Bureau of Transportation Statistics data: does flight distance predict arrival delay, and does one carrier have longer delays than the other? It uses summary statistics, simple linear regression with a slope test, and a Welch two-sample t-test, all in R.

| Question | Result |
|---|---|
| Does distance predict delay? | Barely. The slope is significant (p < 2.2e-16), but distance explains less than 0.05% of the variation (adjusted R² = 0.0005). Each extra 1,000 miles goes with about 2.5 fewer minutes of delay. |
| Do the carriers differ? | Yes. American Airlines averaged 15.3 minutes late and Delta 3.7 minutes. The 95% confidence interval for the difference is 11.5 to 11.8 minutes. |

Files: `Predicting Flight Delays Based on Distance and Carrier.Rmd` (code and text), `Predicting Flight Delays - Todd Sakai.pdf` (report without code) and `Research_Project_Dataset.csv` (the data, with columns Carrier, Delay in minutes, and Distance in miles). 29,538 flights have no recorded delay, because they were cancelled or diverted, and are left out of the delay calculations.

To rebuild the PDF, open the `.Rmd` in RStudio and click Knit. It needs R with the `rmarkdown`, `knitr` and `readr` packages, and a LaTeX installation.
