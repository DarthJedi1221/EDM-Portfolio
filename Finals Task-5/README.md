# Final Task - 5 Using SQL views and Stored Procedures and Stored Functions
## To have an idea of how SQL views work, kindly read the lecture on SQL views and stored procedures, then you may try the following examples in MySQL Workbench: 
## Start Xampp and MySQL Workbench – create or start a connection 
## Open the democodes.sql, and you may try executing all the examples using the hrd.sql file
## AFTER the practice codes…. Perform the required SQL statements of the ff: use inventory.sql for this.
##  Print screen the appropriate sql and output per item

### 1.	CREATE A VIEW that will display the vendors_code, vendors name, product description p_indate, of all products with p_indate from 2002 onwards
CREATE VIEW view_products_2002_onwards AS
SELECT v.v_code, v.v_name, p.p_descript, p.p_indate
FROM vendors v
JOIN products p ON v.v_code = p.v_code
WHERE YEAR(p.p_indate) >= 2002;
![image](https://github.com/user-attachments/assets/c22106b0-2639-49c7-aed1-7126d3fa677c)

### 2.	CREATE a VIEW that will display all products whose price range is between 100-150         
CREATE VIEW view_products_price_100_150 AS
SELECT *
FROM Products
WHERE p_price BETWEEN 100 AND 150;
SELECT * FROM view_products_price_100_150;
![image](https://github.com/user-attachments/assets/8ae386c2-df01-4a7c-b9f6-92ae03567d79)

### 3.	Create a VIEW that will COMPUTE for the (TOTAL_PRICE) of ALL PRODUCTS by getting the (P_ONHAND x P_PRICE) Sold by vendors with the following v_code (21344, 23119 and 24288)
CREATE VIEW view_total_price_by_vendor AS
SELECT v.v_code, v.v_name, p.p_descript, (p.p_onhand * p.p_price) AS total_price
FROM vendors v
JOIN Products p ON v.v_code = p.v_code
WHERE v.v_code IN (21344, 23119, 24288);
SELECT * FROM view_total_price_by_vendor;

![image](https://github.com/user-attachments/assets/d18b8e48-c23a-4956-ad03-9528910c971d)

### 4.	CREATE a STORED PROCEDURE that WILL take a SINGLE PARAMETER and UPDATED the Name of Vendor ‘Bryson,Inc.’ to ‘Bryson and Co’.
DELIMITER //

CREATE PROCEDURE update_vendor_name(IN old_name VARCHAR(50))
BEGIN
    UPDATE vendors
    SET v_name = 'Bryson and Co'
    WHERE v_name = old_name;
END //

DELIMITER ;
![image](https://github.com/user-attachments/assets/6f012b6e-406c-43c4-b38e-66e9c436e2ed)

### 5.	CREATE A Function that will take 2 parameters(v_code and v_state) and display All the product description and price based on the parameters passed to the function
DELIMITER //

CREATE FUNCTION get_products_by_vendor(vcode INT, vstate VARCHAR(3))
RETURNS TEXT
DETERMINISTIC
BEGIN
    DECLARE result TEXT;

    SELECT GROUP_CONCAT(CONCAT(p.p_descript, ' - ', p.p_price) SEPARATOR '; ')
    INTO result
    FROM Products p
    JOIN vendors v ON p.v_code = v.v_code
    WHERE v.v_code = vcode AND v.v_state = vstate;

    RETURN result;
END //

DELIMITER ;

SELECT get_products_by_vendor(21344, 'KY');

![image](https://github.com/user-attachments/assets/525c0464-0a82-4191-b84f-b1664e7e8762)

