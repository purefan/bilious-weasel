Challenge 3
-------
[ [Link to challenge](http://ctf.infosecinstitute.com/levelthree.php) ]

This challenge just gives us a QR image:
<img alt="Screenshot from the challenge" src="https://raw.githubusercontent.com/purefan/bilious-weasel/master/ch03/static/img/01.png" width="30%">

So my first idea was to decode it with an online tool (Im not going to link to the one I used because there are way too many options and its actually better for you to build your own set of tools)

After decoding the image this is the text that I got:

`.. -. ..-. --- ... . -.-. ..-. .-.. .- --. .. ... -- --- .-. ... .. -. --.`

Which at first sight it didn't really tell me anything, but after looking at it for a while I saw that each block is separated by a space and there are only 2 different characters: a dot and a dash... dot dot -pause- dot dot dash dot -pause- dash dash dash -pause- dot dot dot... well, if you say it out loud it sort of sounds like morse code, so yeah I found an online morse code converter and guess what? `INFOSECFLAGISMORSING` ;) Very interesting that they went with a morse code encoded flag in this one.
