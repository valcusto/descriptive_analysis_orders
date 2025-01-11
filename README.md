# Descriptive analysis
## Business problem
SuperStore is a supermarket chain with multiple physical stores that aim to supply food and a variety of consumer products. The SuperStore management has set an objective to use data to streamline decision making related to product restocking and sales in stores. To attain this goal, the company intends to access transactional data to analyse customer behaviour. This includes identifying the highly purchase products, returned products, the number of orders with a given timeframe and more. However, before address those aim the management team would like to know:
1.	How are SuperStore’s orders performing?
   
## Solution
To address this problem, I will use descriptive analysis to answer the management question. For that, I will follow the five key steps of data analysis:
1.	Define the fact: This critical step helps to 1) establish the aim of the analysis, 2) identify relevant business events, and 3) select the appropriate metrics for the analysis.
2.	Define the dimensions: Dimensions are qualitative attributes that provide context to the fact
3.	Combine fact and dimensions: this step characterizes the fact by linking it to the dimensions, providing meaningful context and insights. 
4.	Select appropriate visualization tools: choosing the right graphical tools ensures the data is presented clearly and effectively. 
5.	Present macro and micro views: the final step involves providing macro perspectives (broad trends) and micro-level details (specific insights) of the fact. 
The solution's planning involved applying the SAPE method developed by the Comunidade DS. This method encompasses the definition of an output (SA: saida), the process (P) and the input (E: entrada).
Planning (SAPE and Five steps of data analysis)
1.	Define the fact
Order ID
2.	Define the dimensions
Column	Dimensions	Description
Order Date	Time	When?
Ship Date		
Ship Mode	Delivery	How?
Customer ID	Customer	Who?
Sales	Product	What?
Quantity		
Discount		
Product ID		
3.	Combine fact and dimensions
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
4.	Hypothesis
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
	
5.	Select appropriate visualization tools
Graph	Message	Vizualization
Order number per date (month, year, week, holidays)	1.	Growth
2.	Comparisons per day	1.	Line plot
2.	Column plot
Order number per items quantity in an order	1.	Growth
2.	Comparisons per day	1.	Line plot
2.	Column plot
Order number per customers	1.	Comparisons per day	1.	Column plot
Order number per products	1.	Distribution of the products	1.	Pizza plot
6.	Output (Saida)
Dashboard with the panels

7.	Process
a)	Draw the line plot with the order number per time
b)	Draw line plot with the number of customer per time
c)	Draw bar plot with the number of customers per order number
d)	Draw a bar plot with the number of orders per number of items (shop size)
e)	Draw a pizza plot with the product category distribution
8.	Input (Entrada)
Orders.csv file
9.	Dashboard vision
 
## Results and insights
To understand the order performance at SuperStore, we analyse the order number across the months. We found in general an increase in the order number. In January, a total of 381 orders was made and there was a slight decrease of this number em February (300 orders). In March, the orders increase to 696 and the orders maintain more or less the same amount around 600 to 700 untill August. In August, due to the marketing campaign the order number increase almost 2x to 1383. Then, after the decrease in October, the order number increase higher than the previous month and stay the same till December. Similarly to the order number, the customer number decrease slight in February. In March, there was an increase in the customer number and the number of customer maintain around 300 until August. Then, in September there was 2x growth in the customer number followed by a decrease in October. In November, there was again an increase follow by a small decrease in December. These results suggested that the increase in the order number across the months could be due to the increase in the unique customer increase across the same months. However, we wonder whether was the customer number or the order number per customer that was the responsible for the order number increase. For that, we analyse the average order number performed by the customers. We found that the average order number was around 2.4 order per customer. Then, in September and November, the months that we had an significant increase in order number, the average order number per client was 3. 
Related to product we found that the majority of the order contain 2 to 3 products in the shopping cart. Additionally, we found a significant decrease in order number for the shopping cart with more than 6 products. This result suggest that the customers are doing quick buy and not a plan and massive buy. Related to the way customer want the delivery to be made, 60% have the standard shipment, suggesting that is not urgent buy, 3-5 days. 
