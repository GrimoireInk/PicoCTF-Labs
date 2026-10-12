**Section 4: Python**
---

- Python Wrangling
    - Description: Python scripts are invoked kind of like programs in the Terminal... Can you run ende.py using password.txt to get flag.txt.en?

    - Get the Python script accessible in your shell by entering the following command in the Terminal prompt: $ wget followed by a link to the script. The link can be copied from the details section.
    - $ man python

        - You **NEED** to know how to run Python files in Terminal
        - python3 [python file name]
        - -d = decrypt
        - -e = encyrpt

---

- PW Crack 1
    - Description: Can you crack the password to get the flag? Download the password checker here and you'll need the encrypted flag in the same directory too.

    - To view the file in the webshell, do: $ nano level1.py
    - To exit nano, press Ctrl and x and follow the on-screen prompts.
    - The str_xor function does not need to be reverse engineered for this challenge.

        - Similar to Python Wrangling
        - Open level1.py first and **READ CAREFULLY**

---

- PW Crack 2
    - Description: Can you crack the password to get the flag? Download the password checker here and you'll need the encrypted flag in the same directory too.

    - Does that encoding look familiar?
    - The str_xor function does not need to be reverse engineered for this challenge.

        - Read level2.py 
        - Hex characters - translate them

---

- PW Crack 3
    - Description: Can you crack the password to get the flag? Download the password checker here and you'll need the encrypted flag and the hash in the same directory too.

There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

    - To view the level3.hash.bin file in the webshell, do: $ bvi level3.hash.bin
    - To exit bvi type :q and press enter.
    - The str_xor function does not need to be reverse engineered for this challenge.

        - I did guess and check, but I don't think that's correct 
        - Bridget's Write Up "modify level_3_pw_check() function to include the list of passwords at the beginning of the function and iterate through them until the correct password that matches with the stored password is found"
        - I couldn't get this to work correctly

---

- PW Crack 4
    - Description: Can you crack the password to get the flag? Download the password checker here and you'll need the encrypted flag and the hash in the same directory too.

There are 100 potential passwords with only 1 being correct. You can find these by examining the password checker script.

    - A for loop can help you do many things very quickly.
    - The str_xor function does not need to be reverse engineered for this challenge.

        - You need to reuse the loop from PW Crack 3 
        - I was able to get it to work, indentation is extremely important and will cause this not to work if incorrect

---

- PW Crack 5
    - Description: Can you crack the password to get the flag? Download the password checker here
 and you'll need the encrypted flag and the hash in the same directory too. Here's a dictionary with all possible passwords based on the password conventions we've seen so far.

    - Opening a file in Python is crucial to using the provided dictionary.
    - You may need to trim the whitespace from the dictionary word before hashing. Look up the Python string function, strip
    - The str_xor function does not need to be reverse engineered for this challenge.

        - **REVIEW CYNTAX FORMATTING AGAIN!**
        - You need to make it loop **through** the Dictonary file
            - ##  with open("dictionary.txt", "r") as f:
            ## pos_pw_list = [line.strip() for line in f]