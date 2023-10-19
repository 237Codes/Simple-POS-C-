# Simple-POS-System
A simple Point-of-sale program for a cellphone kiosk to practice C++ programming. Here are the constraints of this project.


# Cell Phone Class #

The program creates a cell phone class. This class contains the following:
• A private string variable to hold the cellphone ID number
• A private string variable to hold the cellphone phone number
• A default constructor that sets both attributes to “none”
• A constructor that takes two string parameters (one for the ID, one for the phone number) and
sets the appropriate attribute to the appropriate value
• Get and Set functions for both attributes

# Customer Class #

The program creates a Customer class. This class contains the following:
• A private string variable to hold the customer’s name
• A private int variable to hold the number of phones purchased; the customer must purchase at
least one cellphone and cannot purchase more than 6 cellphones
• A private double variable to hold the cost of the purchase based on the following:
• Each cell phone cost $199.99 apiece
• There is a 6% sales tax that is added to the total purchase cost
• The total cost is the cost of all of the cell phones plus the sales tax
• An array of cell phone objects (up to a maximum of 6 phones)
• A default constructor that sets the name to “none”, the number purchased to 0, the total cost to
0.0 and the array to one single Cellphone object that uses the Cellphone default constructor
• A constructor that takes as parameters a string for the customer’s name, an int for the number of
cell phones purchased and an array of cell phone objects; the constructor sets the appropriate
attributes and calls a class function to calculate the total cost
• Get functions for all four private attributes
• Set functions for the name, number purchased, and an array of cell phone objects
• A class function to calculate the total cost of the purchase based on the number of cell phones
purchased

# Driver File #

The main function is to create a stack of cell phone objects to hold all the cell phones that are
available to be sold.

The main function is to create a deque of Customer objects to hold the customers who
purchased cellphones and have not been checked out.

The main function must call a function to read the data for the cellphone stack; this function
must:
• Send the stack to the function
• In the function, open a file called “cellphone.txt”; Windows users should place this file in the
c:\test folder and use a constant to define the location; Apple users should place this file where
appropriate and I will update the constant to make it Windows-compliant
• Read the data from the file creating a Cellphone object from the data; that object is added to the
stack; there are 22 cell phones in the data file
• After the code finished reading the file, the file must be closed
• The prototype for this function: void createStack(stack <Cell, vector<Cell>> &);
Once the stack is created, the main function must display a menu to the user

The main function must test that the user enters a valid menu choice; if they do not, the code
must display the appropriate error message and redisplay the menu.
If the user selects to buy a phone, the code calls a function to enter the information about the
customer
• The code must not allow the user to select this option if there are no cell phones in the stack
• The code must allow the user to enter a name and the number of cell phones to purchase
• The code must require the user to enter a number >= 1 for the number of cell phones
• The code must require the user to enter a maximum number of cell phones that can be
purchased; this number is either 6 OR the number of cellphones in the stack if that number is
less than 6.
• After the entry and validation of the information, the code must create a Customer object and add
The customer object to the queue
• The prototype for this function: void buyPhone(stack <Cell, vector<Cell>>&, deque<Customer>&);

. If the user selects to check out a customer, the code must call a function to print out the customer
receipt one customer at a time
• The function takes the Customer object from the front of the queue and displays the appropriate
values in the exact format of the screenshot below
• The function must display the receipts in the exact order that they were purchased

If there are no customers in the queue, the code must display the appropriate error message and
return the user to the main menu

If the user selects to quit
• The code must not allow the user to quit if there are still customers left in the queue that have not
yet been checked out.

If the customer queue is empty, the code displays a thank you message and ends.
