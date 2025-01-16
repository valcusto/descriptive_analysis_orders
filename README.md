# Descriptive analysis
## Business problem
SuperStore is a supermarket chain with multiple physical stores that aim to supply a variety of consumer products. SuperStore management has set an objective to use data to streamline decision-making related to product restocking and store sales. To attain this goal, the company intends to access transactional data to analyse customer behaviour. This includes identifying the highly purchased and returned products, the number of orders within a given timeframe, and more. However, before addressing those aim the management team would like to know:

1.	How are SuperStore’s orders performing?

## Solution
To address this problem, I will use descriptive analysis to answer the management question. For that, I will follow the five key steps of data analysis:

1.	**Define the fact:** This critical step helps to 1) establish the aim of the analysis, 2) identify relevant business events, and 3) select the appropriate metrics for the analysis.
 
2.	**Define the dimensions:** Dimensions are qualitative attributes that provide context to the fact.
 
3.	**Combine fact and dimensions:** this step characterizes the fact by linking it to the dimensions, providing meaningful context and insights. 
 
4.	**Select appropriate visualization tools:** choosing the right graphical tools ensures the data is presented clearly and effectively. 
 
5.	**Present macro and micro views:** the final step involves providing macro perspectives (broad trends) and micro-level details (specific insights) of the fact. 
 
The solution's planning involved applying the SAPE method developed by the Comunidade DS. This method encompasses the definition of an output (SA: saida), the process (P), and the input (E: entrada).

## Planning (SAPE and Five steps of data analysis)
### 1.	Define the fact
Order ID
### 2.	Define the dimensions

| Column        | Dimension     | Description |
| ------------- | ------------- |-------------|
| Order Date    | Time          | When?       |
|Ship Date      |               |	      | 	
|Ship Mode	| Delivery	| How?        |
|Customer ID	| Customer      | Who?        | 
|Sales	        | Product       | What?       |
|Quantity		
|Discount		
|Product ID		
### 3.	Combine fact and dimensions

1.	Order number per date (month, year, week, holidays)
 
2.	Order number per shipping date (month, year, week, holidays)
 
3.	Order number per price tiers (low, medium, high)
 
4.	Order number per items quantity in an order
 
5.	Order number per discount tiers (low, medium, high)
   
6.	Order number per products
   
7.	Order number per customers
   
8.	Order number per date and price tiers
    
9.	Order number per date and items quantity
    
10.	Oder number per date and product
    
11.	Order number per date and customer
    
12.	Order number per shipping date and price tiers
### 4.	Hypothesis
Which panels will answer the question? Order number per time

Expected results? The order number increase across time

Why? 

H1: The customer number increased.

Panel 1: Order number per customers

Panel 2: Customer number per time

H2: The items quantity increased. 

Panel 1: Order number per items quantity

H3: The product influence on the order
 
Panel 1: Distributions of the product per order
	
### 5.	Select appropriate visualization tools
|Graph	|Message	|Vizualization|
| ------| --------------| ------------| 
Order number per date (month, year, week, holidays)|	1.	Growth | 1.	Line plot|
|   | 2.	Comparisons per day |	 2.	Column plot|
|Order number per items quantity in an order |	1.	Growth | 1.	Line plot |
|    |2.	Comparisons per day | 2.	Column plot |
|Order number per customers |	1.	Comparisons per day |	1.	Column plot
|Order number per products  |	1.	Distribution of the products |	1.	Pizza plot
### 6.	Output (Saida)
Dashboard with the panels

### 7.	Process

a)	Draw the line plot with the order number per time

b)	Draw line plot with the number of customer per time

c)	Draw bar plot with the number of customers per order number

d)	Draw a bar plot with the number of orders per number of items (shop size)

e)	Draw a pizza plot with the product category distribution
### 8.	Input (Entrada)
Orders.csv file
### 9.	Dashboard vision
![image](https://github.com/user-attachments/assets/5b33830d-ed98-4381-8569-002be09f2ed4)

 
## Results and insights
To answer the Superstore management questions related to order performance, I analysed the order number from 2014 to 2017. In this analysis, I considered the order ID information as the fact, the information I’m interested in, and to provide context to the fact (dimensions), I defined the following variables as dimension: ship mode, customer ID, quantity, and order date. 

The analysis of the order number shows an increase. By analysing this variable per month, I found that in January, a total of 381 orders were made, which slightly decreased in February (300 orders). In March, the orders increased to 696, which maintained more or less the same amount, around 600 to 700 until August. Due to the marketing campaign, the order number increased almost 2x to 1383 in September. Then, after the decrease in October, the order number increased again, this time higher than the previous months, and stayed the same until December. This result suggests that despite the seasonal increase in sales, the order number generally increases across the year.

To have a deeper understanding of the factors that influence these fluctuations in the order number, I analysed the customer number pattern across the year, the order number per unique customer, the order number per cart size, and the order distribution per ship mode. As expected, I found that the customer number fluctuated similarly to the order number. For example, there was a slight decrease in customer numbers in February compared to January. Meanwhile, in March, there was an increase in the number of customers, and the number of customers remained around 300 until August. Then, in September, there was 2x growth in the customer number, followed by a decrease in October. Finally, there was an observed increase in customer numbers in November, followed by a slight decrease in December. These results suggested that the increase in the order number across the months could be due to the unique customer increase across the same months. 

Then, I wondered whether this unique customer ordered more items in the months we observed an increase in the order numbers. To answer that question, I analyse the average order number performed by the customers. I found that the average order number was around 2.4 orders per customer. Then, we significantly increased order numbers in September and November, where the average order number per customer was 3. Regarding products, I found that most orders contain 2 to 3 products in the shopping cart. Additionally, I found a significant decrease in order numbers for the shopping cart with more than 6 products. Considering these results, we observed that customers are making quick purchases rather than making plans and massive purchases. Regarding how customers want the delivery to be made, 60% have the standard shipment (3-5 days), suggesting that the customers' purchases are not urgent.

