# Email

email = input("Enter your email: ") #g@g.in
k = 0
j = 0
d = 0
if len(email) >= 6:
    if email[0].isalpha():
        if ("@" in email) and (email.count("@") == 1):
            if (email[-4] == ".") ^ (email[-3] == "."): # Put ^ operator
                for i in email:
                    if i == i.isspace():
                        k = 1
                    elif i.isalpha():
                        if i == i.upper():  # w-- W == w
                            j = 1
                    elif i.isdigit():
                        continue
                    elif i == "_" or i == "." or i == "@":
                        continue
                    else: 
                        d = 1

                if k == 1 or j == 1 or d == 1:
                    print("Wrong email! 5")
                else:
                    print("Right Email!")
            else:
                print("Wrong Email! 4")
        else:
            print("Wrong Email! 3")
            
    else:
        print("wrong Email! 2")
else:
    print("Please check the email! 1")
