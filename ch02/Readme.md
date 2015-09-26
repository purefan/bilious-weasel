Challenge 2
-------
[ [Link to challenge](http://ctf.infosecinstitute.com/leveltwo.php) ]

In this challenge we are hinted at a broken image, and more specifically the clue says "check the file"

<img alt="Screenshot from the challenge" src="https://raw.githubusercontent.com/purefan/bilious-weasel/master/ch02/static/img/01.png" width="75%">

There are several ways to do this, but what I did was "download" the image with curl, to do this I right clicked the image and then on _Inspect Element_
<img alt="Inspect Element" src="https://raw.githubusercontent.com/purefan/bilious-weasel/master/ch02/static/img/02.png" width="75%">

Then I right clicked the image node in the DOM tree and copied the url to the image:
<img alt="Getting the url to the image" src="https://raw.githubusercontent.com/purefan/bilious-weasel/master/ch02/static/img/03.png" width="75%">

Then I went to my terminal and just `curl http://ctf.infosecinstitute.com/img/leveltwo.jpeg`:

<img alt="CURL-ing the image" src="https://raw.githubusercontent.com/purefan/bilious-weasel/master/ch02/static/img/04.png" width="75%">

which gave me the text: `aW5mb3NlY19mbGFnaXNfd2VhcmVqdXN0c3RhcnRpbmc=`. Now, Im not an expert in encodings, but I know that Base64 is a popular encoding used in web applications so I decided to blindly run it through a Base64 Decoder (Google will give thousands, no need to download anything) and after running it I got the flag: 
`infosec_flagis_wearejuststarting`
