# Snap scroll carousel

"Classical" carousels huge libraries could be easily replaced by native scroll functionality
 - that would contribute to grater UX, better performance and progressive enhancement practice.

You probably know that scroll is very complex functionality that very hard to implement without access to native OS API. 
That's why native scroll is more comfortable for the user (on modern desktop and mobile) than any point-and-click functionality.

## CSS snap points

But in classical "carousels", you are expected some snapping of scrolling. 
And it could be done with CSS. 

It has been 3 years or so when this API available for browsers. 

* [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/scroll-snap-type)
* [W3C v1](https://www.w3.org/TR/2015/WD-css-snappoints-1-20150326/)
* [W3C v2](https://www.w3.org/TR/css-scroll-snap-1/)
* [Caniuse](https://caniuse.com/#feat=css-snappoints)

## Features

* Progressive enhancement, basic funtionality available without JS
* Responsive
* LTR and RTL directions support
* Plays well with dynamic content
* AAA ARIA accessibility (focus of elements and visibility for AT)
* Could be controlled from keyboard (tab, arrows), mouse, touch etc. without any JS logic (Chrome has bug with arrows navigation)
* Scroll up to all elements, not just 1 at the time

### Infinite scrolling

It is hard to explain why this marquee-like pattern even needed in carousels.

Since carousels mostly represents large lists user should have feels of extremes of the list.
For that type of content more important good browsing UX than "auto scrolling".

## Browser compatibility

As progressive enhancement supports in every browsers from Netscape navigator 1.0 to latest Firefox.

Progressive enhancement and graceful degradation: 

1) if no JS available it would be just native scroll;
2) if scroll snap CSS API available it would be snapped to declared values;
3) if JS and snap scroll available than user will have Buttons and pagination functionality improvements over native scroll.

With polyfill tested:

* FF (68.0), Chrome (75.0.3770.142) Linux
* FF (68.0), Chrome (75.0.3770.142) MacOS

Note! Each OS and OS preferences resulted on different, but always familiar scroll behavior.

Safari 12.1.1 not work smooth scroll (could be polyfiled)
Edge not work smooth scroll
11 not work smooth scroll

## License

MIT D.Nechepurenko 2020
