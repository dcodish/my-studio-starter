# Prompts for each round (copy, then edit)

Each round ends with something that works, and with the documents up to date.

## Round 0: Open the project (19:18)
Claude app → Code tab → pick the folder `my-studio-starter-main`. Permission mode: **Manual**.

    What's in this folder? Explain what each file is for, in plain words.

Watch what it does before it answers: it reads the files first.
**Habit 1: Claude only knows what is in the folder and the chat. Give context in files.**

## Round 1: Requirements (19:25)
1. Pick an idea from IDEAS.md (one minute).
2. Open `docs/REQUIREMENTS.md` and write the 3 lines under **In my words** yourself.
   Want Claude to use your Calendar or Drive? Connect it now (Settings → Connectors) and
   say so in **In my words**.
3. Paste:

       Read the "In my words" section of docs/REQUIREMENTS.md. Ask me up to 3 questions,
       one at a time. Then fill in the rest of docs/REQUIREMENTS.md: goal, users, R1-R3
       each with an acceptance test, nice to have, out of scope. Don't write any code.

4. Read R1-R3 and their tests. Fix them until they say what you meant.

**Habit 2: requirements and plan live in files, not in the chat.**

## Round 2: Design, then build to the plan (19:35)
Switch to **Plan** mode and paste:

    Read docs/REQUIREMENTS.md. Propose the architecture and a step-by-step plan for R1-R3.
    When I approve, write docs/ARCHITECTURE.md and docs/PLAN.md and stop. No code yet.

Read both files (2 minutes). Ask about anything you don't understand. Then:

    Build all the steps in docs/PLAN.md for R1-R3.

Open index.html and run every acceptance test yourself. Write pass or fail in the Status column.
**Habit 3: check against the acceptance tests, not by feel.**

## Round 3: Find a bug, test first (19:50)
Describe what you SEE, not how to code it. Then:

    First add an acceptance test for this bug to docs/REQUIREMENTS.md, then fix it.

You can also drag a screenshot into the chat and say what's wrong.
Going the wrong way? Press **Esc** to stop it. Then rerun all the tests.

## Round 4: Memory, nothing to type (20:05)
A short talk. What to remember:
- General preferences for every project ("explain in Hebrew, I'm a beginner") go in your personal `~/.claude/CLAUDE.md`.
- Rules for this project go in this folder's `CLAUDE.md`. What you're building lives in `docs/`.
- The chat disappears with `/clear`. Files stay.

Working from another computer? The project folder travels if it's in the cloud (GitHub, OneDrive,
Google Drive). Your personal `CLAUDE.md`, Claude's auto memory and your chat history stay on the
machine. On the other computer, start a new chat:

    Read docs/PLAN.md and CHANGELOG.md and tell me where we are.

**Habit 4: general or project-specific? Decide before you save it.**
Use the rest of the round to finish running your R1-R3 tests.

## Round 5: The wow moment (20:15)

    Add the wow moment as a new requirement R4 with an acceptance test,
    add its steps to docs/PLAN.md, then build it.

A new feature = a new requirement. A small change (color, text) = just a CHANGELOG line.
Make the browser window narrow like a phone and check. Works? `/clear`, then the next one.

## Round 6: Publish (20:30)

    Publish index.html as an artifact so I can share it, and add the link to README.md.

Open the page, click **Share**, choose the public link. Open the link on your
phone and run the tests again (habit 3). Then send it to the WhatsApp group.

Staying for the open work hour (21:00–22:00)? Keep building, or pick a mission from BONUS.md.
