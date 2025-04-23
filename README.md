# WEEK3
def calculate_discount(price, discount_percent):
    """
    Applies a discount if the discount percentage is 20% or higher.

    Args:
        price (float): The original price.
        discount_percent (float): The discount percentage.

    Returns:
        float: The final price after applying the discount.
    """
    if discount_percent >= 20:
        discount_amount = (discount_percent / 100) * price
        final_price = price - discount_amount
        return final_price
    else:
        return price

def main():
    while True:
        try:
            original_price = float(input("Enter the original price: "))
            discount_percentage = float(input("Enter the discount percentage: "))
            if original_price < 0 or discount_percentage < 0:
                print("Please enter non-negative values.")
                continue
            break
        except ValueError:
            print("Invalid input. Please enter a valid number.")

    final_price = calculate_discount(original_price, discount_percentage)

    if final_price == original_price:
        print(f"No discount applied. The price remains: {final_price:.2f}")
    else:
        print(f"The final price after discount is: {final_price:.2f}")

if __name__ == "_main_":
    main()
