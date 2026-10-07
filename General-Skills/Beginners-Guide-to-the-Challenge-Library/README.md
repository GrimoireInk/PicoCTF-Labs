# The Beginner's Guide to the Challenge Library

## Challenge Information

| Field | Details |
| :--- | :--- |
| **Category** | General Skills |
| **Difficulty** | Beginner |
| **Status** | Completed |

---

## Challenge Overview

This introductory PicoCTF challenge focuses on learning how to navigate and use the Challenge Library.

The goal of this challenge is to become familiar with PicoCTF challenge environments and understand how these challenges are organized and accessed.

---

## Objectives

- Become familiar with the PicoCTF Challenge Library
- Learn how PicoCTF challenges are organized
- Understand how to access and interact with challenges
- Become familiar with the basic PicoCTF challenge workflow

---

## What I Learned

**What is a Flag?**
- A flag is a text string found in a challenge that proves you solved it
- Flags follow a common format: picoCTF{l33tsp34k_phr4s3_1234abcd}
    - l33tsp34k is a "language" that substitutes some letters for numbers 
    - Often the phrase given is something related to solving the challenge, but not always

**Traditional CTF Categories**
- General Skills: Challenges that build your comfort with essential tools and concepts
    - Example - Using the Linux command line, reading source code, navigating file systems, and working with encodings like base64 or hex
- Cryptography: Challenges involving encoded or encrypted data that you need to decode or break
    - Caesar ciphers or base64
    - **Harder ones introduce real cryptographic algorithms (RSA, AES) and ask you to exploit weaknesses in how they're implemented**
- Forensics: Challenges where you investigate files, disk images, network captures, or other digital artifacts to find hidden information
    - Analyze an image file with something secretly embedded in it, sift through packet captures, or recover deleted data
- Web Exploitation: Challenges that involve finding and exploiting vulnerabilities in web applications
    - Inspect page source or manipulate cookies
    - **Harder challenges involve SQL injection, cross-site scripting, or server-side logic bugs**
- Reverse Engineering: Challenges where you're given a compiled program and need to figure out what it does: usually to discover what input produces the flag
    - Use disassemblers and debuggers to read assembly code or trace program behavior
- Binary Exploitation: Challenges where you exploit memory-safety vulnerabilities in compiled programs — buffer overflows, format string bugs, use-after-free, and so on
    - **This is widely considered the hardest category**

**Approach**
- Step 1: Read the challenge description carefully
- Step 2: Look at the hints for the challenge
- Step 3: Download any files from links in the description
- Step 4: Ask 'What types of files are these?'
- Step 5: Check endpoints, other links or services that you can access using the challenge description

**Section 1: Sanity**
- Obedient Cat
    - Any hints about entering a command into the Terminal (such as the next one), will start with a '$'...everything after the dollar sign will be typed (or copy and pasted) into your Terminal
    - To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget and a link to the flag. The link can be copied from the details section
- Super SSH
    - Template for SSH: ssh username@remote_host
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

## Key Takeaways

- Opening every file can be EXTREMELY HELPFUL
- **EXAMINE EVERYTHING**
- You won't know everything, and that's ok! Learn as you go an think outside the box
- Don't overthink it at first!
