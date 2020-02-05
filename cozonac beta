#not finished.
from Random import randrange
cozonacShelf = []
limitCozonac = 4
shelfSpace = 25
createdCozonac = []
moneyList = []

def CheckCozonac(pos): 
    result = randrange(0, 4)
    if result == 0:
        cozonacShelf[pos] = 3
        print("Cozonac is bad")
    else:
        print("Cozonac is good.")
#assignment: check if the cozonac is good or not. if you find a bad cozonac during selling remove it.
def make():
    if len(createdCozonac) >= limitCozonac:
        print("You don't have creating space left! Store cozonac to gain space!")
        return
    createdCozonac.append(1)
    print("Cozonac made")


def store():
    if len(cozonacShelf) >= shelfSpace:
        print("You don't have storage space left!")
        return
        

    
    if len(createdCozonac) == 0:
        print("You didn't create any cozonac or you don't have any of it unstored! Create some before storing it!")

    else:
        createdCozonac.pop()
        cozonacShelf.append(2)
        print("Cozonac succesfully stored!")

def count():
    print("Total of created cozonac: ", len(createdCozonac))
    print("Total of stored cozonac: ", len(cozonacShelf))
    print("Total of money: ", len(moneyList) * 5)
    print("Sales: ", len(moneyList))

def throw():
    if len(cozonacShelf) > 0:
        cozonacShelf.pop()
        print("Cozonac thrown away!")
    elif len(cozonacShelf) == 0:
        print("Put cozonac on the shelf before throwing it away!")

def eat():
    if len(createdCozonac) > 0:
        createdCozonac.pop()
        print("You ate a cozonac from the created slot!")
    elif len(cozonacShelf) > 0:
        cozonacShelf.pop()
        print("You ate a cozonac from the stored slot!")
    else:
        make() 
        createdCozonac.pop()
        print("You made and ate a cozonac from the created slot!")

def sell():
    if len(cozonacShelf) > 0:
        cozonacShelf.pop()
        moneyList.append(1)
        print("Cozonac sold!")
    elif len(cozonacShelf) == 0:
        print("Put cozonac on the shelf before selling it!")

def devMode():
    print("Cozonac in shelf: ", cozonacShelf)
    print("Cozonac in created slot: ", createdCozonac)
    print("Money: ", moneyList)

def main():
    cmd = eval(input("Tell me the command:"))
    while(cmd != "quit"):
        if cmd == "make":
            make()
        elif cmd == "eat":
            eat()
        elif cmd == "store":
            store()
        elif cmd == "count":
            count()
        elif cmd == "throw":
            throw()
        elif cmd == 'devmode':
            devMode()
        elif cmd == 'sell':
            sell()
        cmd = eval(input("Tell me the command:"))

main()
