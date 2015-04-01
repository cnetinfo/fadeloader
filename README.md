Query Fadeloader v1.0.0: a simple site preloader plugin

The jQuery Fadeloader plugin lets you easily implement a preloader to your site or section, using a cascade fade in effect to show specific blocks of content (for example, you can load first the header, then the menu and finally the content).

Usage

Fist include the required files on your page's HEAD ("easing" is optional):

<script src='//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js'></script>
<script src='//cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js'></script>
<script src='jquery.fadeloader.js'></script>

Then assign a class name to each of your elements using the alphabet. Let's say...

<body>
    <CODE>
    <div class="a"><img class="let" src="http://imageshack.us/a/img577/8746/80670611.jpg"></div>
    <div class="b"><img class="let" src="http://imageshack.us/a/img46/5216/37226104.jpg"></div>
    <div class="c"><img class="let" src="http://imageshack.us/a/img41/5663/51030348.jpg"></div>
    <div class="d"><img class="let" src="http://imageshack.us/a/img9/7412/73031581.jpg"></div>
    <div class="e"><img class="let" src="http://imageshack.us/a/img607/2171/14947433.jpg"></div>
    <div class="f"><img class="let" src="http://imageshack.us/a/img809/60/16218923.jpg"></div>
    <div class="g"><img class="let" src="http://imageshack.us/a/img46/5216/37226104.jpg"></div>
    <div class="h"><img class="let" src="http://imageshack.us/a/img41/5663/51030348.jpg"></div>
    <div class="i"><img class="let" src="http://imageshack.us/a/img9/7412/73031581.jpg"></div>
    <div class="j"><img class="let" src="http://imageshack.us/a/img24/6335/45762992.jpg"></div>
    </CODE>
</body>

Now hide them all with CSS:

body > div {
    display: none;
}

Finally set the Fadeloader in the 'document ready' event. This is the basic usage:

$(document).ready(function() {
    $('body').fadeloader({ });
});

That's it! Enjoy.
Reference
Option 	Type 	Default 	Description
mode 	string 	'class' 	Selection mode. 'Class' would search for elements with alphabetical classes (a, b, c...) inside the parent element ('body' in this case), while 'children' would select all his children.
fadeSpeed 	integer 	500 	The speed of the fade effect.
easeLoad 	string 	'linear' 	Defines easing. Using advanced effects requires 'JQuery Easing' plugin. Options: please visit http://api.jqueryui.com/easings/
displayType 	string 	'block' 	Defines which display style for the affected elements. Options: 'block', 'inline-block', 'inline', 'table', 'inline-table', 'list-item', 'inherit', etc.
preLoader 	boolean 	true 	When 'true', a preloader image will be displayed until the window is completely loaded. Options: 'true' or 'false'.
preloadImg 	string 	'loading.gif' 	Path to the image used as preloader. Defaul 'loading.gif' is provided along with this plugin.
preloadWidth 	integer 	50 	Width in pixels of the preloader image.
preloadHeight 	integer 	50 	Height in pixels of the preloader image.
preloadCustom 	'string' (HTML only) 	'' 	Paste here your HTML to use your own preloader. Remember to set 'preloader' as the class name for the main element.
onComplete 	'string' 	'' 	Callback function, executed after all ellements have been loaded.
