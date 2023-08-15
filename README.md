Describe: wordCounter()

Test: "It should return 1 if a passage has just one word."
Code:
const text = "hello";
wordCounter(text);
Expected Output: 1

Test: "It should return 2 if a passage has two words."
Code:
const text = "hello there";
wordCounter(text);
Expected Output: 2

Test: "It should return 0 for an empty string."
Code: wordCounter("");
Expected Output: 0

Test: "It should return 0 for a string that is only spaces."
Code: wordCounter("            ");
Expected Output: 0

Test: "It should not count numbers as words."
Code: wordCounter("hi there 77 19");
Expected Output: 2


Describe: numberOfOccurrencesInText()

Test: "It should return 0 occurrences of a word for an empty string."
Code:
const text = "";
const word = "red";
numberOfOccurrencesInText(word, text);
Expected Output: 0

Test: "It should return 1 occurrence of a word when the word and the text are the same."
Code:
const text = "red";
const word = "red";
numberOfOccurrencesInText(word, text);
Expected Output: 1

Test: "It should return 0 occurrences of a word when the word and the text are different."
Code:
const text = "red";
const word = "blue";
numberOfOccurrencesInText(word, text);
Expected Output: 0

Test: "It should return the number of occurrences of a word."
Code:
const text = "red blue red red red green";
const word = "red";
numberOfOccurrencesInText(word, text);
Expected Output: 4

Test: "It should return a word match regardless of case."
Code:
const text = "red RED Red green Green GREEN";
const word = "Red";
numberOfOccurrencesInText(word, text);
Expected Output: 3

Test: "It should return a word match regardless of punctuation."
Code:
const text = "Red! Red. I like red, green, and yellow.";
const word = "Red";
numberOfOccurrencesInText(word, text);
Expected Output: 3

Describe: swearFilter();

Test: "It should return a blank string."
Code:
const text = "a";
swearFilter(text);
Expected Output: ""

Test: "It should return a blank string if passed in a zoinks -- a swear word."
Code:
const text = "zoinks";
swearFilter(text);
Expected Output: ""

Test: "It should return a string with a word removed, if passed in a string with two words."
Code:
const text = "oh zoinks";
swearFilter(text);
Expected Output = "oh";

Test: "It should return a string with bad words removed, if passed in a string containing three words."
Code:
const text = "oh zoinks water";
swearFilter(text);
Expected Output = "oh water";

Test: "It should return a string with 2 of the same bad words removed, if passed in a string."
Code:
const text = "oh zoinks water zoinks buffalo"
swearFilter(text);
Expected Output = "oh water buffalo";

Test: "It should return a string with 1 bad word from a selection of 2 bad words, if passed through a string.:
Code:
const text = "oh muppeteer water";
swearFilter(text);
Expected Output = "oh water"