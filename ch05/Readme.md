Challenge 5
-------
[ [Link to challenge](http://ctf.infosecinstitute.com/levelfive.php) ]

Now this is a nasty one, when you first enter the page an infinite cycle of javascript alerts will keep you from doing anything. What I had to do was disable javascript, in Google Chrome you do this by going to settings, searching for javascript, then in Content Settings you can disable it for all sites (feel free to enable it after you're done with this challenge):

<img alt="Disable JS" src="https://raw.githubusercontent.com/purefan/bilious-weasel/master/ch05/static/img/02.png" width="50%">

Only after we do that can we actually see the challenge image:

<img alt="Challenge" src="https://raw.githubusercontent.com/purefan/bilious-weasel/master/ch05/static/img/01.png" width="50%">

So by looking at the image nothing really jumped to light for me, I went to the source code and couldn't find anything, thought that the reference to aliens could be pointing to the headers but didn't find anything there. Then I checked the image in the developer tools and noticed it looked different in the preview tab, so I thought there might be something _in_ the image.

One category of encryption is called Steganography, which is the technique of hiding messages inside other messages, for example... text inside images. so I downloaded the image and _read it_, my first attempt was a quick `curl http://ctf.infosecinstitute.com/img/aliens.jpg` sure enough it looked like a normal jpeg, but I had played a little with steganography and thought it was worth giving it a try so I went to the interwebs and tried to find an alternative for steghide (which is what I used in my Windows machine) for OSX (my main computer now is an apple laptop), after about 15 minutes I thought it was taking too long and just went to google and got [this online service](https://futureboy.us/stegano/decinput.html) for decoding hidden messages in images and when I ran it on [the aliens.jpg image](http://ctf.infosecinstitute.com/img/aliens.jpg) I got this:

`01101001011011100110011001101111011100110110010101100011010111110110011001101100011000010110011101101001011100110101111101110011011101000110010101100111011000010110110001101001011001010110111001110011`

Now, doesn't that look like binary...? well you guessed it, I went online to a binary translator and... `infosec_flagis_stegaliens`
