# Technical Interview Tools and Practice

Want to follow along with a slideshow with resources and answers?
[Click here!](https://www.canva.com/design/DAGeFVRbN9E/v7O8CbuiaVfp0gB_H42L6g/edit?utm_content=DAGeFVRbN9E&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)

## Practice Questions

You can check your code by clicking on the slideshow above ^ or navigating to the Solutions markdown file in this folder.

### SQL
Use the data in the SQL_data folder to complete the following. (Or look at bottom of this page to copy code that manually creates the data)

#### Exercise 1: Find the average age of customers who made a purchase in the last month, grouped by product category.

![image](https://github.com/user-attachments/assets/69d006bc-255e-41b3-a28f-075d5f7b5600)


#### Exercise 2: Identify the top 5 most purchased products in the last 30 days and see how many times each product was purchased.

![image](https://github.com/user-attachments/assets/ffb4ec01-aef8-4974-9b30-9162fe9a93f9)

### Data Manipulation

Choose R or Python to complete the following using the data in the Data_Manipulation_data folder.

#### Exercise 1: Given a dataset of user reviews, clean and preprocess the data by removing duplicates, handling missing values, and normalizing text data.

![image](https://github.com/user-attachments/assets/5b4bcaa7-8688-4d74-9086-745aa5076651)

#### Exercise 2: Write a function to handle outliers in a dataset, using either IQR or Z-scores.

![image](https://github.com/user-attachments/assets/96f759a7-ede3-4872-89df-24a4bc985934)

### Programming

Though Python is most commonly used in the Data Science field, feel free to practice with whatever language you are most comfortable with as the problem solving skills are usually more important.

#### Exercise 1: Find the intersection of two sorted arrays (arr1 and arr2).
```python
arr1 = [1, 2, 4, 5, 6]
arr2 = [2, 5, 6, 7, 8]
result = intersection(arr1, arr2)
print(f"Intersection of arrays: {result}")
```
Intersection of arrays: [2, 5, 6]


#### Exercise 2: Given a list of integers (nums), write a function (max_sum) to return the maximum sum of non-adjacent numbers.
```python
nums = [3, 2, 5, 10, 7]
result = max_sum(nums)
print(f"Maximum sum of non-adjacent numbers: {result}")
```
Maximum sum of non-adjacent numbers: 15


### Manually Create Data for SQL Exercises

```sql
CREATE TABLE 'purchases' (purchase_id TEXT,customer_id TEXT,product_id TEXT,purchase_date TEXT,amount TEXT);
INSERT INTO 'purchases' ('purchase_id','customer_id','product_id','purchase_date','amount') VALUES 
 ('1','1','101','2025-01-15','249.99'), 
 ('2','2','106','2025-01-20','89.99'), 
 ('3','3','103','2025-01-18','19.99'), 
 ('4','4','104','2025-01-22','399.99'), 
 ('5','5','105','2025-01-25','599.99'), 
 ('6','6','102','2025-01-17','49.99'), 
 ('7','7','108','2025-01-19','249.99'), 
 ('8','8','107','2025-01-23','29.99'), 
 ('9','9','110','2025-01-24','79.99'), 
 ('10','10','109','2025-01-26','299.99');
 
CREATE TABLE 'products' (product_id TEXT,category TEXT);
INSERT INTO 'products' ('product_id','category') VALUES 
 ('101','Electronics'), 
 ('102','Clothing'), 
 ('103','Books'), 
 ('104','Electronics'), 
 ('105','Furniture'), 
 ('106','Clothing'), 
 ('107','Books'), 
 ('108','Electronics'), 
 ('109','Furniture'), 
 ('110','Clothing');
 
CREATE TABLE 'customers' (customer_id TEXT,age TEXT,name TEXT,city TEXT);
INSERT INTO 'customers' ('customer_id','age','name','city') VALUES  
 ('1','34','Alice Johnson','New York'), 
 ('2','25','Bob Smith','Los Angeles'), 
 ('3','42','Charlie Brown','Chicago'), 
 ('4','28','Daisy Lee','Miami'), 
 ('5','37','Edward Davis','San Francisco'), 
 ('6','50','Fiona Carter','Seattle'), 
 ('7','22','Greg Wilson','Boston'), 
 ('8','33','Hannah Miller','Austin'), 
 ('9','29','Ian Clark','Denver'), 
 ('10','41','Jessica Taylor','Atlanta');
```
