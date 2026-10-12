Section 5:
---

- Enhanced!
    - Description: Download this image file and find the flag.

        - Zoom in and inspect the image file

---

- Big Zip
    - Description: Unzip this archive and find the flag.

    - Can grep be instructed to look at every file in a directory and its subdirectories?

        - Use -ri to search all text files and subdirectories 
        - Use the path of the folder to find it
        - grep -ri "academy" ~/folder location/big-zip-files

---

- Vault Door Training
    - Description: Your mission is to enter Dr. Evil's laboratory and retrieve the blueprints for his Doomsday Project. The laboratory is protected by a series of locked vault doors. Each door is controlled by a computer and requires a password to open. Unfortunately, our undercover agents have not been able to obtain the secret passwords for the vault doors, but one of our junior agents obtained the source code for each vault's computer! You will need to read the source code for each level to figure out what the password is for that vault door. As a warmup, we have created a replica vault in our training facility.

The source code for the training vault is here: VaultDoorTraining.java

        - Carefully read through the Java code

---

- Keygenme-py
    - Description: keygenme-trial.py

        - This one was quite tricky for me since I don't know much about Reverse Engineering 
        - I followed this article: https://medium.com/@karimwalid keygenme-py-picoctf-reverse-challenges-series-cae76e6a8a28
        - I will need more practice with this later
        - ## "The Low Level Binary Intro playlist is a great place to start learning Reverse Engineering and Binary Exploitation."

---

- Buffer Overflow 0
    - Description: Let's start off simple, can you overflow the correct buffer? The program is available here. You can view source here. Connect using:

nc xebec.cylabacademy.net 23033

    - How can you trigger the flag to print?
    - If you try to do the math by hand, maybe try and add a few more characters. Sometimes there are things you aren't expecting.
    - Run man gets and read the BUGS section. How many characters can the program really read?

        - When you open the source code and the vuln file you learn that anything over 16 characters causes an overflow and it breaks the system, this gives you the flag
