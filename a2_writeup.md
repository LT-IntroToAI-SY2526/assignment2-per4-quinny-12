# Assignment 2 - Write UP

## Description
This assignment is about learning and applying the while loop and iterating through multiple lists at a time.  We also will discuss how we match things in chatbots in order to extract what a user is trying to find.  Next assignment we will work with data bases and how we can extract information from them.

## What to complete
1. Go through the notes.py file w/ Mr. Berg
2. Complete `a2.py`, Mr. Berg will walk everyone through the process
3. Make sure you pass all asserts in `a2.py`
4. Complete the reflection problems below
5. Push your code to github for grading

## Reflection Questions
1. What was difficult for you while completing the match function?

The hardest part of the match function was understanding how the two pointers (pind and sind) move through the pattern and source lists at the same time. The % wildcard was especially tricky because it can match multiple words, so I had to figure out how to look ahead in the source list to find where the next pattern element shows up. It was also difficult to handle all the different situations that could happen, like what to do when we reach the end of one list but not the other, or when % needs to match zero words. Keeping track of when to move each pointer forward and when to return None was confusing, and it was hard to visualize what the code was actually doing as it ran.

2. Explain how you could use the match function for extracting information from a movie database.

The match function could help build a system where users can ask questions about movies in normal English instead of typing complicated database commands. For example, if someone types "who directed The Dark Knight," you could use the pattern ["who", "directed", "%"] to match their question and pull out "The Dark Knight" as the movie they're asking about. Then you'd search your database for that movie's director. Another example would be the pattern ["what", "movies", "did", "_", "direct"] matching "what movies did Steven Spielberg direct" and extracting "Steven Spielberg" to find all his movies. By creating several of these patterns for different types of questions, the system could figure out what the user wants to know and grab the important information (like movie titles, actor names, or years) to search the database and give them an answer.
