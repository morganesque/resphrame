resphrame
=========

Yet another little floating iframe responsive web design testing thing.

[Take a spin](http://morganesque.github.io/resphrame/)

<small><small>* the name's awful I know, it kind of made me laugh how awful it was when I thought of it ... so I kept it ;-)</small></small>

### Background ###

So yeah... Brad Frost (with help no doubt) has collected a wonderful [list of responsive testing tools](http://bradfrost.github.io/this-is-responsive/resources.html#testing) which I've searched through and which mostly I'm really impressed with. But I could never remember which were the ones I liked the best so I ended up writing a kind of précis of all of them (see other_tools.txt in this repo) so I could quickly find the one I remembered using last. 

As I was doing that I realised that there were some feature patterns which emerged (some which I liked and some which were clearly aimed at different use-cases). Also none of them had that combination of all the features I wanted...

### So I built my own ###

Here's a few things about it.

* **Width only** &mdash; I'm not saying height isn't important or shouldn't be considered, but from experience when I'm creating a site I want to control the width but see as much height as possible. Boom.

* **Minimum chrome** &mdash; For the most part I don't want to look at a string of buttons or options and especially as I'm most on a laptop all space is at a premium.

* **Draggable** &mdash; The main interaction therefore is via a draggable handle which you can use to make the viewport smaller and larger. This is because mainly that's what I tend to do during work. I don't want to see static iframes showing me different devices, it's about watching the design as it grows and shrinks and seeing where the problems arise.

* **Viewport size** &mdash; Also when those problems appear I want to know exactly what size viewport I'm at. That's why the width is in the handle itself. At that point that’s all I want to know before I switch back to my CSS and add a media query.

* **Sharable** &mdash; Both a) the **website** I'm testing, and b) the **current width** are stored in the URL (via `history.pushstate`) and so at any point I should be able to just grab that URL, wang it in Skype and show someone else what I'm seeing.

* **Typed widths** &mdash; This also means that setting an exact numeric width is just a matter of hacking the URL (less chrome!).

* **Device presets** &mdash; Instead of having buttons for preset device sizes I've just included little _markers_ in the background which the draggable handle will snap to. You can change the placement of these in the comma-delimited list (on the left).

* **Randomiser** &mdash; Also if you remove the `#320` number from the URL but leave a web address it'll automatically give you a random width.

* **Refresh** &mdash; Many times when I'm working with these things (especially the bookmarklet ones) I edit some code and switch back to my browser and without thinking hit `CMD+r` to refresh. For tools which are bookmarklets this totally trashes the testing, for tools which don't cache the state in the URL you're back to some default viewport size you aren't testing right now. So for this I've grabbed the keystrokes `CMD+r`, `CTRL+r` and `F5` and funneled them into the iframe so only that refreshes _(Nb. it doesn't quite work perfectly so a quick double press should have the whole thing refresh for you - which is enough to catch the instinctive, muscle-memory stuff but doesn't exactly lock you out of your compter!)_.

### Caveats ###

In case you haven't picked it up this is very much directed at me and how I work. It won't suit everyone. Also I can totally see the need for having device sized viewports for showing your boss what the website will actually look at on different popular devices. That's not what I'm trying to provide for.

p.s. I've just built this very quickly today so it's working in Chrome 26. If it looks like anyone else is interested I'll do some more testing (or you can!) and get it working more widely.

### To Do ###

* Make it measure in ems. I tend to use ems in media queries but I'm a little warey of just doing `width/16` so I need to look into it I think.