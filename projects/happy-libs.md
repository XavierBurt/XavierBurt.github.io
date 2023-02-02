---
layout: project
type: project
image: img/mad-libs.png
title: "HappyLibs"
date: 2022
published: true
labels:
  - Python
summary: "A quick game I made in python to level-up my skills."
---

In the spirit of learning python, I coded this game.
```javascript
import random
from Colors import *

nouns = [
    "Your Mom",
    "Briana",
    "Your Doge",
    "Buttons",
    "My Computer",
    "Edward Scizzorhands",
    "The Candy-man",
    "Andrew",
    "Liam",
    "Olivia",
    "Noah",
    "Emma",
    "Charlotte",
    "The Green Arrow",
    "Charlotte's Web",
    "Elijah",
    "Hey There Delilah"
]
verbs = [
    "jumped on",
    "shitted on",
    "killed",
    "stabbed",
    "fucked",
    "squished",
    "wrestled",
    "jiggled",
    "wiggled",
    "danced with",
    "sang",
    "pencilled",
    "broke",
    "bent",
    "bought",
    "sold",
    "himself"
]
places = [
    "the outside",
    "the bathroom",
    "an island in the pacific",
    "your mom",
    "narnia",
    "the woman's bathroom",
    "school",
    "their parents house",
    "an auction house",
    "hell",
    "nirvana",
    "bullshit land",
    "a giant's mouth",
    "the quantum realm",
    "the MCU",
    "the pool",
    "a volcano",
    "space"
]
sentence_formats = {
    "1": "Remember that time when %noun% decided that %noun% %verb% %noun% in %place%?",
    "2": "It would be funny if %noun% and %noun% %verb% eachother in %place%",
    "3": "%noun% %verb% %noun% in %place%",
    "4": "I loved when %noun% %verb% %noun%"
}


def sentence_constructor(output: str):
    replace = False
    tempstr = ""
    end_of_string = False
    i1 = -1
    i2 = -1
    key = random.randint(1, len(sentence_formats))
    sentence_format = sentence_formats.get(str(key))
    while not end_of_string:
        for i, c in enumerate(sentence_format):
            if c == "%":
                if not replace:
                    i1 = i
                    replace = True
                else:
                    i2 = i
                    replace = False
                    break
            elif replace:
                tempstr = tempstr + c
        else:
            end_of_string = True
        match tempstr:
            case "noun":
                noun = random.choice(nouns)
                sentence_format = sentence_format.replace("%noun%", noun, 1)
            case "verb":
                verb = random.choice(verbs)
                sentence_format = sentence_format.replace("%verb%", verb, 1)
            case "place":
                place = random.choice(places)
                sentence_format = sentence_format.replace("%place%", place, 1)
        tempstr = ""
    output = sentence_format
    return key


message = Colors.Fg.lightblue + "Welcome to HappyLibs!"
message = message.center(225)
print(message)
message = Colors.reset + "The objective of this game is to guess what the ai put in the blanks."
message = message.center(225)
print(message)
message = Colors.reset + "For example, you might be given this sentence:"
message = message.center(225)
print(message)
message = Colors.Fg.lightcyan + "I loved when " + Colors.Fg.lightgreen + "(noun) (verb) (noun)" + Colors.Fg.lightcyan
message = message.center(235)
print(message)
message = Colors.reset + "You would fill in the green spaces, each with a different value, for example,"
message = message.center(225)
print(message)
message = Colors.Fg.lightcyan + "I loved when " + Colors.Fg.lightgreen + "your mom fucked Briana" + Colors.Fg.lightcyan
message = message.center(235)
print(message)
message = Colors.reset + "The AI will also do this, it may come up with"
message = message.center(225)
print(message)
message = Colors.Fg.lightcyan + "I loved when " + Colors.Fg.lightgreen + "your mom jumped your doge" + Colors.Fg.lightcyan
message = message.center(235)
print(message)
message = Colors.reset + "In this case, you would end up with 2 points, because you guessed 'your mom,' " \
                         "and you both got the correct noun, and you got it in the right place."
message = message.center(225)
print(message)
```
It actually utilizes a second class, Colors, which allows it to have colored UI
```
class Colors:
    reset = '\033[0m'
    bold = '\033[01m'
    disable = '\033[02m'
    underline = '\033[04m'
    reverse = '\033[07m'
    strikethrough = '\033[09m'
    invisible = '\033[08m'

    class Fg:
        black = '\033[30m'
        red = '\033[31m'
        green = '\033[32m'
        orange = '\033[33m'
        blue = '\033[34m'
        purple = '\033[35m'
        cyan = '\033[36m'
        lightgrey = '\033[37m'
        darkgrey = '\033[90m'
        lightred = '\033[91m'
        lightgreen = '\033[92m'
        yellow = '\033[93m'
        lightblue = '\033[94m'
        pink = '\033[95m'
        lightcyan = '\033[96m'

    class Bg:
        black = '\033[40m'
        red = '\033[41m'
        green = '\033[42m'
        orange = '\033[43m'
        blue = '\033[44m'
        purple = '\033[45m'
        cyan = '\033[46m'
        lightgrey = '\033[47m'
```
My implementation of this very iconic game is something I am very proud of, it is something I could add onto any time, and something that I honestly had a lot of fun making.
