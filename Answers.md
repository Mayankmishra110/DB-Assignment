# DB-Assignment

# 1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.

# Ans-: 1. In the provided schema of Product, product_category, the "Product" table has a column named category_id, which serves as the foreign key. This foreign key establishes the connection between the "Product" table and the "Product_Category" table.


# Product Table:

** id: Primary key for the "Product" table. **
name: Name of the product. <br>
desc: Description of the product. <br>
SKU: Stock Keeping Unit, a unique identifier for the product. <br>
category_id: Foreign key referencing the primary key id in the "Product_Category" table. <br>
inventory_id: Foreign key referencing the primary key id in the "Product_Inventory" table. <br>
price: The price of the product.<br>
discount_id: Foreign key referencing the primary key id in the "Discount" table. <br> 
created_at: Time indicating when the record was created. <br>
modified_at: Time indicating when the record was last modified. <br>
deleted_at: Time indicating when the record was deleted. <br>

<br>
  Product_Category Table:
 <br>
** id: Primary key for the "Product_Category" table. **

name: Name of the product category. <br>
desc: Description of the product category. <br>
created_at: Times indicating when the record was created. <br>
modified_at: Times indicating when the record was last modified. <br>
deleted_at: Times indicating when the record was soft-deleted. <br>

The foreign key relationship is established through the category_id column in the "Product" table, which references the primary key id in the "Product_Category" table. This means that each entry in the "Product" table is associated with a specific category in the "Product_Category" table. It enables the retrieval of detailed information about the category to which a product belongs, facilitating organized and efficient data management.

<br>

# 2. How could you ensure that each product in the "Product" table has a valid category assigned to it?:
<br>
# Ans-: For making sure in every product in the "Product" table belongs to the right category, we use foreign key. This rule says that category listed in the "Product" table must match a valid category in the "Product_Category" table. It's like having a buddy system to check that each product has a real category friend, avoiding confusion and keeping our data organized.
<br>
1. **Connection with "Product_Category":**
   - Every product in the "Product" table is linked to a category through a special link called `category_id`.
  <br>
2. **Making Sure the Category is Real:**
   - We set up a rule (think of it as a guard) that checks if the category mentioned in `category_id` really exists in the "Product_Category" table.
<br>
3. **No Fake Categories Allowed:**
   - This guard makes sure we don't accidentally assign a product to a category that doesn't actually exist. It's like having a buddy system to confirm everyone's identity.
<br>
4. **Keeping Things Tidy:**
   - This guard also prevents situations where a product is left "orphaned" without a real category. It's like making sure everyone has a dance partner at a party.
<br>
5. **Avoiding Mix-ups:**
   - Overall, this helps keep our data neat and tidy. Each product knows exactly which category it belongs to, and we can trust that the information is accurate.

<br>

