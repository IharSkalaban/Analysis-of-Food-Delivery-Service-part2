Here, I will continue to analyze our "Food delivery service" using the same data we have already worked with ([link to part 1](https://github.com/IharSkalaban/Analysis-of-Food-Delivery-Service-))

* I will analyze the most important metrics that allow us to assess from different angles how well our product is working
* Visualize the obtained values with the integrated Redash interface and compile the final dashboard

I will place the solution for each task in individual .txt files
***

**↓↓↓** **Let's put all the graphs from the data study on one dashboard** **↓↓↓** 

[Analysis of the delivery service indicators - part 2](http://redash.public.karpov.courses/public/dashboards/XrXTbJSSl3lPnW0seovcFud1785EHdOamIovBC88?org_slug=default) 
***
### Case Study 1

Let's start with revenue, the most general indicator that shows how much revenue our service generates.

Task:

For each day in the table, calculate the following indicators:

1. **The revenue received on that day**.
2. **The total revenue for the current day**.
3. **The change in revenue received on that day, relative to the previous day's revenue**.

[1,3] [Daily Revenue and Daily Revenue Change](http://redash.public.karpov.courses/embed/query/21669/visualization/33048?api_key=eeZTdjeyOz9wWzWrm5fwXWmTWeNno6cjyanqiYYV&)

[2]   [Total Revenue](http://redash.public.karpov.courses/embed/query/21669/visualization/33050?api_key=eeZTdjeyOz9wWzWrm5fwXWmTWeNno6cjyanqiYYV&)

The solution can be found in this [file](https://github.com/IharSkalaban/Analysis-of-Food-Delivery-Service-part2/blob/main/Daily%20Revenue%20Dynamics.txt)

***
### Case Study 2

Based on the revenue data, let's calculate some relative metrics that show how much consumers are willing to pay on average for our delivery service. We will focus on the following metrics:

1. **ARPU** (Average Revenue Per User) - the average revenue per user for a given period.

2. **ARPPU** (Average Revenue Per Paying User) - average revenue per paying user for a given period. 

3. **AOV** (Average Order Value) - the average receipt or the ratio of revenue for a certain period to the total number of orders for the same time.

Task:

For each day in the tables _orders_ and _user_actions_ calculate the following indicators:

1. Revenue per user (**ARPU**) for the current day.
2. Revenue per paying user (**ARPPU**) for the current day.
3. Revenue per order, or average receipt (**AOV**) for the current day.

[1-3] [ARPU, ARRPU and AOV by Date](http://redash.public.karpov.courses/embed/query/21704/visualization/33107?api_key=kyea4u2aDZ4m3OozbR9dPX3R7RuS8zIIfeJLpWvA&)

The solution can be found in this [file](https://github.com/IharSkalaban/Analysis-of-Food-Delivery-Service-part2/blob/main/ARPU%2C%20ARRPU%20and%20AOV%20by%20Date.txt)

***
### Case Study 3

Let's complete our analysis with even more interesting calculations - let's calculate all the same metrics, but for each day we will take into account the accumulated revenue and all the currently available data on the number of users and orders. Thus, we will get the dynamic ARPU, ARPPU and AOV, and we will be able to track how it has changed over time, taking into account the data we receive.

Task:

Using the _orders_ and _user_actions_ tables, calculate the following for each day:

1. Accumulated revenue per user **(Running ARPU)**.
2. Accumulated revenue per paying user **(Running ARPPU)**.
3. Accumulated revenue per order, or average check **(Running AOV)**.

[1-3] [Runing ARPU, ARPPU and AOV by Date](http://redash.public.karpov.courses/embed/query/21723/visualization/33143?api_key=iA6FQjvrnsh7zzigxR5GyyMYn3JJg7IondHkpCW7&)
***


The solution can be found in this [file](https://github.com/IharSkalaban/Analysis-of-Food-Delivery-Service-part2/blob/main/Runing%20ARPU%2C%20ARRPU%20and%20AOV%20by%20Date.txt)

***
### Case Study 4

Let's calculate the same indicators, but in a different way - not just by day, but by day of the week.

Task:

For **each day of the week** in the _orders_ and _user_actions_ tables, calculate the following indicators:

1. Revenue per user (**ARPU**).
2. Revenue per paying user (**ARPPU**).
3. Revenue per order (**AOV**).

While calculating I will consider the data from August 26, 2022 to September 8, 2022 only, so the analysis will include the same number of all days of the week (exactly two days).

[1-3] [ARPU, ARPPU and AOV by Weekday](http://redash.public.karpov.courses/embed/query/21818/visualization/33302?api_key=nXBy5icIRNhF6IqioiEBUQM2p96VDpQX11TXED7X&)

The solution can be found in this [file](https://github.com/IharSkalaban/Analysis-of-Food-Delivery-Service-part2/blob/main/ARPU%2C%20ARPPU%20and%20AOV%20by%20Weekday.txt)

***
### Case Study 5

Let's complicate our initial query a little bit and separately calculate the daily revenue from the orders of new users of our service. Let's see what share it makes in the total revenue from the orders of all users, both new and old.

Task:

For each day in the orders and user_actions tables, calculate the following indicators:

1. The revenue received on that day.
2. The revenue from the new users' orders received on that day.
3. The share of revenue from the new users' orders in the total revenue received on that day.
4. The share of revenue from the orders of other users in the total revenue received on that day.

[Revenue from New Users](http://redash.public.karpov.courses/embed/query/21846/visualization/33348?api_key=vsTHxz8L0Rywv0s6XDQ2Lffvgm3Uc3DXBHTXBced&)

The solution can be found in this [file](https://github.com/IharSkalaban/Analysis-of-Food-Delivery-Service-part2/blob/main/Revenue%20from%20New%20Users.txt)

***
### Case Study 6

It would also be interesting to see which products are most in demand and bring us the most revenue.

Task:

For each product in the table, calculate the following for the entire period of time in the table:

1. The total revenue received from the sale of this product over the entire period.
2. The share of the revenue from the sale of this product in the total revenue received for the entire period.

Combine items whose rounded share of revenue is less than 0.5% into a common group called "ДРУГОЕ"  by summing the rounded shares of these items.

[Revenue by Products](http://redash.public.karpov.courses/embed/query/21915/visualization/33458?api_key=TKo8fo9Juzuiap5koT7l1Umad9ODKfB5wNfjN1ng&)

The solution can be found in this [file](https://github.com/IharSkalaban/Analysis-of-Food-Delivery-Service-part2/blob/main/Revenue%20by%20Products.txt)

***
### Case Study 7

Now let's try to include costs and taxes in our calculations and calculate the gross profit, that is, the amount we actually received as a result of the sale of products for the given period.

Task:

For each day in the _order_s and _courier_actions_ tables, calculate the following indicators:

1. The revenue generated on that day.
2. The costs incurred on that day.
3. The amount of VAT on the sale of products on that day.
4. The gross profit on that day (revenue less costs and VAT).
5. Total revenue for the current day.
6. Total costs for the day.
7. Total VAT for the day.
8. Total gross profit for the current day.
9. The share of gross profit in the current day's revenue.
10. The share of total gross profit in total revenue for the current day.

_To calculate costs, in this task we introduce additional conditions._

_In a simplified form, the costs of our service will be calculated as the sum of fixed and variable costs. The fixed costs will include warehouse rent, and the variable costs will include the cost of assembly and delivery of the order. Thus, the variable costs will directly depend on the number of orders._

_From the data provided to us by the financial department, we know that in August 2022 the fixed costs were 120,000 rubles per day. However, already in September our service required additional space, and therefore the fixed costs rose to 150,000 rubles per day._

_We also know that in August 2022 it cost us 140 rubles to assemble an order, at the same time we paid our couriers 150 rubles per delivered order and another 400 rubles daily as a bonus if the courier delivered at least 5 orders per day. In September, product managers managed to reduce order picking costs to 115 rubles, but we had to increase the bonus payment for delivery of 5 or more orders to 500 rubles, in order to provide a more competitive labor conditions. At the same time, the payment to couriers for one delivered order remained unchanged in September._

[Daily Gross Profit and Gross Profit Ratio](http://redash.public.karpov.courses/embed/query/21938/visualization/33522?api_key=5sSZB3njOJc7DEn0ORmoaxCBBuieHsnFFrmJ8tyo&)

[Total Gross Profit and Total Gross Profit Ratio](http://redash.public.karpov.courses/embed/query/21938/visualization/33524?api_key=5sSZB3njOJc7DEn0ORmoaxCBBuieHsnFFrmJ8tyo&)

The solution can be found in this [file](https://github.com/IharSkalaban/Analysis-of-Food-Delivery-Service-part2/blob/main/Revenue%2C%20Costs%20and%20Gross%20Profit.txt)

