### Project Name: Exploring Skims' Best-Selling Products
***
### Project Objective
##### What problem are you solving?
Skims currently has over 50 various products on their best sellers tab on their webpage. While this shows that these products sell particularly better than others, it is unclear exactly why this is the case. To better understand this, I will be analyzing all 52 best selling products and dive deeper as to what makes these products popular as well as find patterns amongst the products. This will allow various stakeholders to have a stronger understanding on their products and make strategic decisions based on the insights.
##### How are you solving this problem?
I will be solving this problem by collecting all relevant data found on the best sellers page. I will first web scrape all product names, prices, average ratings from customers (out of 5 stars), and the total reviews it has received. As I do not have access to any invoice information, I will be using the count of reviews in replace of the order count. I will look for trends and patterns within the products on the best sellers page and analyze why certain products are more popular than others.
***
### Job Description
Skims is an American women’s clothing wear brand founded by three women and has quickly risen to success since its launch in 2019. They are seeking a Data Analyst to be a founding member of their Data and Analytics team. One of the main responsibilities consist of collaborating with various stakeholders across the company to utilize analytics to drive the business and better understand the customers needs. The primary goal is to facilitate making strong data-driven decisions across the company by clearly communicating insights to stakeholders that may not have a technical background. This can be accomplished by analyzing data that helps deepen the stakeholders quantitative comprehension of their business while concentrating on insights that expedite growth.

This project relates to the job description as it will allow stakeholders to make data-driven decisions within the best selling products at Skims. As the Data Analyst, I will analyze data to gain more insight on the customers needs while accelerating the growth of the business. I will be sharing these insights in layman's terms with various stakeholders which will allow them to better understand their business. 
***
### Data
https://skims.com/collections/best-sellers <br>
This data source was used to create all four tables in my database (inventory, category, ratings, reviews). I scraped the product name, price, category, average ratings, and reviews and consolidated it into a single database. <br>
Inventory Table: <br>	
  product_id INT NOT NULL AUTO_INCREMENT, <br>	
  name VARCHAR(255) NOT NULL, <br>	
	price VARCHAR(10) NOT NULL, <br>	
	PRIMARY KEY(product_id) <br>
Category Table: <br>
	product_id INT NOT NULL AUTO_INCREMENT, <br>	
	name VARCHAR(255) NOT NULL, <br>	
	category VARCHAR(50) NOT NULL, <br>	
	PRIMARY KEY(product_id) <br>
Ratings Table: <br>
 	product_id INT NOT NULL AUTO_INCREMENT, <br>	
	link VARCHAR(255) NOT NULL, <br>	
	rating FLOAT(50) NOT NULL, <br>	
	PRIMARY KEY(product_id) <br>
Reviews Table: <br>
	product_id INT NOT NULL AUTO_INCREMENT, <br>	
	reviews INT(50) NOT NULL, <br>	
	PRIMARY KEY(product_id) <br>
***
### Notebooks
https://github.com/kristihaha/Skims-Analytics/blob/main/data_collection.ipynb <br>
This notebook contains the data that I web scraped from skims.com best sellers page. I used this data to do sql queries to gain more insight on the best selling products/collections that are currently sold at Skims. <br>

https://github.com/kristihaha/Skims-Analytics/blob/main/sql_analysis.ipynb <br>
This notebook contains the SQL queries I ran to gain more insight on the best selling products at Skims. It includes five exploratory queries as well as three additional queries that tie into my primary question of: Which products/collections are the most popular within the Best Sellers page and why? <br>
***
### Future Improvements
With more time, I would have liked to scraped more relevant data to have more data to work with. The four tables that I have made are relatively simple and contain just enough measures to analyze the 52 products on the best sellers page. I would have liked to scrape all reviews for all products within the best sellers rather than just the total count of reviews. It would have been interesting to see exactly what customers like/dislike within each product. Looking further into key words could have been useful for stakeholders to understand what they should continue doing or stop doing for each product. For example, if customers consistently mention how the sizing is not true to size, Skims would know that they need to fix the sizing on the product to satisfy the customers. By only scraping the average rating, Skims is limited to truly understanding exactly what the ratings consist of.
