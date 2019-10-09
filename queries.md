# Database Queries

### Display the ProductName and CategoryName for all products in the database. Shows 76 records.
```
SELECT ProductName, CategoryName from Products as P
JOIN Categories as C ON P.CategoryId = C.CategoryId;
```

### Display the OrderID and ShipperName for all orders placed before January 9, 1997. Shows 161 records.
```
SELECT OrderID, ShipperName from Orders as O
JOIN Shippers as S on O.ShipperId = S.ShipperId
;
```
### Display all ProductNames and Quantities placed on order 10251. Sort by ProductName. Shows 3 records.
```
SELECT ProductName, Quantity FROM OrderDetails
JOIN Products ON OrderDetails.ProductId = Products.ProductID
WHERE OrderId = 10251
ORDER BY ProductName
;
```
### Display the OrderID, CustomerName and the employee's LastName for every order. All columns should be labeled clearly. Displays 196 records.
```
SELECT OrderId, CustomerName, LastName as EmployeeLastName FROM Orders AS O
JOIN Customers AS C on O.CustomerID = C.CustomerID
JOIN Employees AS E on O.EmployeeId = E.EmployeeId;
```

### (Stretch)  Displays CategoryName and a new column called Count that shows how many products are in each category. Shows 9 records.

### (Stretch) Display OrderID and a  column called ItemCount that shows the total number of products placed on the order. Shows 196 records. 