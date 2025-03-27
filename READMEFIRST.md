Here you will find how I thought of making my programs the way I did. I will address the problem, the solution, and the challenges I faced, respectively.

Q1 Thought Process
  Problem: (var1 + 2) / (var2 - var3)
  Immediately, my first thought with creating a program for this situation was to choose variables that would result in an integer, like 5. However, after seeing that a remainder was required,
  I changed the variables such that the quotient would be 7, and the remainder would be 1. When it came to choosing how to display the results, I decided to pull the quotient and remainder from
  al and ah so I could store them in cl and bl, respectively. So, in the portion of the picture that says "EAX(AL) --> ECX(CL) Quotient," it's simply stating that I understood where the
  quotient was going to be as well as the remainder, though I moved them on purpose for the sake of displaying the values.

  Challenges
  The only challenge I had with implementing this program was identifying where my typo was after I had mistakenly typed "mov [remaindder], bl".

Q3 Thought Process
  Problem: Identify an even or odd number
  My first thought for this was to use the TEST instruction since it can test for either a 1 or 0 in the least significant bit. Since the least significant bit determines whether a number in
  binary is odd or even, I tested for it and made two separate cases "is_even" and "is_odd" to determine if the preselected numbers, 2 and 3, were either odd or even.

  Challenges
  I had two challenges I faced with implementing this code. The first challenge was my misunderstanding of what the line "test al, 1" actually does. It does check for a 1 in the lsb, but I had
  mistakenly used "jnz" instead of the "jz" instruction for testing if two was even. So, if the Zero Flag was raised, nothing would happen, and it would simply move on to exit the program.
  After identifying the issue and the cause, I reworked the code so that it was able to produce the desired outputs in the registers as well as printing "even" or "odd" depending on the value.
