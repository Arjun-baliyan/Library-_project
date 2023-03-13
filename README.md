# Library-_project
I develop this library project in python with the help of OOPs -- Through this library project you can see the book collection , borrow a book , return book and donate a book to library
import datetime
class Library():
    def __init__(self):
        hour=int(datetime.datetime.now().hour)

        if hour>0 and hour<12:
                     print("Good morning .......")
        elif hour>=12 and hour<17:
                     print("Good afternoon.......")
        else:
                     print("Good evening..........")

    def Allbookcollection(self):
        print("This is the collection of all books")
        for item in allbookscollection:
            print("-"+ item)
    
    def Borrowbook(self):
        book=input("Please write the book name which you want to take : ")
        if book in allbookscollection:
            allbookscollection.remove(book)
            print(f" -- that book has been assigned to you , please return this book on time")
        else:
            print("Sorry this book is not in the collection , plase choose right book")
        

    def Returnbook(self):
        book=input("Please write the book name which you want to Return/Add : ")
        allbookscollection.append(book)
        print("Thank you so much for return/add book")

allbookscollection=["dark horse","the one thing"]
entry=Library()


while(True):
        welcomeMsg= '''                          -------welcome to the Delhi Library-------
             Please choose an option
               1. Our collection
               2. Request a book
               3. Return/Add a book
               4. Exit the library
        '''
        print(welcomeMsg)
        a=int(input("Enter a choice : "))
        if a==1:
            entry.Allbookcollection()
        elif a==2:
            entry.Borrowbook()
        elif a==3:
            entry.Returnbook()
        elif a==4:
            print("Thanks for using this library,  Please come again")
            exit()
        else:
            print("Invalid choice, Please choose again  ") 
