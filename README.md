# McGerbers

import random


# intro#

print("Welcome to McGerbers! What can I get for you?")

print()

print("Menu: ")

print()

#pizza topping menu#

print("1 = MUSHROOMS")

print("2 = PEPPERONI")

print("3 = SAUSAGE")

print("4 = PINEAPPLE")

print("5 = OLIVES")

print()

print()

topping = int(input("YOUR CHOICE: "))

print()
#options - what topping you get#
if topping == 1:

    topping = "PINEAPPLE"



elif topping == 2:

    topping = "MUSHROOM"



elif topping == 3:

    topping = "PEPPERONI"



elif topping == 5:

    topping = "SAUSAGE"



elif topping == 4:

    topping = "OLIVE"



else:

    topping = random.randint(1,5)



    if topping == 1:

        topping = "PINEAPPLE"



    elif topping == 2:

        topping = "MUSHROOMS"



    elif topping == 3:

        topping = "PEPPERONI"



    elif topping == 5:

        topping = "SAUSAGE"



    elif topping == 4:

        topping = "OLIVES"



    print("Alright, we'll pick for you.")



# BREAD #



print("What bread would you like?")

print()

print("Menu: ")

print()

print("1 = SOURDOUGH")

print("2 = FLATBREAD")

print("3 = BURNT")

print("4 = RYE")

print("5 = WHOLE WHEAT")

print()

print()

bread = int(input("YOUR CHOICE: "))

print()

if bread == 1:

    bread = "RYE"



elif bread == 2:

    bread = "WHOLE WHEAT"



elif bread == 3:

    bread = "SOURDOUGH"



elif bread == 5:

    bread = "BURNT"



elif bread == 4:

    bread = "FLATBREAD"



else:

    bread = random.randint(1,5)



    if bread == 1:

        bread = "RYE"



    elif bread == 2:

        bread = "WHOLE WHEAT"



    elif bread == 3:

        bread = "SOURDOUGH"



    elif bread == 5:

        bread = "BURNT"



    elif bread == 4:

        bread = "FLATBREAD"
  

    print("Alright, we pick for you.")





# CHEESE #



print("What type of cheese would you like?")

print()

print("Menu: ")

print()

print("1 = PEPPERJACK")

print("2 = AMERICAN")

print("3 = ITALIAN")

print("4 = CHEDDAR")

print("5 = MOZZERELA")

print()

print()

cheese = int(input("YOUR CHOICE: "))

print()

if cheese == 1:

    cheese = "ITALIAN"



elif cheese == 2:

    cheese = "CHEDDAR"



elif cheese == 3:

    cheese = "MOZZERELA"



elif cheese == 5:

    cheese = "AMERICAN"



elif cheese == 4:

    cheese = "PEPPERJACK"



else:

    cheese = random.randint(1,5)



    if cheese == 1:

        cheese = "ITALIAN"



    elif cheese == 2:

        cheese = "CHEDDAR"



    elif cheese == 3:

        cheese = "MOZZERELA"



    elif cheese == 5:

        cheese = "AMERICAN"



    elif cheese == 4:

        cheese = "PEPPERJACK"

print("Alright, we pick for you.")



# DRINK #



print("What drink would you like?")

print()

print("Menu: ")

player_blocking = False


print()

print("1 = KOKO KOLU")

print("2 = DR. SALT")

print("3 = SANTA")

print("4 = GRITE")

print("5 = CHERRY DR SALT")

print()

print()

soda = int(input("YOUR CHOICE: "))

print()

if soda == 1:

    soda = "CHERRY DR SALT"



elif soda == 2:

    soda = "KOKO KOLU"



elif soda == 3:

    soda = "DR SALT"



elif soda == 5:

    soda = "GRITE"



elif soda == 4:

    soda = "SANTA"



else:

    soda = random.randint(1,5)



    if soda == 1:

        soda = "CHERRY DR SALT"



    elif soda == 2:

        soda = "KOKO KOLU"



    elif soda == 3:

        soda = "DR SALT"



    elif soda == 5:

        soda = "GRITE"



    elif soda == 4:

        soda = "SANTA"

    print("Alright, we pick for you.")


print()
print("Alright, you get a " + topping + " pizza on " + bread + " bread with " +  cheese + " cheese and a " + soda+ ".")

