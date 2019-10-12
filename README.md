# Demo of Bug in Thredded

This repo shows a demo of an unusual bug apparently caused by thredded.

If you comment out the thredded gem, you will see the index page shows Part 1, Part 2, and Part 3 all horizontally together on desktop. If you shorten your browser window, they will change into three lines.

This is because it's set up with the pure css grid framework to be class "pure-u-1 pure-u-md-1-3"

However, once you include the thredded gem, this behavior inexplicably breaks.

Working as Intended:
![Working as Intended](https://raw.github.com/pickhardt/testapp/master/working-as-intended.png)

Bug:
![Bug](https://raw.github.com/pickhardt/testapp/master/bug.png)
