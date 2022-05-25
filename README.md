# Substring-Method(The Summary)
Hello again! For this project I had to create a program that would take a string of words and a predefined dictionary, the program would then take every entry from the dictionary and scan the string of words to see if there was a substring that matched the dictionary entry, and how many times it appeared. Once this was done it would add the dictionary entry as a key to an empty hash and the value to this key would be how many times the substring appeared.

This one honestly stumped me quite a bit, I had to do a little bit of research and even try to break down some other peoples code and try to understand what they were doing. This lead me to discovering a wonderful string method called scan which I'll touch on in a bit.

Some of the challenges I faced initially when trying to figure this one out was how to compare the string that the user would input to an existing array of words, and checking the input string for substrings. Also outputting this data to a hash with k/v of 
"substring"/# of appearances.

When I first saw the scan method being used it didnt make much sense to me and then I realized after quite awhile of reading that it's unbelievably useful. It does many things all at once, it can take a whole string and literally scan every word indiviudally looking for a given combination of letters, if it's not found it just moves onto the next word. If it is found, it will begin to create an array that holds every instance of that combination of letters appearing.

This ended up being the only thing I needed to solve this problem. I was able to iterate over the dictionary array, and for every word in the dictionary I scan the given string for a match, if there is a match then I count the instances of matches and save that to a variable then create a new key in the empty hash with the word currently being used to scan the string, and set its value to the number of matches that I saved in a variable.