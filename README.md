# Task-8
Build a chatbot using if-else
# ==========================================
# FINAL ADVANCED CHATBOT PROJECT
# Chatbot with Joke + Calculator Feature
# ==========================================

import datetime

print("🤖 Chatbot: Hello! I am your Python Chatbot.")
print("Type 'help' to see commands.")
print("Type 'bye' to exit.\n")

while True:
    user_input = input("You: ").lower().strip()

    # Greeting
    if user_input == "hello" or user_input == "hi":
        print("🤖 Chatbot: Hi there! 👋")

    # About chatbot
    elif user_input == "what is your name":
        print("🤖 Chatbot: My name is Python Chatbot.")

    elif user_input == "who created you":
        print("🤖 Chatbot: I was created by Dinesh using Python!")

    elif user_input == "how are you":
        print("🤖 Chatbot: I am fine and happy to chat with you!")

    # Time feature
    elif user_input == "time":
        current_time = datetime.datetime.now().strftime("%H:%M:%S")
        print("🤖 Chatbot: Current time is", current_time)

    # Date feature
    elif user_input == "date":
        today = datetime.date.today()
        print("🤖 Chatbot: Today's date is", today)

    # Joke feature
    elif user_input == "joke":
        print("🤖 Chatbot: Why do programmers prefer dark mode?")
        print("🤖 Chatbot: Because light attracts bugs! 😂")

    # Calculator feature
    elif user_input == "calculator":
        print("🤖 Chatbot: Calculator Mode Activated!")
        print("Type 'exit' to leave calculator.")

        while True:
            expression = input("Enter calculation (e.g., 5 + 3): ")

            if expression.lower() == "exit":
                print("🤖 Chatbot: Exiting Calculator Mode.")
                break

            try:
                result = eval(expression)
                print("Result:", result)
            except:
                print("Invalid calculation. Try again.")

    # Help command
    elif user_input == "help":
        print("🤖 Chatbot: Available commands:")
        print("   - hello / hi")
        print("   - what is your name")
        print("   - who created you")
        print("   - how are you")
        print("   - time")
        print("   - date")
        print("   - joke")
        print("   - calculator")
        print("   - bye")

    # Exit chatbot
    elif user_input == "bye":
        print("🤖 Chatbot: Goodbye! Have a nice day 😊")
        break

    # Unknown input
    else:
        print("🤖 Chatbot: Sorry, I don't understand that. Type 'help' for options.")
