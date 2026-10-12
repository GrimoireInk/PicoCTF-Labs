**Section 3**
---

- Wave a Flag
    - Description: Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information... warm

    - This program will only work in the webshell or another Linux computer.
    - To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget <URL here>, where the url can be found in the details section.
    - Run this program by entering the following in the Terminal prompt: $ ./warm, but you'll first have to make it executable with $ chmod +x warm
    - -h and --help are the most common arguments to give to programs to get more information from them!
    - Not every program implements help features like -h and --help.

        - Read through all lines of a file, **CAREFULLY**!

---

- Tab, Tab, Attack
    - Description: Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames. Addadshashanammu.zip

    - After unziping, this problem can be solved with 11 button-presses...(mostly Tab)...

        - My computer turned these into folders, is that meant to happen?

---

- Insp3ct0r
    - Description: Kishor Balan tipped us off that the following code may need inspection: http://chatelaine.cylabacademy.net:42300

    - How do you inspect web code on a browser?
    - There's 3 parts

        - This flag is split into 3 parts
        - Source code

---

- Strings It
    - Description: Can you find the flag in file without running it?

    - 1 strings

        - strings -a strings | grep "academy"
        - Looking at all the lines in the file then limiting the results to any lines with "academy" in them

---

- First Grep
    - Can you find the flag in the file? This would be really tedious to look through manually, something tells me there is a better way. The flag is in this file

    - grep tutorial

        - Reused the previous Grep method from the previous CTF

---

- Where are the Robots
    - Can you find the robots? http://chatelaine.cylabacademy.net:14513

    - What part of the website could tell you where the creator doesn't want you to look?

        - **DON'T LOOK INTO THE SOURCE CODE**
        - Robot.txt