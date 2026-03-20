# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
The game would never tell me to input a higher value. 
When user imputs a value lower than the goal the game would still tell to go lower. 
But, when the user puts in the correct number, it confirms that they won.
The game only gives the user 7 attempts instead of 8.
The button "new game" doesn't work, user is required to reload the page.

- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").
  The hints were wrong, the game hints the user lower even if the secret number was higher.
  The attepts allowed did not update as required.

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).

I used claude ai extension on vscode. Claude ai was able to assist with many correct suggestions, one of them was tocorrect the function check_guess, it assisted with editing the "go lower" and "go higher", since the game was telling the user to go lower when the secret number was higher. I verified the result by checking the website and confirming it was giving me the correct hint.

- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
Claude suggested adding a misleading function to the test_game_logic_utils.py, it suggested not adding the main fuction needed to run the test, I was able to test it by using terminal

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
I decided whether a bug was reallyfixed by rerunning the code and website and retrying the game and investigating what was correct and what was wrong.

- Describe at least one test you ran (manual or using pytest) 
  and what it showed you about your code.
I ran the funtion too_high and too_low, i was able to test them manually by running the file instead of using pytest.

- Did AI help you design or understand any tests? How?
Yes AI helped me design and understand by fixing the issues on the three functions and helped me design the main test function to see each output.


---

## 4. What did you learn about Streamlit and state?

Streamlit reruns a website/app automatically refreshing the page when you change the coded, users do not need to manually refresh the page or app.
In the original code when pressing the button new game it was not letting the user create a new game due to not changing the status back to "playing", it was only updating the secret number.
The line st.session_state.status = "playing" was added so that the game starts when user clicks the button "new game."


---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
Using ai to help with mycode and retesting my code more during the process instead of only in the end,

  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
I would reavaluate his suggestions instead of accepting it at first glance. I would also be more specific when prompting a request.

- In one or two sentences, describe how this project changed the way you think about AI generated code.
It made me realize that ai assist on certain aspects but it is not always correct, therefor I need to be more careful and reavaluate whats given,