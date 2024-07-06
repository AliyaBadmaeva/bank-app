## Development of an expert system with a graphical interface

This is a practical task on developing a GUI application.
A bank wants to implement a customer account management system that supports the following operations:

1. Replenishment of the client's account.

2. Withdrawal of money from the account.

3. Request for account balance.

4. Transfer money between client accounts.

5. Calculation of interest to all clients.

At the start of the program, it is considered that the bank has one client. The bank's client(s) are identified by names (a unique string containing no spaces). At the start of the program, we will set as the client’s name a name with a capital letter, in which a bank account with an arbitrary amount of money should be opened.
The program must be able to enter simple commands that support the following operations:

* **DEPOSIT name sum** If there is no client named name, a client is created with an empty account. In any case, the amount sum is credited to client name's account. The new account status of client name is displayed.
* **WITHDRAW name sum** If there is no client named name, a client is created with an empty account. In any case, the amount sum is withdrawn from client name's account. The new account status of client name is displayed.
* **BALANCE name** If name is given, the account status of this client is displayed. If there is no client named name, the text "NO CLIENT" is displayed. The command can be entered without a name. In this case, the status of the accounts of all clients in the database is displayed line by line.
* **TRANSFER name1 name2 sum** The amount is withdrawn from client name1 and credited to client name2. If one or both clients do not exist, they are created. The new account statuses of both clients are displayed.
* **INCOME p** Charge all clients who have open accounts p% of the invoice amount. Interest is accrued only to clients with a positive account balance. If the client has a negative balance, then his account does not change. After interest is accrued, the amount in the account remains whole, that is, only an integer number of monetary units is accrued. The fractional part of the total is discarded. The new account statuses of all clients are displayed.


Commands are loaded and executed through the program interface in two ways described below.

*The program interface contains:*
• large text field for entering commands;
• if the commands do not fit in the field, vertical scrolling is enabled;
• “Result” button;
• large text field for displaying results;
• if the results do not fit into the field, vertical scrolling is enabled;
• one-line file name entry field;
• "Download" button.

Required program functionality:
• commands are entered into the text field, one on each line;
• the number of commands is not limited; if the vertical field size is exceeded, text scrolling is enabled;
• when you click the “Result” button, the commands are executed sequentially.
• in the file input field, the user can specify the file name, after which the user clicks the “Download” button and the contents of the file are copied into the text input field. Commands are only copied, but are not executed until the user makes a calculation;
• if one of the commands is written incorrectly, then the execution of the commands stops, and an error report in the command operation is written in the output field in the form “ERROR: <command text>”.

*Example of command output:*

COMMAND
 <indent 4 spaces> RESULT
 >>>
 
For example, a possible result of entering BALANCE qq:

BALANCE qq
 NO CLIENT
>>>

Example for displaying account status:

DEPOSIT Ivanov 100
 Ivanov 70122003
>>>

Commands are entered by the user only in capital letters. The command itself, the client's name, and amounts (numbers) are separated by spaces.
