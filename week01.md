# Week 1 - Hello World!

I woke up on Monday morning nervous about being able to keep up and hold my own during class. Before DigitalCrafts, I had blown through a couple free trials of Codecademy, but other than some time spent on the pre-work, I had zero experience coding. I was battling imposter syndrome before even starting the class and was contemplating backing out of the program. Thankfully, I was able to push those thoughts aside for a bit and show up for the first Zoom meeting. There was a bit of information overload the first few days, but I loved that we started working with python and solving problems with code from the get-go. Needless to say, I’m here to stay! I can’t wait to learn everything I can about coding! 

## Highlights of the Week:
Aside from feeling like I’ve conquered my terminal (or at least understand it), the best part of the week was tackling python exercises on my own and with classmates. I spent a little too long on one particular exercise: making a phonebook app. This exercise required you to take entries and store them in a dictionary, as well as look up entries and delete them. For my first attempt, I stuck with the names provided and was able to make a working program with those names. However, I wasn’t sure how to add new entries or what to do with names that weren’t already in my dictionary. Take a peep at my first attempt below: 


### My First Attempt:
```python
catalog = {
    "Igor" : "859-485-2935",
    "Jazz" : "334-584-2345",
    "Melissa": "584-394-5857",
    
}

program_end = True

while program_end == True:
    print("Electronic Phone Book \n")
    print("======================")
    print("\n 1. Look up an entry \n 2. Set an entry \n 3. Delete an entry \n 4. List all entries \n 5. Quit")
    user_input = int(input("What do you want to do? Pick a number from 1 - 5: "))
    #Look Up an Entry
    if (user_input == 1):
        name_selection = int(input("What name would you like to look up? Enter a number 1 -3: \n 1. Igor \n 2. Jazz \n 3. Melissa \n"))
        if (name_selection == 1):
            print(catalog["Igor"])
        elif name_selection == 2:
            print(catalog["Jazz"])
        elif name_selection == 3:
            print(catalog["Melissa"])
        else:
            print("Please type a number from 1 -3.")
```

After an evening Zoom call with a couple of classmates, I felt inspired to take another stab at this exercise and make my app better. I got the idea from a classmate to use an empty dictionary to hold new additions to the phonebook. I kept my same while loop format but swapped out all the if statements involving specific names, with statements that would work regardless of what the user typed in. I’m much happier with this version of my app but, it is far from perfect or even where I want it to be. As of right now, the app cannot store more than one name and number. This is a major flaw, but one I’m willing to look past and pat myself on the back for since it’s only my first week! Here’s a snippet of my second attempt:

### My Second Attempt:

```python
catalog = {}
program_stop = True


while program_stop == True:
    print("\n Electronic Phone Book \n")
    print("======================")
    print("\n 1. Look up an entry \n 2. Set an entry \n 3. Delete an entry \n 4. List all entries \n 5. Quit")
    user_input = int(input("What do you want to do? Pick a number from 1 -5: "))
    #Look up an Entry:
    if (user_input == 1):
        name_selection = input("Who would you like to look up? ")
        if (name_selection == catalog["user_name"]):
            print(catalog["user_name"] + " " + catalog["user_number"])
        else:
            print("Sorry, we don't have someone with that name in our database.")
    # Set an Entry:
    if (user_input == 2):
        user_name = input("Enter your name: ")
        user_number = input("Enter your phone number: ")
        catalog["user_name"] = user_name
        catalog["user_number"] = user_number
        print("You have added an entry for %s with the phone number: %s." % (catalog["user_name"], catalog["user_number"]))
```