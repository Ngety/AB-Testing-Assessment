# AB-Testing-Assessment
The goal of this AB Test assessment is to analyze data from a game where users can buy tokens to keep playing. The game has three different versions (Variant A, Variant B, and Variant C), and we want to determine if there are any significant differences among the versions in terms of daily total revenue, user behavior, and retention rates.

# Objective

The goal of this AB Test assessment is to analyze data from a game where users can buy tokens to keep playing. The game has three different versions and we want to determine if there are any significant differences among the versions in terms of daily total revenue, user behaviour, and retention rates. The complete code for the analysis can be found in my GitHub repository https://github.com/Ngety/AB-Testing-Assessment for reference.

Firstly we will clean our dataset and make necessary transformations to make the data suitable for analysis and to achieve that I added an extra Return_Status column, this will assist with calculating the retention rates for each game version using the 'Return_status' column.

<img width="483" alt="image" src="https://github.com/Ngety/AB-Testing-Assessment/assets/56580918/6c450cca-ec5a-4f5e-8b22-db0d18aa1181">

# Data
The dataset contains the following columns:

• DATE: The date when the user was playing the game.

• Userid: A unique identifier for each user.

• Variant: The version of the game the user received (Variant A, Variant B, or Variant C).

• Purchases: The number of purchases made by the player on that day.

• Total_purchased_amount: The total value of purchases made by the player on that day.

• Return_status: A binary indicator (0 or 1) representing whether the player returned to the game after their first play.

# Summary of Steps
1. Load the data and perform data checks to ensure data integrity.
2. Calculate and compare daily total revenue for each game version.
3. Analyze user behaviour differences in single purchase values and the number of purchases between the game versions.
4. Calculate and compare retention rates for each game version using the chi-square test of independence.

# Data Checks
Understand the dataset and performing data checks

<img width="380" alt="image" src="https://github.com/Ngety/AB-Testing-Assessment/assets/56580918/be7de9db-a819-41e3-b897-663ad77f21fe">

Checking for missing values

<img width="393" alt="image" src="https://github.com/Ngety/AB-Testing-Assessment/assets/56580918/58b7d2af-a620-458a-8fe0-9dec5966e079">

Checking the data types of each column

<img width="381" alt="image" src="https://github.com/Ngety/AB-Testing-Assessment/assets/56580918/eec28166-e4c0-461e-9eb4-17ca29a16730">

Checking the summary statistics for numeric columns

<img width="461" alt="image" src="https://github.com/Ngety/AB-Testing-Assessment/assets/56580918/0bae7117-408e-4f64-a90f-104c803cdcfe">






# Findings
# Daily Total Revenue
Calculating and Visualizing daily total revenue for each game version

We are going to calculate daily_revenue by 'Variant' and 'Total_purchased_amount'sum ()

<img width="437" alt="image" src="https://github.com/Ngety/AB-Testing-Assessment/assets/56580918/5c3fc095-3f80-4aae-80ed-cb7078b6443f">

# Hypothesis

There isn’t a significant difference when comparing daily total revenue for each game, from the data we can see that Version generates the highest daily total revenue compared version 2 and 3.

Null Hypothesis (H0): There is no significant difference in the daily total revenue generated by the different game versions (Version 1, Version 2, and Version 3).

Alternative Hypothesis (H1): There is a slight difference in the daily total revenue generated by the different game versions.

# User Behaviour Analysis

Analyzing user behavior differences in single purchase values and number of purchases and split data by game versions.

We are going to calculate single purchase values

<img width="441" alt="image" src="https://github.com/Ngety/AB-Testing-Assessment/assets/56580918/025738c2-80ef-4ab5-9e5f-e85a61cb6037">

# Hypothesis
Single Purchase Values:

There is a significant difference in single purchase values between the three game versions. We can see version 2 is higher in single purchase values compared to version 1 and 3. Version 3 has the lowest single purchase value.

Alternative Hypothesis (H1): There is a significant difference in the single purchase values between all three of the game versions.

Now we are gonna proceed and visualize number of purchases

<img width="440" alt="image" src="https://github.com/Ngety/AB-Testing-Assessment/assets/56580918/454e4edd-3f29-4bb8-a3d1-820af2d2543c">

# Hypothesis
Number of Purchases:

Null Hypothesis (H0): There is no significant difference in the number of purchases between version 1 and 2.

Alternative Hypothesis (H1): There is a significant difference in the number of purchases when comparing version 3 to version 1 and 2, version 3 has lower purchases compared to the two.

# Retention Rates

 We will compare retention rates for each game version, in this step we will Calculate and visualize daily retention and acquisition rates for each cohort. For simplicity, let's consider retention and acquisition for a 7-day period. We will Calculate retention rates for each cohort and day.

<img width="649" alt="image" src="https://github.com/Ngety/AB-Testing-Assessment/assets/56580918/a3956940-5023-43dc-889d-a741e6c8f3fd">

# Hypothesis

Null Hypothesis (H0): There is no significant difference in the retention rates among the three game versions.

# Conclusion

Based on the AB Test hypothesis, we can conclude that the game versions have different impacts on daily total revenue, user behavior, and retention rates. Version 3 is the lowest performing, although there is no significant difference in single purchase values between Version 1 and Version 2, Version 3 shows lower single purchase values. The business should investigate the possible reasons behind this difference and consider implementing strategies to improve the single purchase values in Version 3. This could include offering attractive incentives or promotions to encourage higher-value purchases. Version 2 is consistent and the business should consider focusing on Version 2 and implementing its features in the other versions or future game updates to maximize revenue and retention. The business should engage with the game’s player community to gather consumer feedback.

