# lab_coedit
Experiments on real-time collaborative editor on web based on javascript.

By: X. Chen  
Since: April 2015  

About
-----

Basically, the tasks involved are:
- collaborative:
  - based on textarea, or based on editable DIV
  - capture event. event source can be: keyboard, mouse, drag/drop, ime input, cut/paste, browser undo/redo
  - how much to capture: 
    - entire text (easy, but large size), 
    - or the changed text (smaller size, but hard to capture sometimes)
  - synchronization through websocket, or ajax.
- editor features:
  - wrap or not wrap
  - line numbering
    - if wrap, then line numbering should change position according to wrap
  - others: 
    - font size, color, style
    - keywords highlighting


Browser type
-----

browser.js can be used to determine what kind of browser it is. For example, output can be:

<pre>
Browser name: Firefox  
Full version: 37.0  
Major version: 37  
App name: Netscape  
User Agent: Mozilla/5.0 (Windows NT 6.1; WOW64; rv:37.0) Gecko/20100101 Firefox/37.0  
Platform: Win32  
Language: en-US  
Java Enabled: false  
</pre>

Web page events
-----

- keydown -> keypress -> keyup
- mousedown -> mouseup
- input
- change
- cut/paste
- dragstart -> dragend, drop
 
Disable ime input
-----

For example, on textarea, include:

- css: ime-mode:disabled;
- attribute: type="tel"

&lt;textarea rows=20 cols=30 id="t1" type="tel" style="ime-mode:disabled">&lt;/textarea>

Textarea no wrap
--------------

Add this to textarea style, so it won't wrap, but scroll in width:

    white-space: pre;
    word-wrap: normal;
    overflow-x: scroll;


Relevant editors
--------

- http://collabedit.com
- Google DOCS editor: https://support.google.com/docs
- http://www.firepad.io
- http://etherpad.org

More References
-----------

<pre>
http://javascript.info/tutorial/keyboard-events#processing-the-character-keypress
http://stackoverflow.com/questions/263743/caret-position-in-textarea-in-characters-from-the-start
http://stackoverflow.com/questions/6157929/how-to-simulate-a-mouse-click-using-javascript
http://stackoverflow.com/questions/17858174/set-cursor-to-specific-position-on-specific-line-in-a-textarea
http://en.allexperts.com/q/Javascript-1520/Inserting-text-text-area.htm
http://blog.vishalon.net/index.php/javascript-getting-and-setting-caret-position-in-textarea/
http://stackoverflow.com/questions/11338592/how-can-i-bind-to-the-change-event-of-a-textarea-in-jquery
http://jsbin.com/puvikutaha/1/edit?html,css,js,output
* http://help.dottoro.com/ljtfkhio.php
* http://stackoverflow.com/questions/3239124/javascript-catch-paste-event-in-textarea
* http://collabedit.com/dtwpg
http://www.quirksmode.org/js/keys.html
* http://see.sl088.com/wiki/Html_%E8%BE%93%E5%85%A5%E6%B3%95%E4%BA%8B%E4%BB%B6
* http://www.cnblogs.com/zoho/archive/2012/07/06/2578885.html
* mouse drag: http://help.dottoro.com/ljmojcxu.php
* disable ime mode: http://stackoverflow.com/questions/15520410/disable-ime-mode-in-google-chrome
  (use both ime-mode:false, and type=tel)
</pre>
