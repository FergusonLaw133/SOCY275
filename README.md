# SOCY275
SOCY 275 UDL NOTES
# Trivia Game: Subcultural Theories & Neighborhood Explanations of Crime

questions = [
    {
        "question": "What is the central premise of subcultural theories in criminology?",
        "options": ["Crime is a product of individual mental illness", 
                    "Crime emerges from conflicts between mainstream societal goals and the means available to achieve them", 
                    "Crime is an inevitable part of urbanization", 
                    "Crime is primarily a result of biological factors"],
        "answer": 2,
        "correct_explanation": "Subcultural theories, particularly strain theory, argue that crime arises when individuals experience strain due to the disconnect between societal goals and the limited means to achieve them.",
        "wrong_explanation": "Incorrect. Subcultural theories focus on the disconnect between societal goals and the means to achieve them, not mental illness or urbanization."
    },
    {
        "question": "According to Elijah Anderson's 'Code of the Street,' how is respect maintained in disadvantaged neighborhoods?",
        "options": ["Through adherence to formal legal systems", 
                    "By showing toughness and retaliating to perceived slights", 
                    "By avoiding confrontation at all costs", 
                    "By cooperating with law enforcement"],
        "answer": 2,
        "correct_explanation": "In Anderson's framework, maintaining respect often involves using violence or displaying toughness in response to disrespect.",
        "wrong_explanation": "Incorrect. In the 'Code of the Street,' respect is often maintained by showing toughness and retaliating to perceived slights, not by cooperating with formal systems."
    },
    # Add more questions here in the same format...
    # This is a template to add all 20 questions
]

def run_game():
    score = 0
    total_questions = len(questions)

    print("Welcome to the Subcultural Theories & Neighborhood Explanations of Crime Trivia!")
    print("Answer the following questions by typing the number of the correct option.\n")

    for idx, question in enumerate(questions):
        print(f"Question {idx + 1}: {question['question']}")
        for i, option in enumerate(question['options'], 1):
            print(f"{i}. {option}")

        try:
            answer = int(input("\nEnter the number of your answer: "))
            if answer == question['answer']:
                print("\nCorrect!")
                print(question['correct_explanation'])
                score += 1
            else:
                print("\nWrong!")
                print(question['wrong_explanation'])
        except ValueError:
            print("\nInvalid input. Please enter a number corresponding to the options.")
        
        print("\n---------------------------------\n")

    # Final Score
    print(f"Game Over! Your final score is {score} out of {total_questions}.\n")

if __name__ == "__main__":
    run_game()
