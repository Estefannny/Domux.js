# Domux

Domux is a simple DOM manipulation library.

## Documentation

Manipulates HTML in the DOM. Also just returns the inner HTML of elements in the collection if called with no arguments.

html
----
	
	### syntax ###

		d$( selector ).html( html ,location );

	or this method will accept just a HTML fragment with a default behavior of inner:

		d$( selector ).html( html );

	or you can use shorthand syntax by using the location name argument as the function name:

		d$( selector ).outer( html );
		d$( selector ).before( html );
	
	or you can just retrieve the inner HTML of elements in the collection with:
	
	    d$( selector ).html();

	### arguments ###
	
    - html `String` is a string of HTML markup or a `HTMLElement`.
	- location `String` can be one of: _inner_, _outer_, _top_, _bottom_, _remove_, _before_ or _after_.

	### example ###

		d$('#foo').html('<strong>rock and roll</strong>','inner');
		d$('#foo').html('<p>lock and load</p>','outer');
		d$('#foo').html('<div>bangers and mash</div>','top');
		d$('#foo').html('<em>mean and clean</em>','bottom');
		d$('#foo').html('<p>some warmup html</p>','before');
		d$('#foo').html('<p>more html!</p>','after');

	or

		d$('#foo').html('<p>sweet as honey</p>');
		d$('#foo').outer('<p>free as a bird</p>');
		d$('#foo').top('<b>top of the pops</b>');
		d$('#foo').bottom('<span>bottom of the barrel</span>');
		d$('#foo').before('<pre>first in line</pre>');
		d$('#foo').after('<marquee>better late than never</marquee>');