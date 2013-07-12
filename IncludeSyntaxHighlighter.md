# Including SyntaxHighlighter

If you are a developer with a Tumblog, you'll definitely want to post some code at some point. The best way to do that is via the awesome [SyntaxHighlighter](http://alexgorbatchev.com/SyntaxHighlighter/) library. The great thing about it is that you can simply point to the hosted versions of all the necessary files, so setting it up couldn't be much simpler.

## Installation

From your theme's `Customize` view choose the `Theme` menu option and select "Use custom HTML". Every theme's source will look different, but in general you can place the following code anywhere in the document `<HEAD>`. For consistency I prefer to locate the end `</HEAD>` tag and insert the following just above that as the last block of code in the header.

	<!--
		BEGIN SyntaxHighlighter support
	-->
	<link href="http://alexgorbatchev.com/pub/sh/current/styles/shCore.css" rel="stylesheet" type="text/css" />
	<!--
		I like this theme too for dark background sites:
		link href="http://alexgorbatchev.com/pub/sh/current/styles/shThemeMidnight.css" rel="stylesheet" type="text/css" 
	/-->
	<link href="http://alexgorbatchev.com/pub/sh/current/styles/shThemeDefault.css" rel="stylesheet" type="text/css" />
	<script src="http://alexgorbatchev.com/pub/sh/current/scripts/shCore.js" type="text/javascript"></script>
	
	<!-- Import whichever brushes you plan to use here -->
	<!-- For more: http://alexgorbatchev.com/SyntaxHighlighter/manual/brushes/ -->
	<script type="text/javascript" src="http://alexgorbatchev.com/pub/sh/current/scripts/shBrushCss.js"></script> 
	<script type="text/javascript" src="http://alexgorbatchev.com/pub/sh/current/scripts/shBrushJScript.js"></script>
	<script type="text/javascript" src="http://alexgorbatchev.com/pub/sh/current/scripts/shBrushBash.js"></script>
	
	<!-- Kick it off -->
	<script language='javascript'>
		// You can turn this on or off, it's personal preference:
	    SyntaxHighlighter.defaults['toolbar'] = false;
		// Highlight all the code blocks on the page:
	    SyntaxHighlighter.all();
	</script>
	<!--
		END SyntaxHighlighter support
	-->

## Details

There's not much to it, other than customizing the code based on your own requirements. Namely, the above code only imports the brushes for CSS, JavaScript and Bash shell syntaxes since those are the only ones I use in my blog posts. [Many more](http://alexgorbatchev.com/SyntaxHighlighter/manual/brushes/) are supported and you can include as many as you like. Of course you can also modify the highlighter itself inside the inline script via the available [API](http://alexgorbatchev.com/SyntaxHighlighter/manual/api/) if needed.

## Usage

There are a couple of [approaches](http://alexgorbatchev.com/SyntaxHighlighter/manual/installation.html) for wrapping code blocks, but using the so-called `<pre /> method` seems the best for a Tumblog since the content will commonly be viewed via RSS. This is the approach I take and it looks like this:

	<pre class="brush: js">
		var foo = function() {
			alert('bar!');
		}
	</pre>

or

	<pre class="brush: bash">
		sh foo.sh -bar
	</pre>

## Tweaking the UI

Finally, I've also overridden the SyntaxHighlighter CSS slightly to suit my own visual taste, and the specific CSS will vary based on the theme in use as well. Here's an example of my tweaks for the theme "Pink Touch 2", mainly to decrease the font size slightly and give the code blocks a visual border:

	<style type="text/css">
	/* pink touch 2 overrides */
	.syntaxhighlighter {
	    font-size: 13px !important;
	    border: 1px solid #ddd;
	    margin: 0 0 1.4em !important;
	}
	</style>
