# Generation-of-arithmetic-and-geometric-progressions
def sequence_generator(first_value, n, func):
    
    current_value = first_value
    count = 0
    
    while count < n:
        yield current_value
        current_value = func(current_value)
        count += 1

def next_value_arithmetic(current):
    return current + 5

def next_value_geometric(current):
    return current * 3

print("Арифметична прогресія:")
for num in sequence_generator(2, 5, next_value_arithmetic):
    print(num)

print("\nГеометрична прогресія:")
for num in sequence_generator(2, 5, next_value_geometric):
    print(num)
