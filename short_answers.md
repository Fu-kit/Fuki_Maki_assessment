Question 1: AI as a Programming Partner

Q)Describe two distinct ways you could use an AI tool during the "Understand" and "Identify Input/Output" phases of our six-step programming methodology. Provide specific example prompts and expected outputs.

A)Regarding the two distinct ways to utilize AI tools during the "Understanding" and "Input/Output Identification" phases, in other words: ① There is a phase for understanding the problem and ② a phase for understanding what goes in and what comes out. ① In the first phase, it's necessary to ask the AI "what exactly is being requested" and "what difficult situations might arise." This is because it helps reveal implicit requirements and preconditions that cannot be explicitly interpreted from the problem statement. ② In the second phase, it's necessary to have the AI provide examples of inputs and outputs. This is because it helps in dealing with extreme cases (invalid inputs or abnormal values).

Q)Explain why using AI in these early stages is beneficial, and what potential pitfalls you need to be aware of. How does this align with the "thinking" aspect of programming (programming = thinking + planning + coding)?

A)Even if I ask AI from the early stages, I don’t know what the problem is or what kind of questions I should ask. This is what I consider a potential pitfall.
As a countermeasure to this problem, I ask the AI, 'Please help me understand the problem' and 'Please provide appropriate example questions.


Question 2: Debugging with AI

Q)Identify the error(s) in this code and explain what will happen when it runs.
A)The main error is handling empty lists. When processing the second test case [] (empty list), len(numbers) becomes 0, which leads to a division by zero error (ZeroDivisionError) when calculating total / len(numbers).

Q)Write a specific prompt you would give an AI tool to help debug this code. The prompt should guide the AI to help you learn, not just fix the problem.
A)

Please identify the error clearly and explain what each part of the code does.

An AI suggested the following code. I think it handles the error we found (i.e., the case of an empty list) well. What do you think?

Based on what we’ve found so far, could you provide a complete, ready-to-use version of the code?

Is there a simpler version of your code that keeps its strengths?

Q)Fix the code and explain your solution approach.
A)Add a conditional statement to check whether the list is empty.

python
Copy
Edit
from typing import List, Optional

def calculate_average(numbers: List[float]) -> Optional[float]:
    """Calculates the average of a list of numbers. Returns None if the list is empty."""
    if not numbers:
        return None
    return sum(numbers) / len(numbers)

# Test cases
if __name__ == "__main__":
    test_cases = [
        ([1, 2, 3], 2.0),
        ([], None),
        ([-1, 0, 1], 0.0),
        ([10.5, 20.5], 15.5),
    ]
    
    for numbers, expected in test_cases:
        result = calculate_average(numbers)
        assert result == expected, f"{numbers}: expected {expected}, got {result}"
        print(f"✓ {numbers} → {result}")







