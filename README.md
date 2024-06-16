# Trivia bot in BCFD
This repo is a template of a trivia bot made in BCFD. Feel free to copy and use this script anywhere you want.

If you want to add these commands, do these steps:
1. Create 3 commands: q?gen, q?ans, q?help (feel free to change the prefix)
2. Set command type to "Import"
3. Paste JSON

There are only 14 questions in this version. I'll add more by time, but here is how you can create your own questions. Find "var questions" in your q?gen command. This is where questions are stored. If you want to create a question, add square brackets `[]` and feel it like this: `["What's 1+1?", "1", "2", "3", "4", 2, noimage]`.

You probably don't know anything about programming, so I'll try to make it simple.

The whole square brackets thing is called an array. An array is filled with elements (example: "What's 1+1?" or "1"). Elements are separated with commas. And that makes one single question.

Let's do the whole question stated upper step by step. Type two square brackets `[]`.

The first element ("What's 1+1?") is a question. This element MUST be in quotation marks (""). Now we have: `["What's 1+1?"]`.

The second, third, fourth and fifth elements ("1", "2", "3", "4") are answers. You don't have to always put 4 answers. If you want to have 2 answers, just do this: `["What's 1+1?", "1", "2"]`. These elements MUST be in quotation marks as well. Let's say we want to have 4 answers. Now we have `["What's 1+1?", "1", "2", "3", "4"]`.

The next element is the number of the correct answer. If the first answer is correct, write `1`. If the second answer is correct, write `2` and so on. DO NOT put quotation marks here. Now we have: `["What's 1+1?", "1", "2", "3", "4", 2]`.

The last element is a question image link. This is an image that should appear with the question. If you want to have an image, copy the image link and **put it inside quotation marks** like this: `"https://i.imgur.com/Qkum1e9.png"`. If you don't want to use any image, just type `noimage` **without quotation marks**. Let's say we don't want to use any image. Now you have completed your first question: `["What's 1+1?", "1", "2", "3", "4", 2, noimage]`.

Now we have to include it in the questions array. It looks something like this:
```
var questions = [
    [question 1...],
    [question 2...],
    [question 3...]
]
```
It stores every question in the bot. To apply your question, do this:
```
var questions = [
    [question 1...],
    [question 2...],
    [question 3...], <--- ADD A COMMA!
    [your question...]
]
```

I hope you understand this a little bit. If you have any question about this, feel free to ping me in the official BCFD server and I'll gladly explain it to you more closely. :)
