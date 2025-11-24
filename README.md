# MOVIE-TICKET-PRICE-CALCULATOR

def calculate_ticket_price():
    print("🎬 MOVIE TICKET PRICE CALCULATOR 🎟️")
    
    age = int(input("Enter your age: "))
    time = input("Show time (matinee/evening): ")
    seat = input("Seat type (normal/premium/recliner): ")
    discount = input("Student discount? (yes/no): ")

    # Base price based on age
    if age < 12:
        price = 150
    elif 12 <= age <= 60:
        price = 170
    else:
        price = 160

    # Time-based addition
    if time == "evening":
        price += 50

    # Seat-based addition
    if seat == "premium":
        price += 60
    elif seat == "recliner":
        price += 190

    # Discount
    if discount == "yes":
        price = 40

    print(f"\nYour final ticket price is: ₹{price}")
    print("Enjoy your movie! 🍿")


