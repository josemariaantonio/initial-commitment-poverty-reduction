README
This notebook provides a detailed analysis of global poverty convergence and its relationship with economic indicators.
Key Analyses and Findings:
1. Beta-Convergence Analysis:
    * Objective: To determine if countries with higher initial poverty levels experienced faster rates of poverty reduction.
    * Finding: Strong evidence of beta-convergence was found (β = -0.409, p < 0.001), indicating that poorer countries tended to catch up faster in terms of poverty reduction.
2. Sigma-Convergence Analysis:
    * Objective: To assess the narrowing or widening of the cross-country dispersion of poverty rates over time.
    * Finding: An initial narrowing trend (sigma-convergence) was observed, but disruptions after 2015 led to a widening of dispersion, and the coefficient of variation increased after 2013.
3. Poverty Reduction vs. Initial GDP per Capita:
    * Objective: To analyze the relationship between the rate of poverty reduction and a country's initial GDP per capita.
    * Methodology: GDP per capita data was fetched using wbgapi and merged with poverty data.
    * Finding: A statistically significant positive slope (β = 0.389, p = 0.013) suggested that countries with higher initial GDP per capita experienced a slower rate of poverty reduction, highlighting the importance of inclusive growth policies.
    * Visualizations: Scatter plots (fig_poverty_vs_gdp_scatter.png, fig_poverty_vs_log_gdp_regression_scatter.png) were generated to illustrate this relationship.
4. ARIMA Forecasting for Sigma Convergence:
    * Objective: To forecast future trends in the dispersion of poverty rates.
    * Methodology: An ARIMA model was developed, with a grid search identifying ARIMA(0, 2, 2) as the optimal model (AIC: 138.66) based on minimizing the Akaike Information Criterion.
    * Forecast: A 5-year forecast was generated, projecting a continued increase in the cross-country standard deviation of poverty rates, with widening confidence intervals.
    * Visualization: The forecast was visualized and saved as fig_arima_sigma_forecast.png.
Usage:
1. Ensure the World Bank poverty data file (API_SI.POV.DDAY_DS2_en_excel_v2_261020.xls) is available in the Colab environment (upload if necessary).
2. Run all cells in sequence.
3. Generated figures (fig5_beta_convergence.png, fig6_sigma_convergence.png, fig_poverty_vs_gdp_scatter.png, fig_poverty_vs_log_gdp_regression_scatter.png, fig_arima_sigma_forecast.png) will be saved locally in the Colab session.
