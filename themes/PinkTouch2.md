# Pink Touch 2 Mods

Just a few minor CSS tweaks to improve the spacing and layout to suit my preference. For more details about the `.syntaxHighlighter` rule see [IncludeSyntaxHighlighter.md](../IncludeSyntaxHighlighter.md).

## Installation

From your theme's `Customize` view choose the `Theme` menu option and select "Use custom HML". Every theme's source will look different, but in general you can place the following code anywhere in the document `<HEAD>`. For consistency I prefer to locate the end `</HEAD>` tag and insert the following just above that as the last block of code in the header.

	<style type="text/css">
	/* customize code blocks */
	.syntaxhighlighter {
	    font-size: 13px !important;
	    border: 1px solid #ddd;
	    margin: 0 0 1.4em !important;
	}
	/* Decrease spacing between content, increase content width */
	#content {
	    padding-top: 210px;
	}
	.post {
	    padding: 25px 50px 22px;
	    margin-bottom: 60px;
	}
	.date {
	    margin-left: -80px;
	}
	/* Add bulleted list support */
	.post ul {
	    list-style: disc inside;
	}
	.post .tags,
	.post .chat {
	    list-style: none;
	}
	.text blockquote {
	    background: #ddd;
	    font-size: 1em;
	    font-style: italic;
	}
	.text blockquote p {
	    padding: 20px;
	}
	</style>
