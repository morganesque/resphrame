resphrame
=========

Yet another little floating iframe responsive web design testing thing.

<small><small>* the name's awful I know, it kind of made me laugh how awful it was when I thought of it ... so I kept it ;-)</small></small>

### Background ###

So yeah... Brad Frost (with help no doubt) has collected a wonderful [list of responsive testing tools](http://bradfrost.github.io/this-is-responsive/resources.html#testing) which I've searched through and which mostly I'm really impressed with. But I could never remember which were the ones I liked the best so I ended up writing a kind of précis of all of them (see other_tools.txt in this repo) so I could quickly find the one I remembered using last. 

As I was doing that I realised that there were some feature patterns which emerged (some which I liked and some which were clearly aimed at different use-cases). Also none of them had that combination of all the features I wanted...

### So I built my own ###

Here's a few things about it.

* I've tried to keep chrome to a minimum. Mostly you don't want to look at it and especially as I'm on a laptop all vertical space is valuable.

* The main interaction therefore is via a draggable handle which you can use to make the viewport smaller and larger. This is because mainly that's what I tend to do during work. I don't want to see static iframes showing me different devices, it's about watching the design as it grows and shrinks and seeing where the problems arise.

* Secondly when those problems come I want to know exactly what size viewport I'm at. That's why the width is in the handle itself. At that point that’s all I want to know.

* Both the website I'm looking at and the current width are stored in the URL (via history.pushstate) and so at any point I should be able to just grab that URL, wang it in Skype and show someone else what I'm seeing. This also means that setting an exact numeric width is just a matter of hacking the URL.

* Instead of having buttons for preset device sizes I've just included little markers in the background which the draggable handle will snap to. You can change the placement of these in the comma-delimited list (on the left).

