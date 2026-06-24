# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
| guess of 60 with <br /> secret number 66| should output "GO HIGHER" | instead outputs "GO LOWER" | None
| pressed submit guess <br /> after clicking new game | submits guess and shows hint <br /> if checkmarked | outputs "Already guessed"| None
| last attempt | "Attempts left: 0" | "Attempts left: 1" | None
---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?  
__Claude__
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).  
__An example of an AI suggestion that was correct was showing that the range for random numbers was always set from 1 to 100, regardless of difficulty level. It suggested to set the argument to variables low and high, which save the range bounds for the selected difficulty.__

- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
__This wasn't necessarily an incorrect suggestion (rather a misleading suggestion) but it fixed the logic behind not keeping the random range generator static, but dynamic to the difficulty level selected. However, it didn't update or fix the user interface, which always showed 1 to 100.__

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
__I ran the streamlit command several times since pytest was throwing errors at me__
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
__A test that I did run manually was intentionally putting a higher number than the secret, as well as a lower, to check whether the hint was logical. It showed that the hint it was throwing at the user was misleading__
- Did AI help you design or understand any tests? How?
__It helped me design the conftest.py file to actually help me run pytest.__
---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
__Session state is reset during reruns and the website returns to its orignal state with no inputs given, and erases previous input and history__
---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
  __Prompt using line numbers__
- What is one thing you would do differently next time you work with AI on a coding task?
  __Create more test cases using AI__
- In one or two sentences, describe how this project changed the way you think about AI generated code.
  __Takes up a lot of tokens for prompts that are very brief! Doesn't use logic sometimes__
