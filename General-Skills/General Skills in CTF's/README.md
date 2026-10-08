# 🖥️ PicoCTF — General Skills Learning Path

This is for tracking my progress through PicoCTF's General Skills in CTF's learning path while connecting previously completed challenges to their original technical write-up.

## 📖 Overview

This learning path focuses on strengthening foundational cybersecurity skills through hands-on exercises involving command-line navigation, programming, file analysis, and problem-solving.

Some challenges overlap with activities I have already completed in the PicoCTF Challenge Library. Rather than duplicating documentation, I'll link to my original write-up.

---

## 🏆 Learning Path Progress

| Challenge | Status | Write-Up |
| :--- | :--- | :--- |
| [Challenge Name] | ✅ Previously Completed | [View Original](../Challenge-Folder/README.md) |
| [Challenge Name] | 🚧 In Progress | Pending |
| [Challenge Name] | ⬜ Not Started | — |

---

## What I Learned

- Katalyst
    - This is a magic themed game that takes CTF and Cybersecurity concepts and masks them as magic school tasks
    - This is very fun to play around with and honestly super cute as well
    - Very addictive 10/10
- General Skills in CTF's I (Video)
    - 
    - To add a non-default port do -p Port_Number
- What's a Net Cat?
    - Netcat (nc): a versatile command-line networking utility that reads and writes data across network connections using TCP or UDP protocols
    - nc [hostserver] [port]
        - **YOU DO NOT NEED -P FOR THIS COMMAND**

**Section 2: CyberChef**
- Mod 26
    - ROT13: a simple letter substitution cipher that replaces a letter with the 13th letter after it in the alphabet
    - *Used CyberChef*
- Warmed Up
    - Base 16 = Hex
    - From Hex To Decimal
- 2warm
    - From Decimal to Binary 
- Bases
    - Convert to Base 64

**Section 3**
- Wave a Flag
    - Read through all lines of a file, CAREFULLY!
- Tab, Tab, Attack
    - My computer turned these into folders, is that meant to happen?
- Insp3ct0r
    - This flag is split into 3 parts
    - Source code
- Strings It
    - strings -a strings | grep "academy"
    - Looking at all the lines in the file then limiting the results to any lines with "academy" in them
- First Grep
    - Reused the previous Grep method from the previous CTF
- Where are the Robots
    - **DON'T LOOK INTO THE SOURCE CODE**
    - Robot.txt

**Section 4: Python**
- Python Wrangling
    - You **NEED** to know how to run Python files in Terminal
    - python3 [python file name]
    - -d = decrypt
    - -e = encyrpt
- PW Crack 1
    - Similar to Python Wrangling
    - Open level1.py first and **READ CAREFULLY**
- PW Crack 2
    - Read level2.py 
    - Hex characters - translate them
- PW Crack 3
    - I did guess and check, but I don't think that's correct 
    - Bridget's Write Up "modify level_3_pw_check() function to include the list of passwords at the beginning of the function and iterate through them until the correct password that matches with the stored password is found"
    - I couldn't get this to work correctly
- PW Crack 4
    - You need to reuse the loop from PW Crack 3 
    - I was able to get it to work, indentation is extremely important and will cause this not to work if incorrect
- PW Crack 5 
    - **REVIEW CYNTAX FORMATTING AGAIN!**
    - You need to make it loop **through** the Dictonary file
        - ##  with open("dictionary.txt", "r") as f:
        ## pos_pw_list = [line.strip() for line in f]
- Enhanced!
    - Zoom in and inspect the image file
- Big Zip
    - Use -ri to search all text files and subdirectories 
    - Use the path of the folder to find it
    - grep -ri "academy" ~/folder location/big-zip-files
- Vault Door Training
    - Carefully read through the Java code
- Keygenme-py
    - This one was quite tricky for me since I don't know much about Reverse Engineering 
    - I followed this article: https://medium.com/@karimwalid/keygenme-py-picoctf-reverse-challenges-series-cae76e6a8a28
    - I will need more practice with this later
    - ## "The Low Level Binary Intro playlist is a great place to start learning Reverse Engineering and Binary Exploitation."
- Buffer Overflow 0
    - When you open the source code and the vuln file you learn that anything over 16 characters causes an overflow and it breaks the system, this gives you the flag

---

[⬅️ Return to General Skills](../README.md)