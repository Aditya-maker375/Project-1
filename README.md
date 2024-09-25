# Project-1
As a begineer i did this project in python language
# List of quiz questions, choices, and answers
quiz_data = [
    {
        "question": "What is the capital of France?",
        "choices": ["A) Berlin", "B) Madrid", "C) Paris", "D) Rome"],
        "answer": "C"
    },
    {
        "question": "Which planet is known as the Red Planet?",
        "choices": ["A) Earth", "B) Mars", "C) Jupiter", "D) Saturn"],
        "answer": "B"
    },
    {
        "question": "Who wrote 'Hamlet'?",
        "choices": ["A) Charles Dickens", "B) J.K. Rowling", "C) William Shakespeare", "D) George Orwell"],
        "answer": "C"
    },
    {
        "question": "What is the largest ocean on Earth?",
        "choices": ["A) Atlantic Ocean", "B) Indian Ocean", "C) Arctic Ocean", "D) Pacific Ocean"],
        "answer": "D"
    },
    {
        "question": "What is the smallest prime number?",
        "choices": ["A) 1", "B) 2", "C) 3", "D) 5"],
        "answer": "B"
    }
]

# Function to ask the questions and get answers
def play_quiz():
    score = 0
    total_questions = len(quiz_data)
   
    print("\nWelcome to the Quiz Game!\n")
   
    for idx, item in enumerate(quiz_data):
        print(f"Question {idx + 1}: {item['question']}")
        for choice in item["choices"]:
            print(choice)
       
        user_answer = input("Your answer (A, B, C, or D): ").upper()
       
        if user_answer == item['answer']:
            print("Correct!\n")
            score += 1
        else:
            print(f"Wrong! The correct answer is {item['answer']}.\n")
   
    # Final score
    print(f"Quiz Complete! You scored {score} out of {total_questions}.\n")

# Main program loop
def main():
    while True:
        play_quiz()
        replay = input("Do you want to play again? (yes/no): ").lower()
        if replay != 'yes':
            print("Thanks for playing! Goodbye!")
            break

if _name_ == "_main_":
    main()
