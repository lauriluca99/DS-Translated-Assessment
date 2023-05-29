### Questions:

1- Can you explain the purpose of the orders_items table?

2- Can you write a SQL query to find the average order cost per country?

3- Can you write a SQL query to find the name of the highest price product sold to an Italian customer?

4- How could you optimize the orders table assuming you have to manage a lot of queries?

5- What would you change if the amount of data is too big to run these queries? (suppose to have 500TB of data)


### Answers:
1- The purpose of the orders_items table is to establish a relationship between orders and products. It stores the details of each product within an order.

2- 
**SELECT** country, **AVG**(order_cost) **AS** average_order_cost
**FROM** orders
**JOIN** customers **ON** orders.id_customer = customers.id
**GROUP BY** country;

