---
title: Hyperlinks
layout: titled
---

`terminalpp` supports both automatic detection of hyperlinks in the terminal text *and* explicit hyperlink definition using the `OSC 8` escape sequence (as discussed for instance [here](https://gist.github.com/egmontkob/eb114294efbcd5adb1944c9f3cb5feda)).

Clicking on the hyperlink either opens it in default browser (left button), or copies the url to clipboard (right button). Note that in case of the explicit hyperlink sequences the displayed text can differ from the actual url. 

# Configuration

Both automatic detection and ansi sequence hyperlinks can be turned or on off via the `sequences.allowOSCHyperlinks` and `sequences.detectHyperlinks` respectively. 

The visual appearance of the hyperlinks can be specified in the `renderer` settings for normal and active (with mouse over) hyperlinks. Font atrributes, foreground and background colors are supported. 

For more details see [configuration](configuration.html).
