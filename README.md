# Sql-Project

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
  product_id INT NOT NULL AUTO_INCREMENT,
  name VARCHAR(255) NOT NULL,
	price VARCHAR(10) NOT NULL,
	PRIMARY KEY(product_id) <br>
Category Table: <br>
	product_id INT NOT NULL AUTO_INCREMENT,
	name VARCHAR(255) NOT NULL,
	category VARCHAR(50) NOT NULL,
	PRIMARY KEY(product_id) <br>
Ratings Table: <br>
 	product_id INT NOT NULL AUTO_INCREMENT,
	link VARCHAR(255) NOT NULL,
	rating FLOAT(50) NOT NULL,
	PRIMARY KEY(product_id) <br>
Reviews Table: <br>
	product_id INT NOT NULL AUTO_INCREMENT,
	reviews INT(50) NOT NULL,
	PRIMARY KEY(product_id)
***
### Notebooks
***
### Future Improvements
