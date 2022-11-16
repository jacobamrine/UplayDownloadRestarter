# UplayDownloadRestarter
Restart Uplay so it can continue downloading a game after failure

My house used to be on slow DSL Internet (now we are on Starlink!) that would fail often. At that time, I would commonly play games that would require large downloads which took days on DSL. I would leave it downloading overnight, but would come find it stopped in the morning.

After some testing, I eventually found that it seems Uplay (game client like Steam) could not recover a game download after an internet failure. I wrote a program in Python that watches for a download failure, then restarts the Uplay client.

This script makes use of pyautogui to detect a zero download speed on the screen (using an example screenshot snip) which will then wait a couple minutes for the internet to come back up, then it will restart Uplay. It will then locate the start download icon within Uplay and click it to restart the download. I know it works because Uplay was still downloading the next morning and my grandparents were complaining about slow internet :D

To reduce load, the program only checks every so often for the 0 download speed. I think pyautogui is rather lightweight, but I didnt want it doing a bunch of screengrabbing in the background if it didnt need to. Honestly, the icons have probably changed by now so the program wouldnt work but I figured I should post it here
