balance="10000"
count=0
ch=int(input("Enter your choice \n 1.Balance Check \n 2.Withdrawn \n 3.View History \n 4.Reser PIN \n 5.Credit amount"))
PIN="1234"

st=""

while(count<2):
    passw=input("Enter your PIN")
    if(passw==PIN):
        if(ch==1):
            print(balance)
        elif(ch==2):
            amount=(input("Enter amount do you want to withdraw"))
            balance=int(balance)-int(amount)
            temp=amount
            st=st+ amount +"Is Debited from your account \n"
            print("Your current balance is:  ",balance)
        elif(ch==3):
            print("Your history of transactions is : ", st)
        elif(ch==5):
            am=input("Enter amount you want to add to your account")
            temp=am
            balance=int(am)+int(balance)
            st=st+ am +"Is Credited to your account \n"
        elif(ch==4):
            print("Enter your last password")
            lastpass=input("Enter pass")
            if(lastpass==PIN):
                print("Enter new password")
                newpass=input("Enter new Password ")
                PIN=newpass
                print(PIN)
            else:
                print("You have enterd wrong last passwprd")
            
        else:
            print("Wrong choice...Try again")
    else:
        count=count+1
        print("Wrong PIN..Enter correct PIN")
        if(count<3):
            passw=input("Enter your PIN")
        else:
            print(" 3 unsuccessfull attempts ...Your account is blocked")
    print("DO you want to continue if yes then press y or n")
    c=input("Enter y or n")
    if(c=="y"):
        ch=int(input("Enter choice"))
    else:
        break