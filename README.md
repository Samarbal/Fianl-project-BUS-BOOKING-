# Fianl-project-BUS-BOOKING-
print("""................BUS BOOKING ................
                                        (Please enter the choices in order)              """)
class Passenger ():
    def __init__(self ):
        self.Name = input(" Enter Your Full Name:" )
        self.ID = input(" Enter Your ID Number: ")
        self.Date = input(" Enter The Date You Want To Leave : ")


    def Trip (self):
        print("""" The station is in Gaza and it goes for 4 station 
                    1- Bus 1 from the station to Haifa
                    2- Bus 2 from the station to Jerusalem
                    3- Bus 3 from the station to Negev Desert
                    4- Bus 4 from the station to Hebron """)
        self.trip = int (input(" Enter the number the bus that you want to take :"))


        if self.trip ==1:
            self.distanation = " Haifa"
            print("  You have just booked a seat to Haifa")
        elif self.trip ==2:
            self.distanation = " Jerusalem "
            print (" You have just booked a seat to Jerusalem ")
        elif self.trip==3:
            self.distanation= " Negev Desert"
            print(" You have just booked a seat to Negev Desert")
        elif self.trip==4:
            self.distanation= " Hebron"
            print(" You have just booked a seat to Hebron")
        else:
            print(" Please enter a correct number ")
            return

#booking a seat
    def booking(self):
       print("[1]__[2]__[3]__[4]__[5]__[6]__[7]__[8]__[9]__[10]")
       seatlist =[1,2,3,4,5,6,7,8,9,10]


       self.bookinglist = [ ]

       while True:
           self.seatno = int(input("Choose a Seat Number & Max To Max You Can Book Two Ticket  :"))
           if 1 <= self.seatno <= 10:

               if self.seatno in seatlist:
                  self.bookinglist.append(self.seatno)
                  print("  You Have booked the seat number ",self.seatno )
                 # del seatlist[self.seatno + 1]

                  break

               else:
                   print("Ticket Allready Booked")
           else: break


choice = 0
def menu ():
    print(""""  .........................................
                           BUS BOOKING
                           1. Show the buses
                           2. Book a seat 
                           3. Exit """)
    global choice
    choice = int (input(" Enter your choice :"))

obj = Passenger()

while True:
    menu()
    if choice== 1:
      obj.Trip  ( )
    elif choice== 2:

      obj.booking()

    elif choice==3:
        print(" The passenger name is ",  obj.Name,
              " The number of the bus is", obj.trip,
              " And the seat number is ", obj.seatno)

        break
    else:
        print(" Invalid choice . Try again  ")




