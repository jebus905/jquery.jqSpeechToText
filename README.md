# jquery.jqSpeechtotext
A simple jQuery UI plugin that attaches speech-to-text capabilities to form fields.

##Features

* works with jQuery 1.8+
* requires jQuery UI 1.9+

##Usage

Basic usage:

    $('textarea').jqSpeechToText( {options} );

##Parameters

###Options

####`icon0`, `icon1`

`icon0` will be displayed in the top right corner of the input/textarea.  It should represent the "microphone off" state.  When clicked, it will toggle the microphone state.
`icon1` is optional, but if given the icon will switch to this icon to represent "microphone on" state.

####`classPrefix`

`classPrefix` The prefix used to apply to the classes of all elements involved. String value. Default = `ui`

The classes involved include:
* interim results box gets `prefix`-speechtotext-interim
* icon gets `prefix`-speechtotext-icon

####`lang`

`lang` is the language setting for speech recognition.  String value. Default = `en-CA` (English, Canada)

####`capitalize`

`capitalize` will force the first character of the first word spoken of each sentence to be capitalized. Boolean value.  Default = true

####`addPeriod`

`addPeriod` will add a period to the end of spoken sentences.  Boolean value. Default = true
	
###Methods

####`toggle`

Will start or stop the speech recognition.

####`start`

Will start speech recognition.

####`stop`

Will stop speech recognition.

####`destroy`

Will destroy all widget elements and return the element to its original state.

####`option`

Get or Set options on-the-fly.

Code example:

	$("textarea").jqSpeechToText("option", "icon1");			                  // getter
	$("textarea").jqSpeechToText("option", "icon1", "images/mic-on.png");		// setter

###Events

####`onstart`

Fires when speech recognition starts.

####`onerror`

Fires when there is an error with speech recognition.

####`onend`

Fires when speech recognition is complete.
