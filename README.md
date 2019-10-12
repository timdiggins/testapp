# Demo of Bug in Thredded

This repo shows a demo of an unusual bug apparently caused by thredded.

If you comment out the thredded gem, you will see the index page shows Part 1, Part 2, and Part 3 all horizontally together on desktop. If you shorten your browser window, they will change into three lines.

This is because it's set up with the pure css grid framework to be class "pure-u-1 pure-u-md-1-3"

However, once you include the thredded gem, this behavior inexplicably breaks.

Working as Intended:
(the Part 1 | Part 2 | Part 3 are shown on three different lines when your browser width is small, e.g. on mobile; note that they should show up on the same line on desktop... by giving them the class name "pure-u-1" AND "pure-u-md-1-3" we are stating we want a responsive design where it changes from desktop to mobile)

![Working as Intended](https://raw.github.com/pickhardt/testapp/master/working-as-intended.png)

Bug:
(the Part 1 | Part 2 | Part 3 are still shown on the same line)

![Bug](https://raw.github.com/pickhardt/testapp/master/bug.png)

For some unknown reason, simply including the thredded gem will cause this behavior flip.
