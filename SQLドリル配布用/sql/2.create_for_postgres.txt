
CREATE TABLE BelongTo (
       BelongID             INTEGER NOT NULL,
       StartDate            DATE,
       EndDate              DATE,
       DepartmentID         INTEGER,
       EmployeeID           INTEGER
);


ALTER TABLE BelongTo
       ADD PRIMARY KEY (BelongID);


CREATE TABLE Categories (
       CategoryID           INTEGER NOT NULL,
       CategoryName         VARCHAR(100)
);


ALTER TABLE Categories
       ADD PRIMARY KEY (CategoryID);


CREATE TABLE CustomerClasses (
       CustomerClassID      INTEGER NOT NULL,
       CustomerClassName    VARCHAR(100)
);


ALTER TABLE CustomerClasses
       ADD PRIMARY KEY (CustomerClassID);


CREATE TABLE Customers (
       CustomerID           INTEGER NOT NULL,
       CustomerCode         INTEGER,
       CustomerName         VARCHAR(100),
       Address              VARCHAR(100),
       CustomerClassID      INTEGER,
       PrefecturalID        INTEGER
);


ALTER TABLE Customers
       ADD PRIMARY KEY (CustomerID);


CREATE TABLE Departments (
       DepartmentID         INTEGER NOT NULL,
       DepartmentName       VARCHAR(100)
);


ALTER TABLE Departments
       ADD PRIMARY KEY (DepartmentID);


CREATE TABLE Employees (
       EmployeeID           INTEGER NOT NULL,
       EmployeeName         VARCHAR(100),
       Height               NUMERIC,
       EMail                VARCHAR(100),
       Weight               NUMERIC,
       HireFiscalYear       INTEGER,
       Birthday             DATE,
       BloodType            VARCHAR(2)
);


ALTER TABLE Employees
       ADD PRIMARY KEY (EmployeeID);


CREATE TABLE Prefecturals (
       PrefecturalID        INTEGER NOT NULL,
       PrefecturalName      VARCHAR(100)
);


ALTER TABLE Prefecturals
       ADD PRIMARY KEY (PrefecturalID);


CREATE TABLE Products (
       ProductID            INTEGER NOT NULL,
       ProductCode          INTEGER,
       ProductName          VARCHAR(100),
       Price                NUMERIC,
       CategoryID           INTEGER
);


ALTER TABLE Products
       ADD PRIMARY KEY (ProductID);


CREATE TABLE Salary (
       SalaryID             INTEGER NOT NULL,
       PayDate              DATE,
       Amount               NUMERIC,
       EmployeeID           INTEGER
);


ALTER TABLE Salary
       ADD PRIMARY KEY (SalaryID);


CREATE TABLE Sales (
       SaleID               INTEGER NOT NULL,
       Quantity             NUMERIC,
       CustomerID           INTEGER,
       ProductID            INTEGER,
       EmployeeID           INTEGER,
       SaleDate             DATE
);


ALTER TABLE Sales
       ADD PRIMARY KEY (SaleID);
