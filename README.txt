===== README: ePortfolio =====

ePortfolio is a GUI program that helps an investor maintain a portfolio consisting of details about different stock and mutual fund investments.

The program stores investment properties such as symbol, name, the number of shares, price of the shares and their bookvalue. 

And then using GUI, it lets the user:
(1) buy a new investment or add more quantity to an existing investment.
(2) sell some investments by reducing some quantity from existing investment.
(3) update and refresh the prices of all the existing investments.
(4) calculate the total gain of their portfolio by accumulating all individual investments.
(5) search of investments that match the search query. 
(6) Quit

----- Compilation Instructions -----

(1) cd to the current folder.
(2) to compile the program: 
javac EPortfolio.java Investment.java MutualFund.java OPFrame.java PortfolioManager.java Stock.java
(3) to run the program: 
java EPortfolio.java Investment.java MutualFund.java OPFrame.java PortfolioManager.java Stock.java

----- Assumptions -----

> The program assumes that there are only 2 kinds of investments, Mutual Funds and Stocks.

> Every time we buy a stock, a commission of $9.99 is applied. 

> Every time we sell a stock, $9.99 is deducted. 

> There is no fee if we invest in mutual funds, but if we sell then, we need to pay a redemption fee of $45. 


----- Limitations -----

> We have to enter all data such as the current price ourselves which could result in errors. 

> We are not using actual stock market java API to get real-time data

> There are only two types of investments


----- User Guide -----

The program begins with a screen that welcomes us and has instructions on how to use the program. At the top, there is a "Commands Menu" that consists of the following options:

Buy Investments
Sell Investments
Update
Get Gain
Search
Quit

The user can then choose the option corresponding to the functionality that they want to perform. 

When the user chooses the Buy Investments option from the menu, the buy feature is implemented. 
The user can then choose from a dropdown menu to choose the investment type (Stock or Mutual Fund) and then enter the data of their investment one by one if the stock did not already exist. If it did, it changes the quantity of shares to buy more.

When the user chooses the Sell Investments option from the menu, the selling feature is invoked. 
It asks the user to enter the quantity and the price of shares the investor wants to sell and then checks if the particular symbol matches. If it does, it adjusts the quantity accordingly.

When the user chooses The Update option in the menu, they can update the prices of all the existing investments. 

By choosing the Get Gain option from the menu, the program shows the user the total gain over all their investments at the top and individual gains at the bottom. 

The search feature from the menu implements when the user inputs 5. It takes the parameters and tries to find the closest match that the investor is wishing for. 

And finally, we can quit the program by choosing the quit option on the commands menu.


----- Test Plan -----

1. The program expects the user to choose the "Buy Investment" command on the commands menu to buy shares.
2. After that, from the dropdown list, the user selects "Stock" to buy stocks.
3. The user then enters the Symbol, name, quantity and price of the stock in the empty fields below.
4. If the user enters some invalid input, such as by leaving a field blank, entering an integer value for quantity or entering text for price and quantity, on clicking the buy button on the right, the program displays the following message:
 Something Went Wrong, Please Try Again.
 Please make sure that
 1)You have not left any Field Blank
 2)You have entered an integer value only for Quantity.
 3)You have not entered any text in the Price and Quantity fields.
5. The user can then enter the data again and try again.
6. If the user has to change some data before buying, the user can then click on the reset button to clear all the fields.
7. If the correct data is entered, and the buy button is clicked, the program will display: "Added <quantity> gel stocks at <price> per stock. 

8. Alternatively, if the user selects "Mutual Fund" from the Type dropdown for Mutual funds, 
9. The program expects the user to enter the Symbol, name, quantity and price for the mutual fund.
10. If the user enters some invalid input, such as by leaving a field blank, entering an integer value for quantity or entering text for price and quantity, on clicking the buy button on the right, the program displays the following message:
 Something Went Wrong, Please Try Again.
 Please make sure that
 1)You have not left any Field Blank
 2)You have entered an integer value only for Quantity.
 3)You have not entered any text in the Price and Quantity fields.
11. The user can then try again with the correct values.
12. If the user has to change some data before buying, the user can then click on the reset button to clear all the fields.
13. If the correct data is entered, and the buy button is clicked, the program will display: "Added <quantity> Mutual Fund at <price> per unit.

14. The user selects the "Sell Investments" option from the commands menu to sell shares.
15. If the user enters a symbol for investment whose shares do not exist, the program displays the following message:
"Uh oh! There is no such investment in your Portfolio."
16. If the user inputs some invalid values, or does not enter values before clicking the buy button, the following message is displayed:
 Something Went Wrong, Please Try Again.
 Please make sure that
 1)You have not left any Field Blank
 2)You have entered an integer value only for Quantity.
 3)You have not entered any text in the Price and Quantity fields.
17. The user can then try again with the correct values.
18. If the user has to change some data before buying, the user can then click on the reset button to clear all the fields.
19. If the quantity of the stocks the user wants to sell is more than what they have, the program displays the following:
"You don't have enough Investments to sell in your Portfolio!"
 For example, if the user has 100 APPL shares and wants to sell 200 shares for APPL, the program informs the user.
20. If a matching symbol for stock or mutual fund is found, and all the inputs are valid, it gives a confirmation such as the follows:
"Successfully Sold the Investments!" and decreases the quantity of the shares

21. The user selects the "Update investments" option from the commands menu to update prices.
22. The program displays all the investments one by one and expects the user to enter a new price for the investment.
23. The user can navigate through the investments by using the prev and next buttons on the right-hand side and save the value for the current price. 
	For example, the user has the data stored for 3 investments, the program goes through all the three investments using the next and prev button and expects the user to enter and save the new value for price one by one.  

24. User selects the Get Gain option from the Commands menu to check gain.
25. If there is no gain, the program displays the message informing the user that there are no gains to display.
26. IF there is a net gain, the program shows the cumulative gain for all investments in the above panel and the individual gain for every investment in the individual gains panel. 
	For example, the user has 2 stocks and 2 mutual funds, the program shows the individual gain for each in the "Individual gains" area and the combined cumulative gain for it at the top. 

27. User selects the "search" option from the commands menu to use the search feature.
28. If there is some invalid input entered by the user, the program displays the following:
Something Went Wrong, Please Try Again.
 Please make sure that
 1)You have not left any Field Blank
 2)You have entered an integer value only for Quantity.
 3)You have not entered any text in the Price and Quantity fields.
29. If the inputs are all valid, the program gives the results accordingly.
	For example, the user enters Toronto, and the investments are namely "Bank of Toronto" "Toronto Bank" and "Apple"
	then the program shows "Bank of Toronto" and "Toronto Bank" and does not show "Apple" 

30. User selects the "Quit" option from the commands menu to quit the program.
31. The program exits.


----- Possible Improvements -----

> More investment categories 

> We could use actual stock market java API to get real-time data



