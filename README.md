# Auction-server
***************************************************************************
		

## Project - AUCTION SERVER

               
***************************************************************************
*

# Contains: 10 .java files, 1 .csv file and README.md file

# Instruction for run the programe,
	I.) Get a terminal or cmd from current derectory

    II.) Run the Server (to compile and run Server.java file like belowe)
    		javac Server.java
    		java Server

    III.) Get another terminal or cmd

    IV.) Run the client (to compile and run ClientApp.java file like belowe)
    		javac ClientApp.java
    		java ClientApp

# How nc works?
When testing on nc, user should provide valid name 1st. If that name is inuse server sends -2. After sending name user should
send valid item else server sends -1.	Then server provide item current bid value and then user can bid. Server updates the
value when a new valid bid happens and it sends the new value to user as well.

A client cant change his name/item and 2 clients cant have the same name. Also after client loggedout, he needs a different name to
log in again.

# How Client GUI works?
	I.) Click "Connect to Server" button to connect to the Server
	II.) The give your user name in Name text field and hit confirm button
	III.)Give sycurity symbol that you want to bid
	IV.) Click "Start Bids" button to bid
	V.)Then give your bid value in "Bid amount" button and hit Bid button to submit

# What are the server GUI's features?
	I.) Can see the changes made in stock items in a log table given in right side in the display
	II.) There is a pannel on left side to monitor the favourite 8 stock items
	III.) The button "Stocks Items List" will give you all the stock items given in stocks.csv file


# Objective: 
You will design a software system using the following concepts:

∙ Threads,

∙ Synchronization primitives,

∙ Sockets,

∙ Objects, classes, and

∙ Collections


Description: for this project you will implement a server which can be used by clients to bid for items in a stock exchange. Specification for each component in of the software is given below.

Item:

∙ Each item has, among other things a Symbol, Security Name, and a Price. This data is given in a CSV file; Comma Separated Value, file; of cause the once the system starts to run the price of the item will vary and what is given in the CSV is the initial price. (see stocks.csv)

∙ Read the CSV file and store the information about the items in a suitable data structure (i.e. suitable collection). Before selecting the data structure read how the data items will be accessed.

Server side: the server should be able to handle more than one connection at a time. It should display the current price of stocks via a GUI. You may assume that stock prices do not change in 500ms.

∙ Server will be listing to incoming connections on port 2000. It should be able to handle more than one connection at a time. Therefore should use threads for handling the connections.

∙ You should be able to connect to the server using a common communication tool such as nc or telnet.

∙ Once a client is connected the should except the first message to be the name of the client. For now we will not authenticate the client but use this as the name for all the bids. Once the name is given the client is expected to provide the Symbol of the security he/she is willing to bid on. If the provided Symbol is found the server should reply back with the current cost of the security or -1 to indicate that the Symbol is invalid.

∙ Once that is done the clients are not allowed to change neither their names (obviously) nor the security that they are bidding on.

∙ Server should be able to locate a given stock item, update its price. Furthermore it should be able to track all the changes done to the stock item; how the offers varied with time and who made the offers.

∙ Server should be able to list the stock items (Symbol, name) together with the current price in an GUI. The GUI should display the price of following Symbols: FB, VRTU, MSFT, GOOGL, YHOO, XLNX, TSLA and TXN.

∙ For the display, you may assume that updates do not happen in 500ms.
