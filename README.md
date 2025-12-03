---
title: Phone Number Search-Linear Search
emoji: 🐠
colorFrom: yellow
colorTo: red
sdk: gradio
sdk_version: 6.0.1
app_file: app.py
pinned: false
short_description: Stores phone numbers saved to names in a database.
---

# Phone Number Search – Linear Search 🐠



## Hugging Face Link
https://huggingface.co/spaces/Endreuz/Phone_Number_Search-Linear_Search


## Author & Acknowledgment
Author: Andrew Zhang  
Course: CISC-121  


## Steps to Run Algorithm

1. Clone the repository or download the files.
2. Install dependencies:
   pip install -r requirements.txt
3. Run the app:
   python app.py
4. Wait for Gradio to start and open the local link.
5. Use the interface to add, search, or remove phone numbers.


## Testing and Verification

1. With the search function, if given wrong name, Result box will tell the user that the inputted name is not found in the notebook.
2. With the add function, if only given a number, Result box will prompt the user to enter a name and a number. Same happens if the user only gives a name.
3. With the remove function, if given the wrong name, Result box will tell the user that the inputted name was not found and removed nothing from the phonebook.
4. With the add function, if given an input that is not only ten numbers, Result box will prompt the user to only input ten digits with no dashes.
5. Confirmed search function will return saved phone number when an existing name is entered.
6. Confirmed add function will add a new contact when a valid name and number is inptuted.
7. Confirmed that the remove function deletes the inputted contact when an existing name is inputted.
8. Confirmed that when database is ran, will display all contacts.
9. Confirmed that when saved, will save database and if page is refreshed, will still have contacts in the database.






## Linear Search

Linear search, also known as sequential search, is a searching algorithm that iterates through an array one by one, in sequential order, until it finds the target element,
or the end of the array is reached.


## The problem I'm solving is keeping track of phone numbers with names.

The input when adding a new phone number is a name and then the phone number.
When searching for the phone number, the input is a name, and then the output is the phone number.

## The user should interact with this app by using a browser.



## Decomposition:
First, get the input from the user of what they want to do. Search, add or to remove from the database.
If choose to search, prompt the user to give a name.
When given name, parse through the dictionary for the given name key.
If the compared value matches the target, return back the value of the key.
If choose to add, prompt for 2 inputs separately.
The first prompt is the name
The second prompt is the phone number with dashes between.
Both are added to the end of the dictionary in the form of “key : value”.
If choose to remove, prompt the user to give a name.
When given a name, parse through the dictionary for the given name key.
If the compared value matches the target, remove the key and value from the dictionary.

## Pattern Recognition:
“Compare and if not target, look at next,” step repeats for every contact until it finishes the list, or it finds the target.
The structure of name then phone number repeats for every data entry

## Abstraction:
Users are asked what they want to do, and when they choose an option, are given different prompts for inputs. When these inputs are given, the dictionary is either parsed through to find a key, or it is shortened or lengthened by one.
Algorithm Design:
Input: “add”
Example input: “Connor”
Example input: “416-423-4361”
Processing: Name and Input added to dictionary in {“Connor” : “416-423-4361”} format.

Input: “search”
Example input: “Connor”
Processing: Parse through the dictionary, searching for the target string key.
Example output: “416-423-4361” or, if did not find target string key, return string explaining no instances of “Connor”

Input: “remove”
Example input: “Connor”
Processing: Parse through the dictionary, searching for the target string key. If target string was found, remove the key and value from the dictionary
Example output: “416-423-4361 was deleted” or, if did not find target string key, return string explaining no instances of Connor to remove


## Why I chose to do linear search

I chose to do linear search for this project mainly because I wanted to make a search algorithm in python for a phone number storing system.
It’ll be a dictionary based searching system where we have a name as the key, and then a phone number that is the value.




## How my algorithm works:
My search function iterates through the database of saved names. For each iteration, there is an if statement to see if the current name being iterated is the target name.
If it is, it returns the name and the phone number, but if it isn't, it simply continues to the next iteration. If the entire for loop continues without returning a single name,
then a return statement automatically is run that says the name is not found in the notebook.

[![Watch the video](https://img.youtube.com/vi/r6cz6fZQC1s/0.jpg)](https://www.youtube.com/watch?v=r6cz6fZQC1s)



Check out the configuration reference at https://huggingface.co/docs/hub/spaces-config-reference
