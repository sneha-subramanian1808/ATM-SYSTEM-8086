# ATM System

## Introduction

This project is a successfully developed an ATM transaction system using emu 8086 microprocessor and our atm system is able to perform all the basic functionalities of an atm that are check balance, withdraw and deposit money as well as change pin after successful verification of the old pin.

This system eliminates the need for paperwork in maintenance. To begin, a cashier or clerk
might be hired to handle all transactions as well as update and preserve records. The new
approach allows the consumer to complete all transactions personally, while the automated
system updates and maintains the data automatically.

Advantages:

● Less work is required to execute the transaction.

● Less time is needed.

● There is no need to have a large number of documents on standby.

## Implementation
![image](https://user-images.githubusercontent.com/98036669/189942416-8e76891e-821f-4a29-a471-374727c76cb1.png)

A) Authentication
1. After asking the user for Account number and Pin we confirm the data
by checking for them in the data already available with us and display
the name of the user as well.
2. Only after successful authentication we allow the user to enter the menu
mode otherwise an error message is displayed.

B) Balance Enquiry
1. Having already Authenticated the user and displayed the user the menu
we ask for their choice in case they give it as one we display the
account’s balance that it mapped to that particular user and redisplay the
menu (INT 21H)

C) Withdraw Money
1. In case the user take the choice 2 we ask for the amount they wish to
withdraw using interrupts (INT 21H)
2. We then take that amount and check if the amount is greater than the
amount in the account of the user and if greater then we display an error
message
3. In case it is lower than the account’s balance then we deduct that
amount from the account and display the updated amount

D) Deposit Money
1. In case the choice is 3 we simply accept the amount to deposit by using
interrupts (INT 21H)
2. Then we simply add the amount to the account balance and display the
updated amount

E) Pin Updation
1. In case the choice is 4 we accept the current pin of the user to
reauthenticate and then only after verifying it we move on to ask the
new pin and ask the user to reconfirm the pin using interrupts(INT 21H)
2. After we find that the new pin and confirm pin is same we map the
updated pin to that particular user’s pin.
