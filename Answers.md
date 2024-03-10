Q.1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.
Ans: The relationship between these two tables is one-to-many. A product can belong to one category (indicated by the foreign key category_id in the Product table), 
but a category can have many products (as a single category can be referenced by many rows in the Product table).  
This design allows for efficient storage of product data and simplifies queries to find all the products in a particular category.
The number 1 on the arrow next to "Product" indicates that a single product can only be linked to one category using the category_id foreign key.
Therefore, one product belongs to one category, but a category can have many products. This exemplifies a classic one-to-many relationship.

Q.2. How could you ensure that each product in the "Product" table has a valid category assigned to it?
Ans: there are a few ways to ensure that each product in the "Product" table has a valid category assigned to it:
1) Not Null Constraint: we can add a NOT NULL constraint on the category_id column in the "Product" table. This would prevent products from being inserted without a category assigned.
2) Foreign Key Constraint:  we can add a foreign key constraint on the category_id column in the "Product" table that references the id column in the "Product_Category" table. 
This would ensure that the category_id value in the "Product" table always refers to an existing category in the "Product_Category" table.
3) Default Category: we can set a default value for the category_id column in the "Product" table. This default value could be a category like "Uncategorized" or "Other". 
This way, even if a product is inserted without explicitly specifying a category, it would still have a valid category assigned.
