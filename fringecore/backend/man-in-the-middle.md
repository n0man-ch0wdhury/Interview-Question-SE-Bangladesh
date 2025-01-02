# Man-In-The-Middle

[Watch the video](https://www.tella.tv/video/man-in-the-middle-e2u1)

<aside>
💡

This challenge was solved by one of our engineers internally.

1. It took ~50 minutes.
2. It was all in one file.
3. Our solution file is 58 lines long.

</aside>

# Environment

1. You definitely need NodeJS version >=20 such that you can run .mjs files directly.
2. Linux environments preferable. WSL2 for Windows might work too.

# How It All Started

Secure messages exchanged between two individuals, Faisal and Monjur, were intercepted, but the encryption and protocol used are custom and complex.

### Encryption Details:

- The encryption keys are 8 bytes long.
- Each message is encrypted with a different key using just XOR.
- Messages include the sender's username in lowercase, appended as a prefix with a colon, e.g., faisal:hello.
- Messages are padded with newlines (\n) to ensure the total length is a multiple of 7 bytes.
- After padding, the message is split into groups of 7 bytes, and an index byte is prepended to each group, turning them into 8-byte blocks.
- All groups, except the first, are shuffled randomly.
- Each group is then encrypted and Base64 encoded.
- Faisal initiates the dialogue.

# What To Build

1. Write a Node.js program to decrypt and reconstruct the original messages to uncover the content of their communication.
2. Your program should write a file named decrypted.json with all the messages in an array.

# Details

1. Each array in `dump.json` is a message (total 20 messages).
2. Definitely watch the video for more information.
3. Do not use any external libraries.
4. DO NOT modify/create any other file other than challenge.mjs.

# Let’s Start

1.  **Clone Repository:**

    `git clone git@github.com:fringecore/fringecore-backend-challenge-man-in-the-middle.git`

2.  **Navigate to Directory:**

    `cd fringecore-backend-challenge-man-in-the-middle`

3. **Open your favorite code editor (like VSCode for example):**

    `code .`

4. **Run challenge.mjs after completing:**

    `node challenge.mjs`

HAPPY CODING! 🎉

# Partial

Just know that we fully understand that these challenges are actually pretty tough. Hence it is surely not an all-or-nothing evaluation scheme. If you hit any of the features below you’re doing great. Every time you achieve one of these points, pat yourself on the back.

1. You have started the challenge.
2. You are able to read the encrypted chunks.
3. You are able to decrypt some of the messages.
4. You decrypted all messages but not ordered correctly.

# Submission

1. First add the fringecore remote repository:
    
    `git remote add fringecore ssh://submission.fringecore.sh/<applicant_id>/fringecore-backend-challenge-man-in-the-middle`
        > **Note:** Your application_id is case sensitive.

2. Then just push into it:
    
    `git push fringecore main`
    
You may see a warning like "The authenticity of host '[submission.fringecore.sh](http://submission.fringecore.sh/) (xx.xx.xx.xx)' can't be established," just type yes and press enter to continue.