#DIALOUGE#

print()

print("YOU: That's not my order, pizza man.")

input("[PRESS ENTER TO CONTINUE]")

print()

cost = random.randint(5, 14)
cost = cost * 2.5
print("PIZZA MAN: Can't you read the sign? No refunds. That'll be $" + str(cost) + ".")

input("[PRESS ENTER TO CONTINUE]")

print()

print("YOU: No, I need a refund.")
input("[PRESS ENTER TO CONTINUE]")

print()

print("PIZZA MAN: Your know what? I've been so fed up with your constant blabbering. I only make 7 dollars an hour but with this treatment i feel like i should be paid triple that.") 

print("[THROWS PIZZA AT YOU]")

print()

print("--- BATTLE STARTS ---")
print()

battle = True 
player_blocking = 0  # Number of rounds remaining for player block
pizza_man_blocking = 0  # Number of rounds remaining for pizza man block
p1win = False
p2win = False
p1 = 30
p2 = 30
move = 1
while battle == True:
    #Player's turn
    print("ROUND " + str(move))
    print()
    print("YOUR HEALTH: " + str(p1))
    print("THEIR HEALTH: " + str(p2))
    print()
    print("YOUR MOVES:")
    print()
    print("1 = ATTACK [3dmg 25% crit for 5 dmg]")
    print("2 = DEFEND [50% chance to fully block and lasts 2 rounds if used sucessfully")
    print("3 = HEAL   [2hp healed 33% chance of 4hp healed]")

    choice1 = input("YOUR MOVE: ")
    print()

    if int(choice1) == 1:
        if pizza_man_blocking > 0:
            print("PIZZA MAN BLOCKED YOUR ATTACK! (" + str(pizza_man_blocking - 1) + " rounds remaining)")
            pizza_man_blocking -= 1
        else:
            crit = random.randint(1, 4)
            if crit == 1:
                p2 -= 5
                print("CRITICAL HIT!")
            else:
                print("IT HIT")
                p2 -= 3

    elif int(choice1) == 2:
        block = random.randint(1, 2)
        if block == 1:
            player_blocking = 2
            print("BLOCKED! (2 rounds remaining)")
        else:
            player_blocking = 0
            print("THE PIZZA BROKE!")

    elif int(choice1) == 3:
        heal = random.randint(1, 3)
        if heal == 1:
            p1 += 4
            print("HEALED + 4!")
        else:
            p1 += 2
            print("HEALED + 2!")

    # Update blocking status
    if player_blocking > 0:
        player_blocking -= 1
    if pizza_man_blocking > 0:
        pizza_man_blocking -= 1

    # Pizza Man's turn
    move_chance = random.randint(1, 100)
    choice2 = 1 if move_chance <= 50 else (2 if move_chance <= 75 else 3)
    print("PIZZA MANS MOVE: " + str(choice2))

    if int(choice2) == 1:
        if player_blocking > 0:
            print("YOUR BLOCK PROTECTED YOU! (" + str(player_blocking - 1) + " rounds remaining)")
        else:
            crit = random.randint(1, 4)
            if crit == 1:
                p1 -= 5
                print("YOU ARE HIT [CRITICAL]!")
            else:
                print("IT HIT!")
                p1 -= 3

    elif int(choice2) == 2:
        block = random.randint(1, 2)
        if block == 1:
            pizza_man_blocking = 2
            print("HE BLOCKED IT! (2 rounds remaining)")
        else:
            pizza_man_blocking = 0
            print("HIS PIZZA BROKE!")

    elif int(choice2) == 3:
        heal = random.randint(1, 3)
        if heal == 1:
            p2 += 4
            print("HE HEALED! + 4")
        else:
            p2 += 2
            print("HE HEALED! + 2")

    move += 1

    # Check health to end the battle
    if p1 <= 0:
        battle = False
        p2win = True
    elif p2 <= 0:
        battle = False
        p1win = True

        print()
        print("--- BATTLE ENDS ---")
        print()
if p1win == True:
    print("YOU WIN!")
    print()
    print("PIZZA MAN: I'm sorry, I'll give you a refund.")
    print()
    print("You sucessfully won! The pizza was free and the store was shut down!")
else:
    print("YOU LOSE!")
