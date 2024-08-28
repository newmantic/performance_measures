# performance_measures


Beta
Beta measures the sensitivity of an asset's returns to the overall market returns.
Beta = Cov(R, R_market) / Var(R_market)
where Cov(R, R_market) is the covariance between the asset returns and market returns, and Var(R_market) is the variance of market returns.

Alpha
Alpha measures the performance of an investment relative to a benchmark index.
Alpha = R_p - [R_f + Beta * (R_market - R_f)]
where R_p is the portfolio return, R_f is the risk-free rate, and R_market is the market return.

Sharpe Ratio
The Sharpe Ratio measures risk-adjusted return by dividing the excess return by the standard deviation of returns.
Sharpe = (R_p - R_f) / sigma
where sigma is the standard deviation of the portfolio returns, R_p is the portfolio return, and R_f is the risk-free rate.

Sortino Ratio
Sortino Ratio is a variation of the Sharpe Ratio that only considers downside risk.
Sortino = (R_p - R_f) / sigma_d
where sigma_d is the downside deviation (standard deviation of negative returns).

Treynor Ratio
The Treynor Ratio measures returns earned in excess of that which could have been earned on a risk-free investment per unit of market risk.
Treynor = (R_p - R_f) / Beta
where Beta is the beta of the portfolio.

Information Ratio
The Information Ratio measures the excess return of an investment over a benchmark, adjusted for tracking error.
IR = (R_p - R_b) / TE
where R_b is the benchmark return and TE is the tracking error (standard deviation of the difference between portfolio and benchmark returns).

Tracking Error
Tracking Error measures the standard deviation of the difference between the returns of an investment and its benchmark.
TE = sqrt((1/N) * Sum from i=1 to N of ((R_p_i - R_b_i)^2))
where R_p_i and R_b_i are the portfolio and benchmark returns at time i.

Maximum Drawdown
Maximum Drawdown measures the maximum observed loss from a peak to a trough of a portfolio before a new peak is attained.
MDD = min((C_i - Peak_i) / Peak_i)
where C_i is the cumulative return at time i and Peak_i is the maximum cumulative return observed up to time i.

Downside Deviation
Downside Deviation measures the standard deviation of returns that fall below a minimum threshold, typically the risk-free rate.
Downside_Dev = sqrt((1/N) * Sum from i=1 to N of (min(0, R_i - MAR)^2))
where MAR is the minimum acceptable return.

Upside Potential Ratio
The Upside Potential Ratio compares the upside potential (positive returns above a threshold) to the downside risk.
UPR = (1/N) * Sum from i=1 to N of max(0, R_i - MAR) / Downside_Dev

Omega Ratio
The Omega Ratio is the ratio of gains to losses relative to a threshold return.
Omega = Sum of (R_i > MAR) / Sum of (R_i < MAR)
where MAR is the minimum acceptable return.

Sortino Ratio
Sortino Ratio is a variation of the Sharpe Ratio that only considers downside risk.
Sortino = (R_p - R_f) / Downside_Dev

Jensen's Alpha
Jensen's Alpha measures the excess return that a portfolio generates over its expected return, given its beta and market return.
Alpha = R_p - [R_f + Beta * (R_m - R_f)]

M-Squared (Modigliani Risk-Adjusted Performance)
M-Squared adjusts a portfolio's return by its risk, making it comparable to the market return.
M^2 = R_f + Sharpe * sigma_m
where sigma_m is the standard deviation of the market returns.

Calmar Ratio
The Calmar Ratio measures the risk-adjusted return of an investment by dividing the annualized return by the maximum drawdown.
Calmar = (Annualized_Return - R_f) / Max_Drawdown

Sterling Ratio
The Sterling Ratio is similar to the Calmar Ratio, but adjusts the maximum drawdown by subtracting an arbitrary threshold (usually 10%).
Sterling = (Annualized_Return) / (Max_Drawdown + threshold)

Burke Ratio
The Burke Ratio is a variation of the Calmar Ratio that accounts for multiple drawdowns rather than just the maximum drawdown.
Burke = (Annualized_Return) / sqrt(Sum of (Drawdown_i^2))

Gain-Loss Ratio
The Gain-Loss Ratio measures the ratio of the sum of all positive returns to the absolute value of the sum of all negative returns.
Gain-Loss = (Sum of (R_i > 0)) / (Sum of (R_i < 0))

Pain Ratio
The Pain Ratio measures risk-adjusted return by dividing the excess return by the average drawdown.
Pain = (Annualized_Return - R_f) / Avg_Drawdown

Tail Ratio
The Tail Ratio measures the ratio of the 95th percentile of returns to the 5th percentile, indicating the asymmetry of the tail risks.
Tail_Ratio = P_95 / P_5
where P_95 is the 95th percentile of returns and P_5 is the 5th percentile of returns.

Capture Ratio
The Capture Ratio measures the percentage of market gains captured during up markets versus the percentage of market losses incurred during down markets.
Capture_Ratio = Up_Capture / Down_Capture
where Up_Capture is the average return of the portfolio during up markets divided by the average return of the market during up markets, and Down_Capture is the same but for down markets.

Upside Capture Ratio
The Upside Capture Ratio measures the percentage of market gains captured by a portfolio during periods when the market was positive.
Upside_Capture = (R_p_up / R_m_up)
where R_p_up is the average return of the portfolio during up markets, and R_m_up is the average return of the market during up markets.

Downside Capture Ratio
The Downside Capture Ratio measures the percentage of market losses captured by a portfolio during periods when the market was negative.
Downside_Capture = (R_p_down / R_m_down)
where R_p_down is the average return of the portfolio during down markets, and R_m_down is the average return of the market during down markets.

Kappa 3 Ratio
The Kappa 3 Ratio measures the risk-adjusted performance using the third-order lower partial moment, focusing more on downside risk.
Kappa_3 = (R_p - R_f) / LPM_3
where LPM_3 is the third-order lower partial moment, calculated as:
LPM_3 = (1/N) * Sum from i=1 to N of (min(0, R_i - MAR)^3)^(1/3)

Modified Sharpe Ratio
The Modified Sharpe Ratio adjusts the Sharpe Ratio by accounting for skewness and kurtosis.
Modified_Sharpe = (R_p - R_f) / (sigma * (1 + (Skew / 6) * Sharpe + (Kurt - 3) / 24 * Sharpe^2))
where Skew is the skewness of the returns, Kurt is the kurtosis, and Sharpe is the standard Sharpe Ratio.
