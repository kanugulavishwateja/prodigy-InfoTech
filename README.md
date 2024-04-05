def celsius_to_fahrenheit(celsius):
    return (celsius * 9/5) + 32

def celsius_to_kelvin(celsius):
    return celsius + 273.15

def fahrenheit_to_celsius(fahrenheit):
    return (fahrenheit - 32) * 5/9

def fahrenheit_to_kelvin(fahrenheit):
    return (fahrenheit - 32) * 5/9 + 273.15

def kelvin_to_celsius(kelvin):
    return kelvin - 273.15

def kelvin_to_fahrenheit(kelvin):
    return (kelvin - 273.15) * 9/5 + 32

def convert_temperature(temp, unit):
    if unit.lower() == 'c':
        celsius = temp
        fahrenheit = celsius_to_fahrenheit(celsius)
        kelvin = celsius_to_kelvin(celsius)
    elif unit.lower() == 'f':
        fahrenheit = temp
        celsius = fahrenheit_to_celsius(fahrenheit)
        kelvin = fahrenheit_to_kelvin(fahrenheit)
    elif unit.lower() == 'k':
        kelvin = temp
        celsius = kelvin_to_celsius(kelvin)
        fahrenheit = kelvin_to_fahrenheit(kelvin)
    else:
        return "Invalid unit input. Please enter 'C', 'F', or 'K'."

    return f"{celsius:.2f}°C, {fahrenheit:.2f}°F, {kelvin:.2f}K"

temp_input = float(input("Enter the temperature value: "))
unit_input = input("Enter the unit of measurement (C for Celsius, F for Fahrenheit, K for Kelvin): ")

result = convert_temperature(temp_input, unit_input)
print("Converted temperatures:", result)
