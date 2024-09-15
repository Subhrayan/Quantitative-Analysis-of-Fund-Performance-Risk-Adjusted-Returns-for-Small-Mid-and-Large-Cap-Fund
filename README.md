# Quantitative-Analysis-of-Fund-Performance-Risk-Adjusted-Returns-for-Small-Mid-and-Large-Cap-Funds
This project analyzes the performance of small, mid, and large cap funds from 2020 to 2023. Using linear regression, it calculates volatility and risk-adjusted returns based on closing indices data, providing insights into each fund's risk and performance.
## Objectives:
So, as we know in 2020 due to COVID-19 and in 2022 due to Russia-Ukraine war Indian stock market went through a deep red. It fell sharply. Although it recovered but as an stock market enthusiast I decided to analyze their perfomance from the start of 2020 to end of 2023. My main motive was to draw a quantitative view about how each of these funds reacted during thet period of time and in the end which gave a better returns taking volatility into account. 
Starting with the data source, here for this project I collected all 4 year data of small, mid and large cap funds from  https://www.bseindia.com/Indices/IndexArchiveData.html this website. I only considered their closing price of each day. Total 994 days of data was there.
## Data Visualization:
![Screenshot 2024-09-15 204644](https://github.com/user-attachments/assets/4ce107cf-87ce-4230-9b10-40048133e736) **This graph presents their performance over 4 years.**
## Evaluating rewards using Linear Regression:
Then I used Linear Regression method to quantify their returns/reward over 4 years.

![340003886-d56d38ca-4409-4ba5-82f4-c1af22b7eac2](https://github.com/user-attachments/assets/92616328-ecb8-483f-bca6-2f9b0e12dbc5)
![340003942-f25b5196-c83e-474f-ae04-2a864eda505a](https://github.com/user-attachments/assets/cdcc8f56-f81a-4e01-8fd0-74dbf4ffedd3)

**Here I got intercept parameter and coefficients for all the funds, where each fund has been taken as both independent and dependent variable.**


![340004163-ddaf6b6f-27c1-45a3-bd2c-69db7e9fc00e](https://github.com/user-attachments/assets/c03f230c-6d37-4501-ab95-a9bdbf753c69)
![340004482-c2802d32-057d-44dc-acf9-a572243137ea](https://github.com/user-attachments/assets/b8647508-4024-4a5c-ab5f-978f03429939)

**So these are the residuals for each of the cases. Which represents how much the predicted value of each funds deviates from the actual value.**

![340005742-a49934f7-e980-486c-be19-cec260b9ade3](https://github.com/user-attachments/assets/be981248-c9db-4b53-b79e-972b72de92f4)

**This is the correlation between funds.**

![340005808-d985a943-3f4c-404d-acaf-e15aaed57a62](https://github.com/user-attachments/assets/12fd1329-8d70-4f83-8e21-ba0ba0fedb4c)

**This the reward of each of the funds, which I got from the sumproduct of residual percentage and correlation.**
## Volatility Measurement:
![340006457-fc63d1e4-8a83-4219-9bf5-969f6d54f2be](https://github.com/user-attachments/assets/23b2938c-e14b-46ee-99f6-db07f8f98b60)

**This shows the volatility of 3 funds.**

To get this first I calculated their per day percentage change in their points from previous day and then got standard deviance of that. Then multiplied sqrt of 252 with standard devance to get volatility of each fund.
## Evaluating Risk-Adjusted reward of all funds:
![340008454-0746c841-4837-4dfd-aae5-20e70561a559](https://github.com/user-attachments/assets/43c51e6e-a95c-4edf-b7dd-d7a0efd147a5)

**This shows the risk-adjusted-reward of small, mid and large cap funds.**

This involves dividing the reward by volatility.

## Result:
 * This suggests that mid cap funds offered the most favorable balance of risk and reward of 0.22, making them an attractive option for investors seeking optimized returns relative to their risk exposure.
 * Small cap funds showed lower risk-adjusted return than mid-cap. Although small cap funds usually give higher returns due to their small market cap and high growth rate but in this period it fell short of mid cap when risk considered as it showed much volatility as compared to mid cap.
 * Large-cap funds showed a negative risk-adjusted reward of -0.19. This result indicates that, over the analysed period, large-cap funds did not provide adequate returns relative to the risks involved.
