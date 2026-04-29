import random

# LIST 1: Spider-Man facts
funFacts = [
    "Spider-Man's real name is Peter Parker.",
    "He was bitten by a radioactive spider.",
    "He lives in New York City.",
    "His motto is: 'With great power comes great responsibility.'",
    "He fights villains like Green Goblin and Doctor Octopus."
]

# LIST 2: Greetings
greetings = [
    "Hey there, citizen!",
    "What's up! 🕷️",
    "Hello! Ready to save the city?"
]

# LIST 3: Villains
villains = [
    "Green Goblin",
    "Doctor Octopus",
    "Venom",
    "Sandman"
]

# PROCEDURE
def response(input):
    input = input.lower()

    if "hello" in input or "hi" in input:
        return random.choice(greetings)

    elif "who are you" in input:
        return "I'm Peter Parker! Or... Spider-Man as I'm famously known as."

    elif "fact" in input:
        response = "Here are some fun facts about me!:\n"
        for fact in funFacts:
            response = response + "- " + fact + "\n"
        return response

    elif "villain" in input:
        response = "Here are some Spider-Man villains:\n"
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
        return "See you later! Stay safe, citizen!"

    else:
        return "I don't understand that. Try asking in a different way!"


# MAIN PROGRAM

print("Hello! I'm Spider-Man") 

while True:
    usersResponse = input("You: ")

    spiderSponse = response(usersResponse)

    print("Spider-Man Bot:", spiderSponse)

    if "bye" in usersResponse.lower():
        break
