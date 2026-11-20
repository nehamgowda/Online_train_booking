# Online_train_booking

class Train:
    def __init__(self, number, name):
        self.number = number
        self.name = name

    def search_train(self):
        print("Searching train")

    def get_train_details(self):
        print(self.number, self.name)


class Reservation:
    def book_ticket(self):
        print("Ticket booked")

    def cancel_ticket(self):
        print("Ticket cancelled")

    def check_availability(self):
        print("Seat available")


class General:
    def __init__(self, number, price):
        self.number = number
        self.price = price


class Payment:
    def online_payment(self):
        print("Online payment successful")

    def cash_payment(self):
        print("Cash payment successful")

    def process_payment(self):
        print("Payment processed")


class Coach:
    def __init__(self, number, name):
        self.number = number
        self.name = name

    def get_coach_details(self):
        print(self.number, self.name)

    def check_seat_availability(self):
        print("Seat available")


class Ticket:
    def __init__(self, number, name, price):
        self.number = number
        self.name = name
        self.price = price

    def generate_ticket(self):
        print("Ticket generated")

    def get_ticket_details(self):
        print(self.number, self.name, self.price)

    def calculate_price(self):
        return self.price


class AC(Ticket):
    def book_ac_seat(self):
        print("AC seat booked")

    def calculate_fare(self):
        return self.price


class NON_AC(Ticket):
    def book_non_ac_seat(self):
        print("Non AC seat booked")

    def calculate_fare(self):
        return self.price


class Tatkal(Ticket):
    def book_tatkal_ticket(self):
        print("Tatkal ticket booked")

    def calculate_tatkal_fare(self):
        return self.price + 200


# Main program
t = Train(101, "Express")
t.search_train()
t.get_train_details()

r = Reservation()
r.book_ticket()
r.check_availability()

c = Coach(1, "A1")
c.get_coach_details()

ticket = AC(101, "AC Ticket", 1500)
ticket.generate_ticket()
print("AC Fare:", ticket.calculate_fare())

p = Payment()
p.online_payment()
p.process_payment()
