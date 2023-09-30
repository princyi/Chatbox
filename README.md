# Chatbox

CHATBOT WITH RULE-BASED
RESPONSES
Build a simple chatbot that responds to user inputs based on
predefined rules. Use if-else statements or pattern matching
techniques to identify user queries and provide appropriate
responses. This will give you a basic understanding of natural
language processing and conversation flow



import random


# Function to generate a random greeting
def get_greeting():
    greetings = ["Hello!", "Hi there!", "Greetings!"]
    return random.choice(greetings)


# Function to generate a response based on user input
def get_response(user_input):
    user_input = user_input.lower()

    # Define some predefined patterns and their corresponding responses
    if "hello" in user_input:
        return get_greeting()
    elif "how are you" in user_input:
        return "I'm just a chatbot, so I don't have feelings, but thanks for asking!"
    elif "your name" in user_input:
        return "I'm just a chatbot, you can call me ChatBot."
    elif "goodbye" in user_input:
        return "Goodbye! Have a great day!"
    else:
        return "I'm not sure how to respond to that."


# Main loop to chat with the bot
print("Hello! I'm ChatBot. You can start a conversation or type 'exit' to quit.")
while True:
    user_input = input("You: ")
    if user_input.lower() == "exit":
        print("ChatBot: Goodbye!")
        break
    response = get_response(user_input)
    print("ChatBot:", response)
