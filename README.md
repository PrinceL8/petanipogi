	divider_line = ("=" * 50)
	xp_per_level = 30

	print("Welcome to Python Quest!")
	player_name = input("What is your name? ")
	if player_name == "":
    	player_name = "Python Learner"
	print(f"Hi {player_name}! Fill in the blanks and fix the bugs.")
	print("You get 2 tries per exercise: 10 XP on the first, 5 XP on the second.")
	print("If you get one wrong, you will see a hint.")
	input("\n(press Enter to start)")

	total_xp = 0
	player_level = 1

	for lesson_number in range(1, 7):


    print("")
    print(divider_line)
    if lesson_number == 1:
        print("LESSON 1: Print")
        print(divider_line)
        print("print() shows things on the screen.")
        print('    print("Hello!")         # text needs quotes')
        print('    print("Score:", 100)    # numbers do not')
        print("Python is case sensitive: print works, Print does not.")
    elif lesson_number == 2:
        print("LESSON 2: Variables")
        print(divider_line)
        print("A variable stores a value.")
        print("    age = 15")
        print("    print(age)              # shows 15")
        print("Names cannot have spaces: my_age is good, my age is bad.")
        print("A variable can change:")
        print("    x = 5")
        print("    x = x + 1               # x is now 6")
    elif lesson_number == 3:
        print("LESSON 3: If / Else")
        print(divider_line)
        print("An if runs code only when its condition is True.")
        print("    if age >= 18:")
        print('        print("adult")')
        print("    else:")
        print('        print("child")')
        print("The if / else line ends with a colon. == compares, = stores.")
        print("Use elif for extra choices.")
    elif lesson_number == 4:
        print("LESSON 4: Nested conditions")
        print(divider_line)
        print("A nested condition is an if inside an if.")
        print("The inner code is indented 4 MORE spaces.")
        print("    if x > 5:")
        print("        if x > 8:")
        print('            print("very big")')
        print("You can also combine conditions with and / or:")
        print("    if age >= 13 and has_ticket:")
    elif lesson_number == 5:
        print("LESSON 5: Arrays (lists)")
        print(divider_line)
        print("A list stores many items in [ ].")
        print('    fruits = ["apple", "pear", "plum"]')
        print("Counting starts at 0: fruits[0] is apple, fruits[2] is plum.")
        print('    fruits.append("kiwi")    # adds to the end')
        print("    len(fruits)              # counts the items")
    else:
        print("LESSON 6: Loops")
        print(divider_line)
        print("A for loop repeats a set number of times:")
        print("    for i in range(3):")
        print("        print(i)             # 0, 1, 2")
        print("A while loop repeats while its condition is True:")
        print("    while count < 3:")
        print("If the condition never becomes False, it never ends!")

    input("\n(press Enter to start the exercises)")


    for exercise_number in range(1, 4):

        code_line_1 = ""
        code_line_2 = ""
        code_line_3 = ""
        code_line_4 = ""
        code_line_5 = ""
        alternative_answer = ""

        if lesson_number == 1:
            if exercise_number == 1:
                exercise_type = "FILL IN THE BLANK"
                exercise_prompt = "Show text on the screen."
                code_line_1 = '____("Hello, world!")'
                correct_answer = "print"
                hint = "It is the function that shows output."
            elif exercise_number == 2:
                exercise_type = "FIX THE BUG"
                exercise_prompt = "Type the fixed line."
                code_line_1 = "print(Hello)"
                correct_answer = 'print("Hello")'
                alternative_answer = "print('Hello')"
                hint = "Text needs quotes around it."
            else:
                exercise_type = "FILL IN THE BLANK"
                exercise_prompt = "Make it show:  Score: 100"
                code_line_1 = 'print("Score:", ____)'
                correct_answer = "100"
                hint = "Numbers do not need quotes."

        elif lesson_number == 2:
            if exercise_number == 1:
                exercise_type = "FILL IN THE BLANK"
                exercise_prompt = "Make the program show 15."
                code_line_1 = "age = ____"
                code_line_2 = "print(age)"
                correct_answer = "15"
                hint = "print(age) shows whatever age is storing."
            elif exercise_number == 2:
                exercise_type = "FIX THE BUG"
                exercise_prompt = "Type the fixed line."
                code_line_1 = "my age = 12"
                correct_answer = "my_age = 12"
                alternative_answer = "my_age=12"
                hint = "Use an underscore _ instead of the space."
            else:
                exercise_type = "FIX THE BUG"
                exercise_prompt = "We want to show 6. Type the fixed line 2."
                code_line_1 = "x = 5"
                code_line_2 = "x + 1"
                code_line_3 = "print(x)"
                correct_answer = "x = x + 1"
                alternative_answer = "x=x+1"
                hint = "Store the new value back into x."

        elif lesson_number == 3:
            if exercise_number == 1:
                exercise_type = "FILL IN THE BLANK"
                exercise_prompt = "Fill in the blank."
                code_line_1 = "age = 20"
                code_line_2 = "____ age >= 18:"
                code_line_3 = '    print("adult")'
                correct_answer = "if"
                hint = "This keyword starts a condition."
            elif exercise_number == 2:
                exercise_type = "FIX THE BUG"
                exercise_prompt = "Type the fixed line 2."
                code_line_1 = "x = 7"
                code_line_2 = "if x > 5"
                code_line_3 = '    print("big")'
                correct_answer = "if x > 5:"
                alternative_answer = "if x>5:"
                hint = "An if line must end with a colon."
            else:
                exercise_type = "FILL IN THE BLANK"
                exercise_prompt = "Fill in the blank (line 4)."
                code_line_1 = "x = 3"
                code_line_2 = "if x > 5:"
                code_line_3 = '    print("big")'
                code_line_4 = "____:"
                code_line_5 = '    print("small")'
                correct_answer = "else"
                hint = "It runs when the if condition is False."

        elif lesson_number == 4:
            if exercise_number == 1:
                exercise_type = "WHAT PRINTS?"
                exercise_prompt = "What does this program print?"
                code_line_1 = "x = 10"
                code_line_2 = "if x > 5:"
                code_line_3 = "    if x > 8:"
                code_line_4 = '        print("very big")'
                correct_answer = "very big"
                hint = "x is bigger than 5 AND bigger than 8."
            elif exercise_number == 2:
                exercise_type = "FILL IN THE BLANK"
                exercise_prompt = "Both things must be True. Fill in the blank."
                code_line_1 = "age = 20"
                code_line_2 = "has_id = True"
                code_line_3 = "if age >= 18 ____ has_id:"
                code_line_4 = '    print("Enter")'
                correct_answer = "and"
                hint = "Both things must be True."
            else:
                exercise_type = "FILL IN THE BLANK"
                exercise_prompt = "How many spaces is line 3 indented? (type a number)"
                code_line_1 = "if a > 0:"
                code_line_2 = "    if b > 0:"
                code_line_3 = '        print("both")'
                correct_answer = "8"
                hint = "Each level of nesting adds 4 spaces."

        elif lesson_number == 5:
            if exercise_number == 1:
                exercise_type = "FILL IN THE BLANK"
                exercise_prompt = "Show the first item (apple). Which index?"
                code_line_1 = 'fruits = ["apple", "pear", "plum"]'
                code_line_2 = "print(fruits[____])"
                correct_answer = "0"
                hint = "Counting starts at 0."
            elif exercise_number == 2:
                exercise_type = "FILL IN THE BLANK"
                exercise_prompt = "Add green to the end of the list."
                code_line_1 = 'colors = ["red", "blue"]'
                code_line_2 = 'colors.____("green")'
                correct_answer = "append"
                hint = "It is the list method that adds an item to the end."
            else:
                exercise_type = "FIX THE BUG"
                exercise_prompt = "There is no index 3. Which index shows the LAST item?"
                code_line_1 = "nums = [10, 20, 30]"
                code_line_2 = "print(nums[3])"
                correct_answer = "2"
                hint = "Counting starts at 0, so the indexes are 0, 1, 2."

        else:
            if exercise_number == 1:
                exercise_type = "FILL IN THE BLANK"
                exercise_prompt = "Repeat 3 times. Fill in the blank."
                code_line_1 = "for i in ____(3):"
                code_line_2 = "    print(i)"
                correct_answer = "range"
                hint = "range(3) gives 0, 1, 2."
            elif exercise_number == 2:
                exercise_type = "FILL IN THE BLANK"
                exercise_prompt = "Fill in the blank."
                code_line_1 = "count = 0"
                code_line_2 = "____ count < 3:"
                code_line_3 = "    count = count + 1"
                correct_answer = "while"
                hint = "This loop repeats while a condition is True."
            else:
                exercise_type = "FIX THE BUG"
                exercise_prompt = "This loop never stops! Type the line to add inside it (no indent)."
                code_line_1 = "count = 0"
                code_line_2 = "while count < 3:"
                code_line_3 = "    print(count)"
                correct_answer = "count = count + 1"
                alternative_answer = "count=count+1"
                hint = "count never changes, so count < 3 stays True forever."

        if alternative_answer == "":
            alternative_answer = correct_answer


        print(f"{player_name}  |  Level {player_level}  |  XP {total_xp}")
        print(divider_line)
        print(f"Exercise {exercise_number} of 3  |  {exercise_type}")
        print(exercise_prompt)
        print("")
        if code_line_1 != "":
            print(f"  1 | {code_line_1}")
        if code_line_2 != "":
            print(f"  2 | {code_line_2}")
        if code_line_3 != "":
            print(f"  3 | {code_line_3}")
        if code_line_4 != "":
            print(f"  4 | {code_line_4}")
        if code_line_5 != "":
            print(f"  5 | {code_line_5}")
        print("")


        is_solved = False
        for try_number in range(2):
            player_answer = input("Your answer: ")
            if player_answer == correct_answer or player_answer == alternative_answer:
                is_solved = True
                if try_number == 0:
                    xp_gained = 10
                else:
                    xp_gained = 5
                total_xp = total_xp + xp_gained
                print(f"Correct!  +{xp_gained} XP  (total: {total_xp})")
                if total_xp // xp_per_level + 1 > player_level:
                    player_level = total_xp // xp_per_level + 1
                    print(f"*** LEVEL UP! You are now level {player_level}! ***")
                break
            elif try_number == 0:
                print("Not quite. Hint: " + hint)
        if not is_solved:
            print(f"Not this time. The right answer was: {correct_answer}")

        input("\n(press Enter to continue)")

	print("")
	print(divider_line)
	print(f"All done, {player_name}!")
	print(f"Final XP: {total_xp}   Final level: {player_level}")
