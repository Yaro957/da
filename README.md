# Data Analyst Interview Preparation Guide

## 📋 Table of Contents
- [Personal Introduction](#personal-introduction)
- [Project Deep Dives](#project-deep-dives)
- [Behavioral Questions](#behavioral-questions)
- [Technical Questions](#technical-questions)
  - [Python](#python-basic-to-moderate)
  - [SQL](#sql-most-common-for-data-analyst)
  - [Power BI](#power-bi-concept--visualization)
  - [Excel](#excel-functional--practical)
  - [OOPs](#oops-object-oriented-programming)

---

## Personal Introduction

Hello, I'm **Om Jumde**, a final-year IT student from the Government College of Engineering.

During my final year, I worked on two projects in Power BI — an **Amazon Sales Dashboard** and a **Customer Churn Analysis**.

Throughout my academic journey, I've also explored areas like web development and cybersecurity. However, after completing these Power BI projects, I realized that my true interest lies in working with data — analyzing it, visualizing insights, and turning information into decisions.

Apart from academics, I've been the **Club Head of the Hackslash Coding Club**, where I mentored my juniors on their projects across different domains.

---

## Project Deep Dives

### 🛒 Amazon Sales Dashboard

One of my key projects involved building a comprehensive **Sales Performance Dashboard** for an e-commerce company that generated around **$1.57 million in revenue** across nearly **6,000 orders**.

**The Challenge:**  
Stakeholders lacked a clear, real-time view of regional performance, sales trends, and profitability, which slowed down their decision-making.

**My Approach:**

1. **Data Modeling:** Designed a **star schema data model** in SQL Server with dimension tables for products, customers, and regions, and a central fact table for sales transactions
2. **Integration:** Connected the optimized model to Power BI
3. **Advanced Analytics:** Created measures using DAX for profit margins, year-over-year growth, and regional comparisons
4. **Visualization:** Built an interactive dashboard with drill-down capabilities by region, product category, and time period

**Business Impact:**
- ✅ Reduced report refresh time by **40%**
- ✅ Improved data accuracy
- ✅ Enabled real-time decision-making
- ✅ Helped optimize regional sales strategies and focus on high-performing categories

---

### 🏦 Customer Churn Analysis

I worked on a **Bank Customer Churn Analysis** dashboard for a retail bank that wanted to understand why customers were leaving.

**The Challenge:**  
The bank had over **10,000 customer records**, but their existing reports didn't show clear churn patterns, making it difficult to design retention strategies.

**My Approach:**

1. **Data Integration:** Built a star schema data model in Power BI, integrating multiple sources including customer demographics, credit card usage, and activity data
2. **Analysis:** Used DAX and Power BI visuals to analyze monthly churn trends, region-wise performance, and credit card holder churn rates
3. **Interactivity:** Created a fully interactive dashboard enabling marketing and product teams to filter and explore customer segments dynamically

**Key Findings:**
- 🔍 Discovered a **429% spike in churn** following a policy change
- 💰 Projected that targeted retention strategies could recover approximately **$250,000 in annual revenue**

**Business Impact:**  
This project showcased my ability to connect data insights to business outcomes and emphasized the power of using BI tools for strategic decision-making.

---

## Behavioral Questions

### 💡 What motivated you to pursue data analytics?

Initially, I was more into development, but when I worked on my Power BI projects, I saw how data could tell powerful stories. Seeing business decisions change based on insights I built really motivated me. I realized analytics sits perfectly between **logic, technology, and business** — and that blend is what excites me most.

---

### 📊 What kind of datasets have you worked with in your projects?

I've worked with e-commerce sales data and bank customer data:

- **Amazon Sales Dashboard:** Handled data of over **6,000 orders** and **$1.57M in revenue**, cleaning and modeling it using SQL before connecting to Power BI
- **Customer Churn Project:** Worked with **10,000+ customer records**, combining demographics, credit usage, and activity data to find churn trends

---

### ⚙️ Which tool do you enjoy the most: Power BI, SQL, or Excel — and why?

I enjoy **Power BI** the most because it allows me to connect technical and business perspectives. I like how you can take cleaned data from SQL or Excel, use DAX for dynamic calculations, and visualize insights that directly help decision-makers. It's satisfying to see the complete story of data come alive visually.

---

### 🧠 How do you approach a new dataset when given for analysis?

My approach is structured:

1. **Understand the business problem** — what question we're trying to answer
2. **Explore the dataset** — look at column names, missing values, and data types
3. **Clean and model the data** using SQL or Power Query
4. **Analyze patterns** using summaries, visualizations, or measures
5. **Present insights clearly** — usually through dashboards or reports that answer the main question

---

### 🚧 What are some challenges you faced in your projects and how did you overcome them?

**Amazon Sales Dashboard:**  
The dataset was very messy with inconsistent region names and missing profit values. I overcame this by cleaning and standardizing data using Power Query and designing a star schema in SQL Server.

**Churn Project:**  
I struggled with performance issues when combining multiple tables, so I optimized the model and replaced calculated columns with DAX measures — which made the dashboard run faster.

---

### 💼 What kind of business impact did your dashboards bring?

**Amazon Sales Dashboard:**
- Identified high-performing product categories and regions
- Improved decision-making
- Reduced report generation time by **40%**

**Customer Churn Project:**
- Discovered a **429% spike in churn** after a policy change
- Projected recovery of **$250,000 in annual revenue** through targeted retention strategies

---

### 🚀 Where do you see yourself in the next 2 years in the data domain?

In the next two years, I see myself growing as a Data Analyst who's not just technically sound but also understands business needs deeply. I want to work on real-world datasets, build dashboards that drive decisions, and gradually move toward advanced analytics and predictive insights.

---

## Technical Questions

## 🐍 Python (Basic to Moderate)

### 1️⃣ What are Python variables? How do you declare them?

Variables in Python are containers used to store data values. You don't need to explicitly declare their data type — Python infers it automatically.

```python
name = "Om"
age = 22
```

Here, `name` is a string, and `age` is an integer.

---

### 2️⃣ Difference between mutable and immutable data types in Python?

**Mutable:** Can be changed after creation (like lists, dictionaries, sets)  
**Immutable:** Cannot be changed once created (like strings, tuples, integers)

```python
a = [1, 2, 3]  # mutable
b = (1, 2, 3)  # immutable
```

---

### 3️⃣ What are lists, tuples, and dictionaries?

- **List:** Ordered, mutable collection  
  Example: `[1, 2, 3]`

- **Tuple:** Ordered, immutable collection  
  Example: `(1, 2, 3)`

- **Dictionary:** Key-value pairs  
  Example: `{"name": "Om", "age": 22}`

---

### 4️⃣ How do you remove duplicates from a list?

Convert it to a set and back to a list:

```python
mylist = [1, 2, 2, 3]
unique_list = list(set(mylist))
```

---

### 5️⃣ Write or explain a pseudo code for a prime number check

```python
num = int(input("Enter number: "))
if num > 1:
    for i in range(2, int(num**0.5) + 1):
        if num % i == 0:
            print("Not Prime")
            break
    else:
        print("Prime")
else:
    print("Not Prime")
```

**Logic:** Loop from 2 to √n and check divisibility.

---

### 6️⃣ What are functions in Python? Give an example

Functions are reusable blocks of code that perform a specific task.

```python
def greet(name):
    return f"Hello, {name}"
```

---

### 7️⃣ What are modules and libraries?

- **Module:** A single Python file containing code (functions, classes)
- **Library:** A collection of related modules packaged together

For example, `math` is a module; `pandas` is a library.

---

### 8️⃣ What libraries are used for data analysis in Python?

Common ones are:

- **Pandas** for data manipulation
- **NumPy** for numerical operations
- **Matplotlib / Seaborn** for visualization
- **Scikit-learn** for machine learning

---

### 9️⃣ How do you handle missing values in a dataset?

Using Pandas:

```python
df.dropna()        # remove missing values
df.fillna(value)   # replace with mean/median or a constant
```

Choice depends on data and context.

---

### 🔟 What's the difference between `is` and `==` operators?

- `==` compares values
- `is` compares memory locations (object identity)

```python
a = [1,2]
b = [1,2]
a == b  # True
a is b  # False
```

---

## 🗄️ SQL (Most Common for Data Analyst)

### 1️⃣ What is SQL?

SQL stands for **Structured Query Language** — used to store, manipulate, and retrieve data from relational databases.

---

### 2️⃣ What are joins?

Joins combine rows from two or more tables based on a related column.

---

### 3️⃣ Explain INNER JOIN, LEFT JOIN, RIGHT JOIN, and FULL OUTER JOIN

- **INNER JOIN:** Returns only matching rows from both tables
- **LEFT JOIN:** All rows from the left table + matching from right
- **RIGHT JOIN:** All rows from right + matching from left
- **FULL OUTER JOIN:** Returns all records from both sides

```sql
SELECT a.name, b.order_id
FROM Customers a
LEFT JOIN Orders b
ON a.customer_id = b.customer_id;
```

---

### 4️⃣ Difference between WHERE and HAVING clauses?

- **WHERE** filters rows before aggregation
- **HAVING** filters after aggregation

```sql
SELECT city, COUNT(*) FROM customers
GROUP BY city
HAVING COUNT(*) > 5;
```

---

### 5️⃣ What is a primary key and a foreign key?

- **Primary key:** Unique identifier for each record in a table
- **Foreign key:** A reference to the primary key in another table

---

### 6️⃣ What is normalization? Why is it important?

Normalization is the process of organizing data to reduce redundancy and improve data integrity. It divides large tables into smaller, related ones.

---

### 7️⃣ Difference between COUNT(*), COUNT(column_name)?

- `COUNT(*)` counts all rows including NULLs
- `COUNT(column_name)` ignores NULLs

---

### 8️⃣ Write a query to get the second highest salary

```sql
SELECT MAX(salary)
FROM employees
WHERE salary < (SELECT MAX(salary) FROM employees);
```

---

### 9️⃣ Explain GROUP BY and ORDER BY clauses

- **GROUP BY** groups rows with the same values
- **ORDER BY** sorts results (ASC/DESC)

```sql
SELECT department, COUNT(*) 
FROM employees 
GROUP BY department 
ORDER BY COUNT(*) DESC;
```

---

### 🔟 Difference between DELETE, TRUNCATE, and DROP

- **DELETE:** Removes specific rows (can use WHERE)
- **TRUNCATE:** Removes all rows, keeps structure
- **DROP:** Deletes the entire table

---

### 1️⃣1️⃣ What are subqueries and when do you use them?

A subquery is a query inside another query, used to filter, compare, or aggregate data dynamically.

---

### 1️⃣2️⃣ How to find customers who never placed an order?

```sql
SELECT c.customer_id, c.name
FROM Customers c
LEFT JOIN Orders o
ON c.customer_id = o.customer_id
WHERE o.customer_id IS NULL;
```

---

## 📊 Power BI (Concept + Visualization)

### 1️⃣ What is Power BI?

Power BI is a business intelligence tool that helps visualize and analyze data using interactive dashboards.

---

### 2️⃣ Key components of Power BI

- **Power Query:** Data extraction and transformation
- **Power Pivot:** Data modeling
- **DAX:** Calculations and measures
- **Visualizations:** Charts, reports, dashboards

---

### 3️⃣ What types of graphs or charts have you used?

Bar, line, pie, map, tree map, and funnel charts.

For example, I used a line chart for monthly trends and bar charts for regional comparisons.

---

### 4️⃣ Difference between Power Query and Power Pivot

- **Power Query:** Used for data cleaning and transformation
- **Power Pivot:** Used for modeling and relationships

---

### 5️⃣ What is DAX? Examples

DAX (Data Analysis Expressions) is used to create calculated columns/measures.

```dax
Profit Margin = DIVIDE(SUM(Sales[Profit]), SUM(Sales[Revenue]))
```

---

### 6️⃣ What is a star schema?

A star schema has one fact table linked to multiple dimension tables. It's used for efficient querying and simpler data modeling.

---

### 7️⃣ How do you make dashboards interactive?

By adding slicers, filters, bookmarks, and drill-throughs so users can explore data dynamically.

---

### 8️⃣ What are measures and calculated columns?

- **Measure:** Calculated at query time (e.g., SUM, AVG)
- **Calculated column:** Stored with data; calculated row-wise

---

### 9️⃣ How to handle large datasets efficiently?

Filter at data source, use star schema, avoid complex visuals, and use measures instead of calculated columns.

---

### 🔟 How to publish and share dashboards?

After creating, publish via Power BI Service, then share links, workspaces, or embed in apps.

---

## 🧮 Excel (Functional + Practical)

### 1️⃣ How much do you know Excel?

I'd rate myself 8/10 — I've used Excel for cleaning, analyzing data, and building summary dashboards.

---

### 2️⃣ Common functions used for analysis

`SUMIF`, `COUNTIF`, `VLOOKUP`, `INDEX-MATCH`, `IFERROR`, `TEXT`, and logical functions like `IF` and `AND`.

---

### 3️⃣ What is a Pivot Table?

A Pivot Table helps summarize and analyze data quickly — grouping and aggregating large datasets without formulas.

---

### 4️⃣ What is conditional formatting?

It highlights cells based on rules — for example, marking sales below 5000 in red.

---

### 5️⃣ How to remove duplicates in Excel?

Go to **Data → Remove Duplicates**, or use formulas like `=UNIQUE(A2:A10)` in newer versions.

---

### 6️⃣ What is a dynamic chart?

A chart that updates automatically when data changes — usually built using named ranges or tables.

---

### 7️⃣ How to handle missing data?

Use filters to find blanks and either replace with average/median or mark as "Not Available."

---

### 8️⃣ Absolute vs Relative cell referencing

- **Absolute:** Fixed reference (`$A$1`)
- **Relative:** Changes when copied (`A1`)

---

### 9️⃣ Data validation in Excel

Used to restrict data entry — e.g., allowing only dates or numbers within a range.

---

### 🔟 Reports or dashboards built in Excel

I've built sales summaries using Pivot Tables, slicers, and conditional formatting before moving to Power BI.

---

## 🧩 OOPs (Object-Oriented Programming)

### 1️⃣ What is OOPs and why is it useful?

Object-Oriented Programming helps structure code using objects and classes, making it reusable, modular, and easier to maintain.

---

### 2️⃣ Four main pillars of OOPs

1. **Encapsulation**
2. **Inheritance**
3. **Polymorphism**
4. **Abstraction**

---

### 3️⃣ Explain inheritance with an example

It allows a class to inherit properties from another.

```python
class Animal:
    def sound(self): 
        print("Animal sound")

class Dog(Animal):
    def sound(self): 
        print("Bark")
```

---

### 4️⃣ What is encapsulation?

Encapsulation means wrapping data and methods together. It protects data from unauthorized access.

Example: Private variables in a class.

---

### 5️⃣ Abstract class vs Interface

- **Abstract class:** Can have both concrete and abstract methods
- **Interface:** Only defines method signatures (no implementation)

---

### 6️⃣ Method overloading vs Method overriding

- **Overloading:** Same method name, different parameters
- **Overriding:** Same method name in child class modifies parent behavior

---

### 7️⃣ What does the `self` keyword do in Python?

`self` refers to the current instance of the class and allows access to class variables.

---

### 8️⃣ Difference between a class and an object

- **Class:** Blueprint or template
- **Object:** Instance of that class

---

### 9️⃣ How is implementing different from inheriting?

- **Inheriting:** Reusing existing code (class-based)
- **Implementing:** Writing code to fulfill an interface or abstract definition

---

### 🔟 Real-life examples of OOP concepts

- **Encapsulation:** Bank account balance access
- **Inheritance:** Car inheriting from Vehicle
- **Polymorphism:** Same "start()" method for Bike, Car
- **Abstraction:** Using ATM — we don't see internal code, only operations

---

## 📝 Quick Tips for Interviews

✅ **Be specific** with numbers and impacts in your project stories  
✅ **Use the STAR method** (Situation, Task, Action, Result) for behavioral questions  
✅ **Practice SQL queries** on paper or whiteboard  
✅ **Prepare 2-3 questions** to ask the interviewer  
✅ **Stay calm** and think aloud when solving technical problems

---

**Good luck with your interviews! 🚀**
