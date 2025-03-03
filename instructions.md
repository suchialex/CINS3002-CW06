# Instructions

<details>
  <summary>
    💡 Code Guide
  </summary>

  - To toggle commenting, highlight the line(s) and press Ctrl + /
  - To move a statement or block of statements one indent to the right, select the statement(s)  press Tab
  - To move a statement or block of statements one indent to the left, select the statement(s)  press Shift+Tab
  - Avoid using backspaces or spaces to remove or place indents
</details>

<details>
  <summary>
     Assignment Instructions
  </summary>

  1. This is a part of the project to validate user input to manage product inventory - each product record has four comma separated data elements,
     - Product ID
     - Product Name
     - Product Price
     - Product Quantity 
  2. These validations will be coded in validations.py
</details>   

# Start Working

<details>
  <summary>
    ✅ Copy Code
  </summary>
  
  - Create a new project in PyCharm in a folder of your choice
  - Create a new folder called **cw06**
  - To the folder cw06, copy all the code in functions.py, list_functions.py, multilist_functions.py, validations.py files from cw05
  - Download products.csv https://github.com/suchialex/CINS3002-CW06/blob/main/products.csv
  - Download products.txt https://github.com/suchialex/CINS3002-CW06/blob/main/products.txt

</details>


  
## In validations.py

<details>
  <summary>
    ✅ Modify validate_product_name()
  </summary>

  Parameters: This function doesn't accept any parameters  
  Return: It returns a string (the validated product name)  
  
  Description:  
  The purpose of this function is to ask the user to provide a product name and check if it is a valid name - which is, 
  - all alphabetical characters
  - special characters are allowed
  - no numbers allowed
  - cannot be all spaces
     
  If user enters a valid product name, we format it where the first character of each word is capitalized, and return this formatted valid name to the calling function.  
  If the user enters an invalid name, we print `Invalid Product Name` entered, and ask user to provide product name again.  
  The whole process is repeated until the user enters a valid product name

<details>
  <summary>Code Logic</summary>
  
  - Set a flag called valid to False
  - Start a while loop by checking if valid is False
  - Inside the while loop
    - Using an input statement to ask for employee first name, store it in a variable
    - Using the appropriate string methods, check if name is alphabetical with special characters
      - If yes, set valid to True
      - If not, print `Invalid Product Name` Entered
  Outside the while loop, (the product name is valid, if you made it out of the while loop)
  - Format product name to where the first letter of each word is capitalized and the rest of them are lowercase
  - Return this formatted product name<br>
</details>
  
</details>


## In main.py

<details>
  <summary>
    ✅ Test validate_product_name
  </summary>

  - Comment out any code inside main body
  - call validate_product_name and store in a variable (may have to import the module)
  - print this variable and test code
</details>


## In validations.py

<details>
  <summary>✅ Modify validate_price</summary>

- Price
  - must be numeric
  - cannot be special characters other than .
  - cannot have any alphabetic characters
- Keep asking the user to provide price, until a valid price is provided
- Return valid price

<details>
  <summary>Code Logic</summary>
  
  - Set a flag called valid to False
  - Start a while loop by checking if valid is False
  - Inside the while loop
    - Using an input statement to ask for price, store it in a variable
  - Using the appropriate string methods, check if price is only numeric, may contain only `.` and no alphabetic characters
  - If yes, set valid to True
  - If not, print Invalid Price Entered
  Outside the while loop, (the price is valid, if you made it out of the while loop)
  - Return this valid price
</details>
  
<details>
  <summary>📜 Testing</summary>

- If the user enters ten thousand, the output must be Invalid Price Entered
- If the user enters $1000, the output must be Invalid Price Entered
- If the user enters 455 or 350.99, those are valid input

</details>
</details> 

## In main.py
<details>
  <summary>
    ✅ Test validate_price
  </summary>
  
  - You may comment out other validate functions if they are working correctly
  - call validate_price store in a variable
  - print the above variable and test code with the test cases provided
</details>

## In validations.py
<details>
  <summary>
    ✅ Modify validate_quantity
  </summary>

  - Quantity must be all numeric (no decimal points allowed)
  - Quantity must be between 1 and 100
  - Quantity cannot be all spaces

<details>
  <summary>Code Logic</summary>

  - Set a flag called valid to False
  - Start a while loop by checking if valid is False
  - Inside the while loop
    - Using an input statement to ask for product qty, store it in a variable
  - Using the appropriate string methods, check if quantity is
    - only numeric
    - between 0 and 100
    - and is not empty
  - If yes, set valid to True
  - If not, print Invalid Quantity Entered  
  Outside the while loop, return the quantity
</details>

<details>
  <summary>📜 Testing</summary>

- If the user enters apple, the output must be Invalid Quantity Entered
- If the user enters 30000 or 35.0, the output must be Invalid Quantity Entered
- If the user enters 66 , the output must be 66

</details>

</details>

## In main.py

<details>
  <summary>
    ✅ Test validate_quantity
  </summary>

  - You may comment out other validate functions if they are working correctly
  - call validate_quantity 
  - print the above variable and see if it is working correctly
</details>


