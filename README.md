# fibonacci
Let's generate Fibonacci numbers! [Run the program in your browser](http://htmlpreview.github.io/?https://github.com/joeltornatore/fibonacci/blob/master/fibber.html)!

Jeffery and I were exploring Fibonacci numbers, and decided to write a
program to generate them. The first two Fibonacci numbers are 0 and 1,
and every successive number is calculated by summing the previous two.
So the sequnce starts like this:
* 0
* 1
* 1 (= 0 + 1)
* 2 (= 1 + 1)
* 3 (= 1 + 2)
* 5 (= 2 + 3)

Wikipedia has a great page describing Fibonacci numbers. You can read
it [here](https://en.wikipedia.org/wiki/Fibonacci_number).

YouTuber [Vi Hart](https://www.youtube.com/channel/UCOGeU-1Fig3rrDjhm9Zs_wg)
has a great three-part video series on the occurance of
Fibonacci numbers in plants. You can find them here:
* [Part one](http://youtu.be/ahXIMUkSXX0)
* [Part two](http://youtu.be/lOIP_Z_-0Hs)
* [Part three](http://youtu.be/14-NdQwKz9w)

---

Our program is very simple. It displays a blank page with three buttons:
one pops up our silly copyright text (just for fun!), one redirects
you to github to see this file, and one that calls the _fibber_
function. That's where the actual work is done.

The fibber function does the following:
* Prompts for how many Fibonacci numbers to generate. We make sure you
entered a real number (instead of words or random characters) by
calling the [_parseInt_](https://www.w3schools.com/jsref/jsref_parseint.asp)
function. It returns _NaN_ (Not A Number) if you entered text that was
not a number. In that case, we will generate _default_how_many_
Fibonacci numbers. We also check that you don't ask for too few or too
many. The minimum you can do is two, and most is 1478. Try more to
see what happens!
* We initialize our _fibs_ list to 0 and 1, the first two in the series.
* We generate the rest of the numbers by adding the two previous numbers
and _pushing_ that sum onto the end of the _fibs_ list. We do this
_count - 2_ times, which seems like it would be two fewer than
requested, but we initialized the list with the first two numbers so it
works out.
* The numbers get printed by updating the _output_ HTML element. We
[_join_](https://www.geeksforgeeks.org/javascript-array-join-method/)
 each of the numbers in our list with the line break element, so there
is one per line.

---
This was a fun little project for both of us. Let's do more!
