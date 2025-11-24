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
        price += 40

    # Seat-based addition
    if seat == "premium":
        price += 70
    elif seat == "recliner":
        price += 150

    # Discount
    if discount == "yes":
        price = 20

    print(f"\nYour final ticket price is: ₹{price}")
    print("Enjoy your movie! 🍿")

if __name__ == "__main__":
    calculate_ticket_price()
