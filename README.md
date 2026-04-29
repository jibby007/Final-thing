import random

funFacts = [
    "I'm actually Peter Parker.",
    "I was bitten by a radioactive spider.",
    "I live in New York City.",
    "My uncles motto is: 'With great power comes great responsibility.'",
    "I fight crazy bad villains like Green Goblin and Doctor Octopus."
]

greetings = [
    "Hey there, citizen!",
    "What's up!",
    "Hello! Ready to save the city?"
]

villains = [
    "Green Goblin",
    "Doctor Octopus",
    "Venom",
    "Sandman"
]

def response(input):
    input = input.lower()

    if "hello" in input or "hi" in input:
        return random.choice(greetings)

    elif "who are you" in input:
        return "I'm Spider-Man! Or... Peter Parker as some know me as."

    elif "fact" in input:
        response = "Here are some fun facts about me!:\n"
        for fact in funFacts:
            response = response + "- " + fact + "\n"
        return response

    elif "villain" in input:
        response = "Here are some of my villains:\n"
        for v in villains:
            response = response + "- " + v + "\n"
        return response

    elif "fight" in input:
        enemy = random.choice(villains)

        responses = [
            "Spider-Man swings in and fights ",
            "Spider-Man dodges attacks from ",
            "Spider-Man uses his webs against ",
            "Spider-Man outsmarts "
        ]

        action = random.choice(responses)

        return action + enemy + "!"

    elif "bye" in input:
        return "See you later! Stay safe, weird citizen!"

    else:
        return "Hold on I'm not all knowing like Mr. Richards!"


# MAIN PROGRAM

print("Hello! I'm Spider-Man") 

while True:
    usersResponse = input("You: ")

    spiderSponse = response(usersResponse)

    print("Spider-Man:", spiderSponse)

    if "bye" in usersResponse.lower():
        break
