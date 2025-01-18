# ThisService 3

![image](https://github.com/user-attachments/assets/d23a8361-4c43-4ac7-9963-5a04e5fce0d8)

<s>See [ThisService](http://wafflesoftware.net/thisservice/).</s>[^1]

Create Mac OS X services from any script.

[Main + Download](https://web.archive.org/web/20151022020930/http://wafflesoftware.net/thisservice/)[New in 3.0](https://web.archive.org/web/20151022020930/http://wafflesoftware.net/thisservice/whatsnew/)[Service list](https://web.archive.org/web/20151022020930/http://wafflesoftware.net/thisservice/services/)[Future](https://web.archive.org/web/20151022020930/http://wafflesoftware.net/thisservice/services/)

## Hot feature requests and current tradeoffs

ThisService does the things it does well, but like most things, it's not perfect. This page is here to capture a few common feature requests and my thinking on them.

Most of the features that I put into ThisService and the way they are approached are direct results of discussions with people about them. If you have any ideas, please [let me hear it](https://web.archive.org/web/20151022020930/http://wafflesoftware.net/thisservice/contact). However, if you contact me about features that are mentioned on this page, I will assume that you have read about it.

Remember: ThisService is open source. Anyone willing could start from the stable version and try to add anything in if they'd like.

### File, formatted text and image/media services

Right now, ThisService supports only services that deal in unformatted text. It does not support making services that deal in files or that pass around images, sounds or video. Why is this? Because what ThisService supports is very well-defined; UTF-8 encoded text using the traditional UNIX filter concept.

In contrast to that, what would a service need to support for formatted text? Let's say you pick RTF or HTML - which version and which extensions? Should fragments or entire document structures be provided? What if there are references to external media within the text? What if the data is invalid; should you scrub it, making it valid? It's not impossible to solve, but it's significantly more to agree on than the unformatted text and consequently few utilities that deal in this. Most that spring to mind actually work on the plain-text encoding of the formatted text, like "tidy" utilities for HTML source code.

And what about images? Images seem very simple; just a bunch of colored pixels! In some cases, this is a close enough approximation to be functionally correct but in others it won't do. Images contain metadata and not only may that metadata be interesting but will also sometimes change the look of an image. A color profile or gamma setting makes the image look different, and tossing out information about orientation and DPI could make the image look upside down or way too small.

I understand that many people want to see support for other kinds of services. Right now, ThisService only supports things that are very easy to get right. Services have the potential to be very useful and it is my hope that they are shared to other people. That means that they are subject to different input under different circumstances than the original author might not have prepared for. If a service supports UTF-8, every allowed code point, and thus every unforeseen character, will have the opportunity to pass through unharmed (depending on the specific script, of course). With this kind of thinking, a service written several years ago by someone you don't know could still be ready for Emoji symbols or text in Arabic, Vietnamese or Cherokee.

It is unclear to me how to best make this kind of judgement for the types of extra services that are requested. I know that Automator does some of them, but only in the context of letting you piece together (say) image handling code that Apple's already written for you, not expecting you to write all of it and to get it right yourself. I will gladly hear your feedback if you have specific advice.

Copyright © 2006–2012 waffle software  
Contact [Jesper](https://web.archive.org/web/20151022020930/http://wafflesoftware.net/thisservice/contact/), the creator.  
Original concept: [John Gruber](https://web.archive.org/web/20151022020930/http://daringfireball.net/?ts).  
[ThisService Tech profile](https://web.archive.org/web/20151022020930/http://wafflesoftware.net/thisservice/techprofile/).


[^1]: Link is now dead!
