# Coffee-machine
Coffee machine
from random import randint
MENU = {
    "espresso": {
        "ingredients": {
            "water": 50,
            "coffee": 18,
        },
        "cost": 1.5,
    },
    "latte": {
        "ingredients": {
            "water": 200,
            "milk": 150,
            "coffee": 24,
        },
        "cost": 2.5,
    },
    "cappuccino": {
        "ingredients": {
            "water": 250,
            "milk": 100,
            "coffee": 24,
        },
        "cost": 3.0,
    }
}

resources = {
    "water": 300,
    "milk": 200,
    "coffee": 100,
}
# TODO: 1. Ask user what type of coffee wants.
coffee = input("What would you like? (espresso/latte/cappuccino): ").lower()
#TODO: 2. turn off the machine by entering "OFF" to the prompt.
if coffee == "off":
    print("TURNED OFF")

# TODO: 3. Print report of all coffee machine resources
if coffee =="report":
    print(resources['water', 'milk', 'coffee'])

#TODO: 4. Check resources sufficient to make drink order.
def sufficient_amount_of_ingredients(coffee_type):
    if coffee =="coffee_type":
        if resources["water"] < MENU['coffee_type']['water']:
            print("Sorry there is not enough water.")
        elif resources['milk'] < MENU['coffee_type']['milk']:
            print("Sorry there is not enough milk.")
        elif resources['coffee'] < MENU['coffee_type']['coffee']:
            print("Sorry there is not enough coffee.")
sufficient_amount_of_ingredients(coffee)

def sufficient_amount_of_money(quarters, dimes, nickles, pennies):
    quarters*quarters_cost + dimes* dimes_cost + nickles* nickles_cost + pennies* pennies_cost

def check_transaction(total_amount):

print("Please insert coins.")
quarters_cost = 0.25
dimes_cost = 0.1
nickles_cost = 0.05
pennies_cost = 0.01
quarters = int(input("how many quarters?: "))
dimes = int(input("how many dimes?: "))
nickles = int(input("how many nickles?: "))
pennies = int(input("how many pennies?: "))
