# Instructions

<details>
  <summary>
    💡 REPL/PyCharm Guide
  </summary>

  - To toggle commenting, highlight the line(s) and press Ctrl + /
  - To move a statement or block of statements one indent to the right, highlight the statement(s)  press Tab
  - To move a statement or block of statements one indent to the left, highlight the statement(s)  press Shift+Tab
  - Avoid using backspaces or spaces to remove or place indents
  - REPL Comments
    - To ask the instructor a code question, highlight the line(s) of code and press Alt + / and type in your question/issue/comment and click on collapse
    - To view comments placed by the instructor click on the comment icon at the end of any highlighted code
    - If your issue is resolved, click on Resolve to remove the comment
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

## Start Working

<details>
  <summary>
    ✅ Create a new PyCharm project
  </summary>

- Create a new project in PyCharm and a folder of your choice
- Copy main.py from HW05
- Create a new folder called **cw06**
- Copy the code for the functions below from HW05 into the folder **cw06**
   - functions.py
   - list_functions.py
   - multilist_functions.py
   - validations.py
- Download the data files to the folder **cw06**
   - [products.txt](https://github.com/suchialex/CINS3002-CW06/blob/main/products.txt)
   - [products.csv](https://github.com/suchialex/CINS3002-CW06/blob/main/products.csv)
- Because of this new folder structure, you will have to change your import statements and file open functions with the correct file path
</details>


## In validations.py

<details>
  <summary>
    ✅ Modify validate_product_name()
  </summary>

  Parameters: This function doesn't accept any parameters  
  Return: It returns a string (the validated product name)  
  
  **Description:**  
  The purpose of this function is to ask the user to provide a product name and check if it is a valid name - which is, 
  - all alphabetical characters
  - special characters are allowed
  - no numbers allowed
  - cannot be all spaces
     
  If user enters a valid product name, we format it where the first character of each word is capitalized, and return this formatted valid name to the calling function  
  If the user enters an invalid name, we print `Invalid Product Name` entered, and ask user to provide product name again  
  The whole process is repeated until the user enters a valid product name

<details>
  <summary>🔑 Code Logic</summary>
  
  - Set a flag called valid to False
  - Start a while loop by checking if valid is False
  - Inside the while loop
    - Using an input statement to ask for employee first name, store it in a variable
    - Using the appropriate string methods, check if name is alphabetical with special characters
    - 💡 One way to do this is to use a for loop and count the number of digits (similar to validating employee last name)
    - 💡 Another way is to use any() function
      - If yes, set valid to True
      - If not, print `Invalid Product Name Entered`
  Outside the while loop, (the product name is valid, if you made it out of the while loop)
  - Format product name to where the first letter of each word is capitalized and the rest of them are lowercase
  - Return this formatted product name
</details>

</details>
  



## In main.py

<details>
  <summary>
    ✅ Test validate_product_name
  </summary>

  - Comment out any code inside main body
  - call validate_product_name and store in a variable (may have to import the appropriate module)
  - print this variable and test code

<details>
  <summary>📜 Testing</summary>

- If the user enters samsung2 the output must be Invalid Product Name Entered
- If the user enters Microsoft's Headset, it is valid input

</details>

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
  <summary>🔑 Code Logic</summary>
  
  - Set a flag called valid to False
  - Start a while loop by checking if valid is False
  - Inside the while loop
    - Using an input statement to ask for price, store it in a variable
  - Using the appropriate string methods, check if price is only numeric, may contain only `.` and no alphabetic characters
    - 💡 One way to do this is to replace the . with "" and then check if the resultant string is all numeric, if yes, valid is True else print `Invalid Price Entered`
    - 💡 Another way is to use a try block and convert the input to a float, if exception is raised, valid is False and print `Invalid Price Entered`, in else block valid is True
  - Outside the while loop, (the price is valid if you made it out of the while loop)
  - Return this valid price
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

<details>
  <summary>📜 Testing</summary>

- If the user enters ten thousand, the output must be Invalid Price Entered
- If the user enters $1000, the output must be Invalid Price Entered
- If the user enters 455 or 350.99, those are valid input

</details>

</details>

## In validations.py
<details>
  <summary>
    ✅ Define validate_quantity()
  </summary>

  - This function accepts no parameters and returns an integer
  - Get user input to get product quantity
  - Quantity must be all numeric (no decimal points allowed)
  - Quantity must be between 1 and 100
  - Quantity cannot be all spaces

<details>
  <summary>🔑 Code Logic</summary>

  - Set a flag called valid to False
  - Start a while loop by checking if valid is False
  - Inside the while loop
    - Using an input statement to ask for product quantity, store it in a variable
  - Using the appropriate string methods, check if quantity is
    - only numeric
    - between 0 and 100
    - and is not empty
    - 💡 One way to do this is test if the string has all numeric data (similar to validating employee salary)
  - If yes, set valid to True
  - If not, print Invalid Quantity Entered  
  Outside the while loop, return the quantity
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

<details>
  <summary>📜 Testing</summary>

- If the user enters apple, the output must be Invalid Quantity Entered
- If the user enters 30000 or 35.0, the output must be Invalid Quantity Entered
- If the user enters 66 , the output must be 66

</details>

</details>


<details>
  <summary>
    ✅ After testing validations
  </summary>

  - If all the validation functions execute correctly, **delete all the validate calls from main** and uncomment the call to product_operations
  - Make sure you are importing multilist_functions
  - In add_product() function, after call to validate_price(), add a function call to validate_quantity(), add this as a new element to the product list
  - Execute your code, add the following new product and test if it is added with quantity
    - product name: apple watch
    - product price: $355.89
    - product quantity: 15
  - Modify display_products() to add the quanity at the end, use formatting that best fits the data
</details>

## Bonus: 1pt

<details>
  <summary>
    ✅ Add functions/code to accommodate the new data field - quantity
  </summary>

  - Edit employees.txt to add quantity (choose your values) for each product after its price line
  - In main.py. import list_functions instead of multilist_functions
  - In add_product() function, after call to validate_price(), add a function call to validate_quantity(), add this as a new element to the products list
  - Execute your code, add the following new product and test if it is added with quantity
    - product name: apple watch
    - product price: $355.89
    - product quantity: 15
  - Modify display_products() to add the quanity at the end, use formatting that best fits the data
  - Add a new function update_price() and write code for it using other update functions' code logic
  - Add this to your printed menu options and add the appropriate elif block for update_price
</details>


## Copy code to replit

<details>
  <summary>
    ✅ Copy code to replit
  </summary>
  
  - Copy the contents of functions.py, list_functions.py, multilist_functions.py, validations.py, products.csv products.txt to replit under folder cw06
  - Comment out the existing import statement and code in main function body
  - Copy and paste the import statement and code from main.py in your PyCharm Project
  - Submit the URL on Canvas assignment
</details>



