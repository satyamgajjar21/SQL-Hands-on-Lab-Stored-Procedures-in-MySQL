# Hands-on Lab: Stored Procedures in MySQL

This lab teaches you how to create, execute, and manage stored procedures in MySQL using the phpMyAdmin interface. Stored procedures allow you to encapsulate SQL statements into reusable routines that improve performance, enforce business logic, and simplify complex operations.

---

## Table of Contents

- [Overview](#overview)  
- [Objectives](#objectives)  
- [Software and Database](#software-and-database)  
- [Setup Instructions](#setup-instructions)  
- [Lab Exercises](#lab-exercises)  
  - [Exercise 1: Create and Execute a Retrieval Stored Procedure](#exercise-1-create-and-execute-a-retrieval-stored-procedure)  
  - [Exercise 2: Create and Execute an Update Stored Procedure](#exercise-2-create-and-execute-an-update-stored-procedure)  
- [Viewing and Dropping Procedures](#viewing-and-dropping-procedures)  
- [Conclusion](#conclusion)  
- [Authors](#authors)

---

## Overview

Stored Procedures in SQL are database objects that group multiple SQL statements into a single routine. They can accept input parameters, return output, and include control-flow logic such as conditional statements. This improves application performance, code reuse, and ensures consistent enforcement of business rules.

---

## Objectives

By completing this lab, you will be able to:

- Create stored procedures in MySQL  
- Execute stored procedures  
- Drop stored procedures when no longer needed  

---

## Software and Database

- **Software:** MySQL using phpMyAdmin interface  
- **Database:** `PETS` database containing a `PETSALE` table with sample data  

---

## Setup Instructions

1. Create the `PETS` database in phpMyAdmin.  
2. Download and run the `PETSALE-CREATE-v2.sql` script to create and populate the `PETSALE` table.  

---

## Lab Exercises

### Exercise 1: Create and Execute a Retrieval Stored Procedure

Create a stored procedure `RETRIEVE_ALL` to fetch all records from the `PETSALE` table:

```sql
DELIMITER //
CREATE PROCEDURE RETRIEVE_ALL()
BEGIN
  SELECT * FROM PETSALE;
END //
DELIMITER ;
