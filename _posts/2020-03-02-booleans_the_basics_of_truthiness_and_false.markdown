---
layout: post
title:      "Booleans, the basics of truthiness and false"
date:       2020-03-02 18:22:41 +0000
permalink:  booleans_the_basics_of_truthiness_and_false
---

Boolean values come in handy in programming when we want to implement control flow. Control flow is the idea that we can tell our program to execute certain lines of code based upon certain conditions.
In ruby only false and nil are FALSEY, everything else is truthy.

```
def age
      if age < 2
   "baby"
else
   "not a baby"
end
```

true and false methods can be a numerous amount of things, including **OR/||**, **if/else**, the modulo operator **%**(this checks if a number you are calling is divisible by a number assigned EX.  i % 4 == 0.

for a more official definition of what a Boolean is refer to this article: [(https://www.techopedia.com/definition/5495/boolean)]

the great thing about Booleans is that you don’t always have to define a truth or false to them.
```
def method
      if input == 3
			true
end
```

basically, what this will do is return true if your input is a 3. every other input will return false without having to code in
```
else
false 
```

this was just a short rundown on Booleans i hope you found it useful!

