# Instructions

<details>
  <summary>
    💡 REPL Guide
  </summary>

  - To toggle commenting, highlight the line(s) and press Ctrl + /
  - To move a statement or block of statements one indent to the right, highlight the statement(s)  press Tab
  - To move a statement or block of statements one indent to the left, highlight the statement(s)  press Shift+Tab
  - Avoid using backspaces or spaces to remove or place indents
  - To ask the instructor a code question, highlight the line(s) of code and press Alt + / and type in your question/issue/comment and click on collapse
  - To view comments placed by the instructor click on the comment icon at the end of any highlighted code
  - If your issue is resolved, click on Resolve to remove the comment
</details>

<details>
  <summary>
     Assignment Instructions
  </summary>

  1. This is a part of the project to validate user input to manage product inventory - each product record has four data elements,
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
  
  - Copy the employees folder and all its contents from HW08, including the data files (Download the HW08 repl as a zipped folder and unzip and upload folder contents to this assignment)
  - To the folder products, copy all the code in functions.py, list_functions.py, multilist_functions.py, validations.py and the employee data files from
    - CW02 -or-
    - Exam 1 Prep - Product Inventory
    whichever has the complete working code
    - If neither works, copy the code from the solution I repl I posted

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
  If the user enters an invalid name, we print Invalid Product Name entered, and ask user to provide product name again.  
  The whole process is repeated until the user enters a valid product name

<details>
  <summary>Code Logic</summary>
  
  - Set a flag called valid to False
  - Start a while loop by checking if valid is False
  - Inside the while loop
    - Using an input statement to ask for employee first name, store it in a variable
    - Using the appropriate string methods, check if name is alphabetical with special characters
      - If yes, set valid to True
      - If not, print Invalid Product Name Entered
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

  - Comment out any code inside main
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
  - Using the appropriate string methods, check if price is only numeric, may contain only ., no alphabetic characters
  - If yes, set valid to True
  - If not, print Invalid Price Entered
  Outside the while loop, (the price is valid, if you made it out of the while loop)
  - Return this valid price
</details>
  
<details>
  <summary>💡 Testing</summary>

- If the user enters ten thousand, the output must be Invalid Price Entered
- If the user enters $1000, the output must be Invalid Price Entered
- If the user enters 350.99, it is a valid input

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
  - Quantity must be between 0 and 100
  - Quantity cannot be empty

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
  <summary>💡 Testing</summary>

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

## Finish Code Improvement

<details>
  <summary>
    ✅ In all functions files
  </summary>

  - In functions.py and validations.py, change filename to products1.txt (use the correct file path)
  - In list_functions.py change filename to products2.txt
  - In multilist_functions.py change filename to products3.txt
  - Test and make sure data is getting entered correctly into the respective files
</details>


<details>
  <summary>
    ✅ Improve Code
  </summary>

  - Remove any unnecessary print statements or modules
  - In functions.py, save the filename as a global constant and use that constant everywhere you are opening the file
  - Use context managers and exception handlers wherever applicable
  - If file is empty or not available, set default product ID to "3001"
</details>

## Bonus

<details>
  <summary>
    ✅ Bonus generate_email()
  </summary>

  - If you are done with all these, attempt the bonus for generate_email() in employees module (Check HW08 instructions)
</details>