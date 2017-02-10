# Span & Div

Source: http://htmldog.com/guides/html/intermediate/spandiv/

HTML is all about applying meaning to content. Whereas most HTML tags apply meaning (p makes a paragraph, h1 makes a heading etc.), the span and div tags apply no meaning at all. This might sound about as useful as a foam hammer but they are actually used quite extensively in conjunction with CSS.

They are used to group together a chunk of HTML and hook some information onto that chunk, most commonly with the attributes class and id to associate the element with a class or id CSS selector.

The difference between span and div is that a span element is in-line and usually used for a small chunk of HTML inside a line (such as inside a paragraph) whereas a div (division) element is block-line (which is basically equivalent to having a line-break before and after it) and used to group larger chunks of code.


<div id="scissors">
    <p>This is <span class="paper">crazy</span></p>
</div>

Examples
New Examples Section!
See all of this code stuff in action, and play around with it.

div, and especially span, shouldn’t actually be used that often. Whenever there is a sensible alternative that should be used instead. For example, if you want to emphasize the word “crazy” and the class “paper” is adding italics for visual emphasis, then, for richer, more meaningful content, the code might look like this:


<div id="scissors">
    <p>This is <em class="paper">crazy</em></p>
</div>

If you haven’t got a clue about classes and ID’s yet, don’t worry, they’re all explained in the CSS Intermediate Tutorial. All you need to remember is that span and div are “meaningless” tags.

While they are not replacement for the div tag, HTML 5 introduces a number of tags used for grouping blocks of code together and adding meaning at the same time. For more information on article, header, footer, and more, see the article about sectioning.


# Div and Span example

<div id="header">
    <div id="userbar">
        Hi there, <span class="username">Chris Marasti-Georg</span> |
        <a href="/edit-profile.html">Profile</a> |
        <a href="http://www.bowlsk.com/_ah/logout?...">Sign out</a>
    </div>
    <h1><a href="/">Bowl<span class="sk">SK</span></a></h1>
</div>

Ok, what's going on? At the top of my page, I have a logical section, the "header". Since this is a section, I use a div (with an appropriate id). Within that, I have a couple of sections: the user bar and the actual paghttps://www.fastcodesign.com/3038367/9-gifs-that-explain-responsive-design-brilliantlye title. The title uses the appropriate tag, h1. The userbar, being a section, is wrapped in a div. Within that, the username is wrapped in a span, so that I can change the style. As you can see, I have also wrapped a span around 2 letters in the title - this allows me to change their color in my stylesheet.

Also note that HTML5 includes a broad new set of elements that define common page structures, such as article, section, nav, etc. Section 4.4 of the HTML 5 working draft lists them, and gives hints as to their usage. HTML5 is still a working spec, so nothing is "final" yet, but it is highly doubtful that any of these elements are going anywhere. There is a javascript hack that you will need to use if you want to style these elements in some older version of IE - you basically need to create one of each element using document.createElement before any of those elements are specified in your source. There are a bunch of libraries that will take care of this for you - a quick Google search turned up html5shiv.
