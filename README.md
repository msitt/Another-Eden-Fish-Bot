# Another Eden Fish Bot
This is a bot for Another Eden that completely automates the entire fishing process, including returning to the fish vendor and traveling to different fishing spots.

[Download here!](https://github.com/MegaMagicPower/Another-Eden-Fish-Bot/releases/latest)

## Is it safe to run this? Will I get banned?
I can't guarantee anything, but I have taken as many precautions as possible. The bot itself does not modify or even read the game memory or emulator memory at all; it simply takes screenshots, processes them, and clicks the screen. I've also put steps in to avoid the behavior being the exact same every time. There are randomly timed pauses between every action, and the clicks have a randomized area so its never the exact same pixel. Catching the fish itself is always done with at least 200-250ms+ reaction time, which is average human reaction time. Since this is essentially just a macro on steroids, and they don't ban for macros, I don't think anything will happen. But don't blame me if it does.

## What do I need to run this?
As of right now, the only emulator supported is LD Player. I tried to get it to work on Nox, but it doesn't respond to mouse messages correctly. Its possible that other emulators may work, I just haven't tried them. If there's enough interest in them I may try. As of right now, simply download LD Player, transfer your account, finish all your fishing, and then transfer back to your emulator/device of choice.

You also must be able to run the game at full speed at all times (no potato computers), as the bot is very heavily macro based. If you can't run the reroll macro, you most likely can't run this. The game must also be run with the English language setting.

## How do I run this?
First, open up the config.txt file and read through it. The instructions should be pretty self explanatory, except for the first setting, which I'll explain. The bot needs to be able to find the window the game is running in, which it does so with the window name. You can find this in the top left corner of the window (see screenshot where my window name is "Suz2"). By default this is "LDPlayer", but you may have renamed it. Put this in as your "Window Name" in the config file.

![Preview](https://i.imgur.com/INxSNRW.png)

Once that's done, start your emulator. The emulator itself needs to be set to at least around 1280x720 resolution; this is because the bot is reading the screen, so if its hard to read for you, its hard to read for the bot as well. Feel free to experiment but if the bot starts to act odd, you've most likely chosen too low of a resolution. From here, you're free to resize the window, however the same as before applies; the smaller you make the window, the harder it will be for the bot to successfully read it.

Now start your game and get to the normal state where you're free to run around. The menu should not be open. Make sure the emulator is not minimized. Now you're ready to run the bot, which you can do so via the command prompt or simply double clicking the exe file. If everything worked correctly, you should see the map screen being opened as it travels to the fish vendor. The bot always visits the fish vendor to turn in fish and buy bait for traveling to each pool. If you haven't changed the config file, you'll be buying 20 Fishing Dango's and then traveling to Kira Beach to fish. Once you are satisfied that it's working correctly, feel free to setup the config file how you want to travel to other locations.

While the bot is running, you are free to use your computer as normal. Browse the web, play games, etc. The only thing you need to remember is you cannot let your mouse move over the window. Why? When mouse messages are processed, where the mouse currently is in the window takes precedence over any location specified in the message. That means if the bot wants to click in the center of the screen, but you have the mouse in the top left corner, it will click in the top left corner, thus breaking the macro and forcing you to restart the bot. This sounds more troublesome than it actually is; simply put the emulator window behind another one (like your browser, game, discord, etc) and forget about it. If you have a second monitor, this also works great as well as a spot to store it. If you don't have a second monitor, but want to check up on it periodically to make sure it hasn't gotten stuck, Windows has a nice feature on with Aero where you can hover your mouse over a program in the task bar at the bottom and it will display a mini window showing you what's going on. This is how I check up on it myself.

The other thing to remember is you cannot minimize the emulator. Why? When minimized, the window no longer renders, so the bot is unable to take screenshots. So don't minimize, just put it behind another window.

## What about random battles?
All battles are done via just auto attacking, so put your best physical attackers in the group. The bot never attempts to heal, so technically you could die if you can't 1 turn everything, although it would probably take 12+ hours.

## What about horrors and lake lords?
This is still an experimental feature as I haven't actually gotten far enough in my own fishing to test it out in a live scenario. What should happen is that if you enter a random battle after using a bait high enough to attract a horror or lakelord in the pool you're at, the bot should completely pause and give you a message that its encountered one. Manually finish the battle, re-enter the fishing pool (click the fish icon), and then finally press enter to continue fishing where you left off. As an example, let's take the Greater Whale in the Dimension Rift. According to the fish guide, you can only catch it with Snitch Sardine. So if you're currently using the Snitch Sardine, and you enter any random battle after a fish catch, it will pause. This could be annoying if this particular bait can also cause regular battles, which at the moment I'm unsure of. I might revisit this if it turns out to not be a very good solution.

## The bot got stuck. Wtf?
Traveling to the pools is entirely macro based. If your computer or internet have a lag spike, the macro will break. Restart the bot to continue. The macro itself may just break randomly sometimes too as I'm not perfect; if you find any spot that breaks a lot, let me know and I'll try to fix it.

## Can I run this over night without anything weird happening?
You should be able to. If a macro breaks, it will finish it out and then enter an infinite loop (waiting to catch a fish) that it will never exit from. So at most you should only have random commands being entered for about 5 minutes max before this happens.

## How do I build this myself?
You need OpenCV built with Tesseract linked to it. I suggest using Microsoft's vcpkg package manager to build Tesseract and then manually building OpenCV and directing it to the Tesseract library you built. Then you'll need to put the various DLLs, as well as the Tesseract english trained data in the same directory as the exe (tessdata/eng.traineddata)

## Donations
[paypal.me/megamagicpower](paypal.me/megamagicpower)