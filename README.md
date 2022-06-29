# Monefy
This is the application under test. 
Monefy can help a user in tracking daily purchases, bills, and everything else you spend money on has never been so quick and enjoyable with this money manager.
Monefy is more than a money tracker, it's also one of the best savings apps to help you with money management. Keep track of your personal expenses and compare them to your monthly income with the budget planner.

# Framework Used
## Page Object Model and Page Factory using Appium.
Page Object Model, also known as POM, is a design pattern in Selenium that creates an object repository for storing all web elements.In Page Object Model, consider each web page of an application as a class file. Each class file will contain only corresponding web page elements. Using these elements, we can perform operations on the application under test.
* It is useful in reducing code duplication and improves test case maintenance.
* Helps with reusing code
* It eases readability and reliability of scripts: 

### Tools used.
* Appium Server
* Appium inspector

### Dependencies used in the framework
* Maven
* TestNG
* Selenium dependencies
* Appium client libraries
 
### Programming language used
* Java

### To test Project locally, 
* Clone repository at https://github.com/AKAlbert/Moneyfy_Automation
* Navigate to the pom.xml file and click build in your IDE to download the required dependencies.
* Navigate to src/test/java/config, update the config file with the details of your device i.e Device name, Android Version and Device Id.
* Run your Appium server
* Navigate to the testng.xml and run the tests locally.
* To check report, a test-output folder is created, open it and open index.html 

### Test ideas and Prioritization of test cases.
* Since the core business features are tracking income and expenses, these are the first areas to consider for out testing.
* Additionally, I have tested the filtering of information by date. Why? This is because in many cases, users would want to know their expenses or income on a certain date, so it would be important to automate this feature so as it can easily be tested.
* Lastly , I have automated the Account section. This is because a user would want to manage their finances from the account section since the Account is the home of the budgets and the user can view multiple expenses and incomes at a time.

### Test Case 1 - TestFilterDate
* Validate users can filter by date.
* Open the Monefy Application
* On the Home screen, tap open navigation in the left right corner
* Tap choose Date
* On the calendar screen, click the pencil icon to edit.
* Fill in the date (5/09/25)
* Click ok
* On the Home screen, verify that the date is equal to the set date.

### Test Case 2 - TestExpenses
* Validate Users can add expense
* Open Monefy Application
* On the Home screen, Tap the Add expense button
* Tap amount eg $5
* Tap choose category and select category.
* On the Home screen, verify that the balance is equal to the amount added.
#### Validate user can edit expense
- Open the Monefy Application
- On the home screen, click in the balance 
- On the transactions page, click an existing amount
- Clear field
- Input new Amount
- Navigate back to the Home screen and verify if the amount is now set to a new amount.
#### Validate users can delete expenses.
* Open the Monefy Application
* On the home screen, click in the balance 
* On the transactions page, click an existing amount.
* Click the delete button in the extreme top right corner.
* Validate that expense was deleted by checking the outstanding balance.

### Test Case 3 - TestIncome
* Validate Users can add income
* Open Monefy Application
* On the Home screen, Tap the Add income button
* Tap amount eg $5
* Tap choose category and select deposit category.
* On the Home screen, verify that the balance is equal to the amount added.

### Validate user can edit income
* Open the Monefy Application
* On the home screen, click in the balance 
* On the transactions page, click an existing amount
* Clear field
* Input new Amount
* Navigate back to the Home screen and verify if the amount is now set to a new amount.

### Validate users can delete income.
* Open the Monefy Application
* On the home screen, click in the balance 
* On the transactions page, click an existing amount.
* Click the delete button in the extreme top right corner.
* Validate that expense was deleted by checking the outstanding balance.

