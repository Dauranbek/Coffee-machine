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
# coffee = input("What would you like? (espresso/latte/cappuccino): ").lower()
#TODO: 2. turn off the machine by entering "OFF" to the prompt.
# if coffee == "off":
#     print("TURNED OFF")

# TODO: 3. Print report of all coffee machine resources
# if coffee =="report":
#     print(resources['water', 'milk', 'coffee'])

#TODO: 4. Check resources sufficient to make drink order.
def sufficient_amount_of_ingredients(coffee_type):
    if coffee =="coffee_type":
        if resources["water"] < MENU['coffee_type']['water']:
            print("Sorry there is not enough water.")
        elif resources['milk'] < MENU['coffee_type']['milk']:
            print("Sorry there is not enough milk.")
        elif resources['coffee'] < MENU['coffee_type']['coffee']:
            print("Sorry there is not enough coffee.")
# sufficient_amount_of_ingredients(coffee)




def check_transaction():
    if coffee =='espresso' and formula <         int(MENU["espresso"]["cost"]):
        print("Sorry that is not enough money. Money refunded.")
    else:
        if coffee == 'espresso':
            print("Here is your espresso. Enjoy!")
    if coffee == 'cappucino' and formula < int(MENU["cappuccino"]["cost"]):
        print("Sorry that is not enough money. Money refunded.")
    else:
        if coffee == 'cappucino':
            print("Here is your cappucino. Enjoy!")
    if coffee == 'latte' and formula < int(MENU["latte"]["cost"]):
        print("Sorry that is not enough money. Money refunded.")
    else:
        if coffee == 'latte':
            print("Here is your latte. Enjoy!")


def change():
    if formula > int(MENU["espresso"]["cost"]):
        change_amount = formula - int(MENU["espresso"]["cost"])
        print(f"Here is ${round(change_amount, 2)} in change")
    elif formula > int(MENU["cappuccino"]["cost"]):
        change_amount = formula - int(MENU["cappuccino"]["cost"])
        print(f"Here is ${round(change_amount, 2)} in change")
    elif formula > int(MENU["latte"]["cost"]):
        change_amount = formula - int(MENU["latte"]["cost"])
        print(f"Here is ${round(change_amount, 2)} in change")
# print("Please insert coins.")
quarters_cost = 0.25
dimes_cost = 0.1
nickles_cost = 0.05
pennies_cost = 0.01
# quarters = int(input("how many quarters?: "))
# dimes = int(input("how many dimes?: "))
# nickles = int(input("how many nickles?: "))
# pennies = int(input("how many pennies?: "))
# formula = quarters*quarters_cost + dimes* dimes_cost + nickles* nickles_cost + pennies* pennies_cost
# resources['Money'] = {}
# resources['Money'] = round(formula, 2)
# change()
# check_transaction()
off = False
while off == False:
  coffee = input("What would you like? (espresso/latte/cappuccino): ").lower() 
  if coffee == "report":
    print(resources)
  elif coffee == "off":
    off = True
  else:
    sufficient_amount_of_ingredients(coffee)
    print("Please insert coins.")
    quarters = int(input("how many quarters?: "))
    dimes = int(input("how many dimes?: "))
    nickles = int(input("how many nickles?: "))
    pennies = int(input("how many pennies?: "))
    formula = quarters * quarters_cost + dimes * dimes_cost + nickles * nickles_cost + pennies * pennies_cost
    resources['Money'] = {}
    resources['Money'] = round(formula, 2)
    change()
    check_transaction()
