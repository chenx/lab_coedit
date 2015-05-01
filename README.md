# lab_coedit
Experiment on collaborative editor.

Browser type
-----
browser.js can be used to determine what kind of browser it is. For example, output can be:

Browser name: Firefox  
Full version: 37.0  
Major version: 37  
App name: Netscape  
User Agent: Mozilla/5.0 (Windows NT 6.1; WOW64; rv:37.0) Gecko/20100101 Firefox/37.0  
Platform: Win32  
Language: en-US  
Java Enabled: false  

Web page events:
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


