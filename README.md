Smart Password Generator

Overview
People often struggle with passwords that are tough to remember but not very secure. This tool helps fix that issue. It draws from the XKCD comic number 936 on password strength. The generator makes strong and memorable passwords. It combines words from dictionaries and adds security tweaks. You get passwords that stick in your mind without being easy to crack.

Features

Core Functionality
The tool lets you generate multiple passwords all at once in one run. It builds them from word combinations pulled from dictionaries. Those make the passwords memorable and still secure enough. You can tweak settings like how many words to use per password. Decide on the number of passwords to create. Set limits on word lengths too. For extra security, turn on l33t speak substitutions. Mix up the case randomly if you want. Results stay the same each time if you use a seed for randomization.

Advanced Options
Load words from more than one dictionary file at a time. Combine them for variety. Filter the words to keep only those between certain lengths. Apply l33t changes to swap letters for numbers or symbols. Add that ransom note style with random upper and lower case letters. Check out stats on your word lists. See sample words and counts to get a feel for what is available.

Technologies Used

Programming Language
It runs on Python version 3.8 or newer.

Core Libraries
Argparse handles the command line setup. Random module does the secure picking of words. Re library cleans up text and processes patterns. String module works with characters for changes.

Platform
The whole thing works across different systems. That includes Windows, macOS, and Linux without issues.

Installation

Prerequisites
You need Python 3.8 or a higher version installed. Know your way around basic command line stuff.

Setup Steps
First, grab the project files by cloning or downloading them. Make sure Python is set up on your machine. That is all you need. It sticks to the standard library, so no extra installs required.

Usage

Basic Examples

Generate 5 passwords with 4 words each.
Run this command, python password_maker.py nouns.txt adjs.txt -n 5 -w 4.

Generate passwords with l33t transformation.
Try python password_maker.py nouns.txt verbs.txt -l -n 3 for that.

Show word list statistics.
Use python password_maker.py dictionary.txt --stats to see them.

Command Line Options
The option --num or -n sets how many passwords to make. Default is 5. --words or -w picks the number of words in each password. Default sits at 4. --min-len or -m controls the shortest word allowed. It defaults to 3 letters. --max-len or -x sets the longest word. Default is 6. --l33t or -l turns on those character swaps. It defaults to off. --seed or -s gives a number for repeatable results. No default there. --stats shows details on the word lists. Defaults to false.

Advanced Usage

Reproducible password generation.
For consistent outputs, run python password_maker.py nouns.txt adjs.txt verbs.txt -n 10 -w 3 -l -s 12345.

Custom word length range.
To limit words between 4 and 8 letters, do python password_maker.py dictionary.txt -m 4 -x 8 -n 5.

Multiple dictionary files.
Combine several like python password_maker.py adjs.txt nouns.txt verbs.txt places.txt -n 3.

Project Structure
The main folder is smart-password-generator. Inside src, you find password_maker.py as the key script for generating passwords. There are word lists too, like adjs.txt for adjectives. Nouns.txt holds nouns. Verbs.txt covers verbs. Requirements.txt lists any dependencies, though it uses mostly standard stuff. The tests folder has test.py for integration checks. Unit.py runs unit tests. Docs contains project_report.pdf with full details. README.md is this document. Statement.md outlines the problem and scope.

How It Works

Password Generation Process
It starts by reading dictionary files and pulling words together. Cleans them up by stripping non-letter characters and fixing case. Filters based on length limits you set. Picks words at random to match your count. If you enable transformations, it applies l33t and case mixes. Finally, it shows the passwords. Includes hints on their strength.

Security Features
Instead of random letters, it uses word combos that you can remember. L33t swaps make them harder to guess by replacing letters with look-alikes. Random case adds more variety without much effort. It can tack on punctuation at the end for extra strength.

Testing

Running Tests
To run unit tests, type python tests/unit.py. For integration, use python tests/test.py. Do both with python tests/unit.py && python tests/test.py.

Test Coverage
Tests check word cleaning and validation steps. They cover the logic for building passwords. Security changes get tested too. Error handling for odd cases is included. The command line parts are verified.

Contributing

Adding New Features
Fork the repo to start. Make a branch for your feature. Code your additions there. Write tests to cover the new parts. Send a pull request when ready.

Reporting Issues
Post on the GitHub issue tracker. Mention your Python version and OS. Give clear steps to repeat the problem.

License
This project stays open source under the MIT License.

Contact

Developer
Prince Tiwari.

Institution
VIT University BHOPAL.

Course
CSE CYBERSECURITY AND DIGITAL FORENSICS.

Academic Year
2025-2029.

Academic Context
The project came from a Build Your Own Project assignment. It shows real-world use of programming ideas. That covers command line building. File input and output operations. Text handling with regular expressions. Generating random numbers securely. Testing methods for software. Organizing and documenting projects properly.

Security Notes
Passwords show up in the terminal only. They do not get saved anywhere. Use unique ones for each service. A password manager helps store them safely. Update sensitive account passwords now and then.

Performance
It handles thousands of words without slowing down. Memory use stays low overall. Even big dictionary files run fast. Algorithms are tuned for quick results.

Note
This tool suits educational and personal needs. For serious stuff, go with proven password managers. They add more security layers.