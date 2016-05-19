# database_model
#This is a report on possible queries that can be used to query the database model
CREATE TABLE Customers (
    customer_id INT AUTO_INCREMENT PRIMARY KEY,
    customer_name VARCHAR(100)
);
#############################################
CREATE TABLE Orders (
    order_id INT AUTO_INCREMENT PRIMARY KEY,
    customer_id INT,
    amount DOUBLE,
    FOREIGN KEY (customer_id) REFERENCES Customers(customer_id)
);
###########################################################
INSERT INTO `Customers` (`customer_id`, `customer_name`) VALUES
(1, 'Adam'),
(2, 'Andy'),
(3, 'Joe'),
(4, 'Sandy');
###############################################################
SELECT * FROM Orders JOIN Customers USING(customer_id)

#############################################################
DELETE FROM `customer` WHERE `customer_name`="Adam";
