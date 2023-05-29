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

3-

**SELECT** products.name

**FROM** orders

**JOIN** orders_items **ON** orders.id = orders_items.id_order

**JOIN** products **ON** orders_items.id_product = products.id

**JOIN** customers **ON** orders.id_customer = customers.id

**WHERE** customers.country = 'Italy'

**ORDER BY** products.price **DESC**

**LIMIT** 1;

4- To optimize the orders table for managing a lot of queries is possible to identify the commonly queried columns and create indexes on those columns, this can speed up the search and retrieval process. Another solution cal be to implement a caching mechanism to store frequently accessed data in memory, this can reduce the need for repeated database queries and improve overall system performance.

5- There are several approaches to do it but the ones that seem to be better use distributed database systems that can distribute the data across multiple nodes or servers to allows for parallel processing and improves query performance on large datasets and split the data into smaller partitions and distribute them across multiple storage systems. This can improve query performance by allowing parallel processing and reducing the load on individual systems.


