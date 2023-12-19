def is_prime(number):
    """Check if a number is prime."""
    if number < 2:
        return False
    for i in range(2, int(number**0.5) + 1):
        if number % i == 0:
            return False
    return True

def display_primes_in_range(start, end):
    """Display prime numbers in the specified range."""
    prime_numbers = [num for num in range(start, end + 1) if is_prime(num)]
    print(f"Prime numbers between {start} and {end}: {prime_numbers}")

# Set the range
start_range = 25
end_range = 50

# Display prime numbers in the specified range
display_primes_in_range(start_range, end_range)
