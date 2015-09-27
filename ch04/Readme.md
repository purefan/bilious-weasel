Challenge 4
-------
[ [Link to challenge](http://ctf.infosecinstitute.com/levelthree.php) ]

This is the image of the challenge:

<img alt="Screenshot from the challenge" src="https://raw.githubusercontent.com/purefan/bilious-weasel/master/ch04/static/img/01.png" width="50%">

So from it we can spot 2 important clues:
1. There is  the Sesame Street Cookie Monster
2. The message refers to the HTTP protocol

An event happens when you hover your mouse over the image, an alert says "stop poking me".

The first thing that I did was to look at the request for the document, after all the hint pointed at HTTP, so I pressed `cmd + alt + i` to open the developer tools:

<img alt="Developer tools in Chrome" src="https://raw.githubusercontent.com/purefan/bilious-weasel/master/ch04/static/img/02.png" width="50%">

Then by inspecting the cookies tab we see an interesting record:

<img alt="Display of the cookie" src="https://raw.githubusercontent.com/purefan/bilious-weasel/master/ch04/static/img/03.png" width="50%">

The value of this cookie is `vasbfrp_syntvf_jrybirpbbxvrf`, now those underscores look like they are meant as spaces, and if we make the switch it looks like this `vasbfrp syntvf jrybirpbbxvrf`. It looks like gibberish, but to me they look structured like words, and I know that one of the oldest forms of cryptography is to replace a letter by another, we now have a name for this and we call it rotor cryptos because the original process of encoding involved a disc that you would rotate to find the encoded letter, so I googled "rot decoder" and found [this very nice website](http://theblob.org/rot.cgi) which gives me a list of the different rotated/decoded outcomes:

<img alt="Result from the rotor decryptor" src="https://raw.githubusercontent.com/purefan/bilious-weasel/master/ch04/static/img/04.png" width="50%">

There you have your flag ^_^
