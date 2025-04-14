# capstone-project-30
<sub>Level 1 Task 30</sub>

## Table of Contents

1. [Introduction](#intro)
2. [Project Description](#description)

   2.1. [How to run the program](#run)
  
3. [What I can do to improve the program](#changes)
4. [Conclusion](#conclusion)
5. [References](#references)

## 1. Introduction <a name = "intro"></a>
This was the final capstone for a previous task. The project is a shoe inventory system where users can track the number of shoes they own based on their location, code, product, price, and quantity. The inventory.py file was a template, and the inventory.txt file was provided for the assignment. 

The language used is Python.

## 2. Project Description <a name = "description"></a>
The assignment was based on a shoe inventory system for a Nike warehouse, to assist store managers with stock-taking. To optimise the delivery time, an inventory system needs to be implemented.
The warehouses store the following information:
* Country
* Code
* Cost
* Quantity
* Value

The program also allows store managers to search for the products by code, help them determine which product needs to be restocked by finding out the product with the lowest quantity, find the product with the highest amount, and calculate the total value of each item in stock.

### 2.1. How to run the program <a name = "run"></a>
When you run the program, the first thing you will see is the menu. See the image below.

![Screenshot of the menu](/images/menu.PNG)

#### Read data
First, you will need to read the data from the text file, inventory.txt. To do this, you need to enter _r_ to read the data. The data in the text file is stored in a list, making it easier to use the data. A message will be displayed if the data was captured.

![Screenshot of reading the data](/images/Read_data.PNG)

Once the data from the text file has been read, you can then decide to view the list, add a new shoe product, re-stock shoes, search for shoes, find the value per item, and find the highest quantity. If the user is done, they can exit the program.

####  Capture data
If the user wants to ship shoes to a country, they will need to enter _c_  in the menu, then input the following information: 
* The country the shoes will be shipped to
* The product code (SKU + 5 digits = 8 characters)
* The name of the product
* The cost of the product
* The quantity to be shipped (see image below).

![Screenshot of captured user data](/images/Capture_data.PNG)

#### View data 
To view the data, the user will need to enter _va_ in the menu. The data is printed in a list (see the image below):

![Screenshot of the list](/images/view_data.PNG)

This makes it easier for the user to see for users to see which shoes are being sold in what country, the cost of each shoe, and stock in the warehouse. 

#### Update data
If the user wishes to restock the shoes, the program will find and return the information of the country with the lowest stock. First, enter _rs_, the program will return the country with the lowest stock. The user will be prompted if they wish to restock the shoes. If yes is entered, the user will be required to enter the amount; this amount will be added to the current stock, and the information will be updated to the inventory.txt file. Otherwise, the user will be returned to the menu.

![Screenshot of restocking a shoe product](/images/restock_data.PNG)

#### Search data
You can search for the shoes using the product code. The code is eight characters long and consists of the following:
* The first three characters (SKU)
* The last five digits

If the code exists, the program will return the country, code, the name of the shoes, the price of the shoes, and the stock available in that country's warehouse (see the image below).

![Screenshot of searching for shoes](/images/search_daata.PNG)

#### Find value per item
To find the value of the shoes in each country, the program will calculate the value of the shoes by creating two lists, one with the quantity of the shoes and the other with their prices. The values from both lists will be multiplied together and appended to a new list. First, enter _vi_, the program will return a new list with the value per product in each country.

![Screenshot of value per item](/images/value_per_item_data.PNG)

#### Find the highest quantity
The program will return the country with the highest stock of Nike shoes. Enter _h_ in the menu. The program will print the number on the list, the country, product code, product name, the cost of the product, and the quantity they have in the warehouse.

![Screenshot of the highest stock](/images/highest_item_data.PNG)

## 3. How I can improve the program <a name = "changes"></a>
The program can be proven in the following areas:
* In the restock function, I can prevent the user from entering a value lower than the current stock.
* In the menu, in the capture shoe data option, I could have added more to the capture_shoes method. I should have asked the user to enter the last 5 characters of the code and added it to SKU.
* Adding a GUI using Tkinter or some other Python library.

## 4. Conclusion <a name = "conclusion"></a>
The program aims to make it more convenient and efficient for the shoe warehouse to monitor the stock of their products and to help them optimise delivery time to help stores restock.

## 5. References <a name = "references"></a>
* https://stackoverflow.com/questions/26051749/how-can-i-convert-the-index-of-a-string-to-an-integer-in-python 
* https://www.geeksforgeeks.org/python-converting-all-strings-in-list-to-integers/
* https://stackoverflow.com/questions/28618342/find-min-and-max-from-text-file-python
* https://stackoverflow.com/questions/45187646/python-how-to-write-to-specific-line-in-existing-txt-file
* https://www.geeksforgeeks.org/python-program-to-replace-specific-line-in-file/
