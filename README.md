# python-quiz-game
questions = ("How many elements are in the periodic table?",
             "Which animal lays the largest eggs?",
             "What is the most abundant gas in the earth's atmosphere?",
             "How many bones are in the human body?",
             )
             
options = (("A. 116", "B. 117", "C. 118", "D. 119"),
           ("A. whale", "B. crocodile", "C. ostrich", "D. dog"),
           ("A. nitrogen", "B. oxygen", "C. carbon dioxide", "D. hydrogen"),
           ("A. 206", "B. 207", "C. 208", "D. 209"))

answers = ("C", "C", "A", "A")
guesses = []
score = 0
question_num = 0

for question in questions:
    print("---------------------")
    print(question)
    
    # Display the options for the current question
    for option in options[question_num]:
        print(option)
    
    guess = input("Enter your answer (A, B, C, or D): ").upper()
    guesses.append(guess)
    
    if guess == answers[question_num]:
        print("Correct!")
        score += 1
    else:
        print("Wrong!")
    
    question_num += 1

print(f"\nYour final score is {score}/{len(questions)}")
