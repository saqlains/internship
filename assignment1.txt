balance=10000.00
count=0
ch=int(input("Enter your choice"))
PIN="1234"

while(count<2):
    passw=input("Enter your PIN")
    if(passw==PIN):
        if(ch==1):
            print(balance)
        elif(ch==2):
            amount=float(input("Enter amount do you want to withdraw"))
            balance=balance-amount
            print("Your current balance is:  ",balance)
        else:
            print("Wrong choice...Try again")
    else:
        count=count+1
        print("Wrong PIN..Enter correct PIN")
        if(count<3):
            passw=input("Enter your PIN")
    print("DO you want to continue if yes then press y or n")
    c=input("Enter y or n")
    if(c=="y"):
        ch=int(input("Enter choice"))
    else:
        break