# Library Management System

## Topic: Library Management System  

This project is based on a Library Management System that tracks all information about books in the library, their cost, status, and the total number of books available.  

---

## Database Structure  

### **Database Name:**  
`library`  

### **Tables:**  
1. **Branch**  
2. **Employee**  
3. **Books**  
4. **Customer**  
5. **IssueStatus**  
6. **ReturnStatus**  

---

### **Attributes for the Tables:**  

#### **1. Branch**  
- `Branch_no` - Set as **PRIMARY KEY**  
- `Manager_Id`  
- `Branch_address`  
- `Contact_no`  

#### **2. Employee**  
- `Emp_Id` - Set as **PRIMARY KEY**  
- `Emp_name`  
- `Position`  
- `Salary`  
- `Branch_no` - Set as **FOREIGN KEY** and refers to `Branch_no` in the **Branch** table  

#### **3. Books**  
- `ISBN` - Set as **PRIMARY KEY**  
- `Book_title`  
- `Category`  
- `Rental_Price`  
- `Status` [Specify 'Yes' if the book is available and 'No' if not]  
- `Author`  
- `Publisher`  

#### **4. Customer**  
- `Customer_Id` - Set as **PRIMARY KEY**  
- `Customer_name`  
- `Customer_address`  
- `Reg_date`  

#### **5. IssueStatus**  
- `Issue_Id` - Set as **PRIMARY KEY**  
- `Issued_cust` - Set as **FOREIGN KEY** and refers to `Customer_Id` in the **Customer** table  
- `Issued_book_name`  
- `Issue_date`  
- `Isbn_book` - Set as **FOREIGN KEY** and refers to `ISBN` in the **Books** table  

#### **6. ReturnStatus**  
- `Return_Id` - Set as **PRIMARY KEY**  
- `Return_cust`  
- `Return_book_name`  
- `Return_date`  
- `Isbn_book2` - Set as **FOREIGN KEY** and refers to `ISBN` in the **Books** table  

---

### **Queries:**  

1. Retrieve the book title, category, and rental price of all available books.  

2. List the employee names and their respective salaries in descending order of salary.  

3. Retrieve the book titles and the corresponding customers who have issued those books.  

4. Display the total count of books in each category.  

5. Retrieve the employee names and their positions for the employees whose salaries are above Rs.50,000.  

6. List the customer names who registered before 2022-01-01 and have not issued any books yet.  

7. Display the branch numbers and the total count of employees in each branch.  

8. Display the names of customers who have issued books in the month of June 2023.  

9. Retrieve book titles from the Books table that belong to the "History" category.  

10. Retrieve the branch numbers along with the count of employees for branches having more than 5 employees.  

11. Retrieve the names of employees who manage branches and their respective branch addresses.  

12. Display the names of customers who have issued books with a rental price higher than Rs. 25.  
