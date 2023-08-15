# Wacky-tech-diary
### NTB45's diary of wacky tech stuff
This place will have all my issues and errors and if found, their fixes here

I made it for small issues for which making a whole guide would be wasteful of resources


## Metal Gear Rising Revengence Crashing on launch on Intel GPU

### Intel with their infinite wisdom dropped support for directX9 and below stuff on intel Arc gpus and 12th gen integrated Iris graphics and up.

but no hope lost, you can run it from **DXVK** linux style

I suggested DXVK instead of **D3D9on12** because its much easier to use and i heard from a lot of sources that it is faster.

If my guide is too shitty use this gentleman's guide https://www.reddit.com/r/pcgaming/comments/mlfcsc/a_guide_to_dxvk_on_windows/  (if you hate reddit open it on libreddit or archive.org or something)



download DXVK dlls from this repo's releases https://github.com/doitsujin/dxvk/releases

Unzip/untar it (you may need to unzip the tar twice)

you got 2 folders there

32 bit is for 32 bit games

64 bit is for 64 bit games

go find out what your game uses, use pcgamingwiki.com for that, great site

then paste(probably overwrite, if overwriting, back the original game dlls up) the dlls in the same folder where the game's .exe is

if you want to be sure, paste it in other places you find a .dll file to, just to be safe, extra dlls at places that dont need it wouldn't hurt

and boom

**game running**

For me the error was that the game just launched, made a window, initialised a white screen, and crashed

if yours crash after that god knows whats wrong.

## TranslucentTB not working on Windows 11
This issue appeared because microsoft changed a few things in a windows update and as the result it ducked translucenttb

But no biggie, we can easily revert to the old visually and functionally identical taskbar without a lot of fuzz like downgrading and stuff.

Credit goes to this guy on reddit for posting an easy fix that doesn't involve the command line 
https://www.reddit.com/r/WindowsHelp/comments/11kyhiz/translucenttb_not_working_windows_11_version_22h2/jc8e1gg/

1.  Go to the **Vivetool GUI GitHub** page: https://github.com/PeterStrick/ViVeTool-GUI/releases and download the latest version of the software.
2.  Once the download is complete, run the installer to install **Vivetool GUI** on your computer.
3.  After the installation is complete, open **Vivetool GUI**.
4.  In the top left box, you will see a drop-down menu that says "Select build". Select the first build that is listed in the menu.
5.  In the search box, type **26008830**. This is the ID of the feature that messes with TranslucentTB.
6.  Click on the "Perform action" button and select "Deactivate feature".
7.  Close all windows and reboot your computer.
8. and BAM, TRANSLUCENTTB working
Now you can do this from command line too in single copy paste solution, but i prefer more control from the gui.

## How to install FIREFOX without using any other browser in Windows

If you are messing around with enterprise LTSC versions or stripped down versions of Windows like tiny11, there is a good chance that edge will not be installed by default, that is a good thing, but if there is absolutely no browser preinstalled, that could be a huge problem.
and opening internet explorer is like opening rats nest, its way too outdated to use
But we can again, do things linux style and install browsers from the command line.
Now there are quite a few ways to do it.

But first of all open the Powershell by searching it on the start menu

then putting the directory to Desktop by
	cd Desktop
### Curl
Its a cross platform terminal software used for viewing and doing all sorts of stuff with http
Curl is preinstalled on Windows 10 version 1803 or later
curl -L "https://download.mozilla.org/?product=firefox-latest&os=win&lang=en-US" -o FirefoxSetup.exe

### Wget
Wget is the mozilla recommeded way of downloading firefox from command line

wget -O FirefoxSetup.exe "https://download.mozilla.org/?product=firefox-latest&os=win&lang=en-US"

### Winget
winget is one of the new toys microsoft released to download applications from command line proper linux style
Easiest method so far to install firefox, only if winget happens to be preinstalled in your windows installation , its sometimes preinstalled, sometimes not

just go
	winget install firefox
and it should do the magic.



## Persona 4 Golden from Fitgirl repacks not Launching with Community Enhancement pack or Aemulus

First, make sure mod you are installing is persona4 32bit compatable 

### Then make sure the standard fitgirl compatability of running .exe as administrator from compatablity tab of it's exe's properties is disabled

It should work now


## How to disable widgets menu in windows 11

Everyone hates that useless pesky little menu that Microsoft added
but if you have Windows 11 pro, that bastard can be removed in minute and never bother you again

*First* : Open the **Local Group Policy Editor** (gpedit.msc on run).

*Second* : Navigate to **Computer Configuration\Administrative Templates\Windows Components\Edge UI**​

*Third* : In the right pane of **Edge UI** in the Local Group Policy Editor, double click/tap on the **Allow edge swipe** policy to edit it.

*Fourth* : Click on Enabled to enable it, or Disable to disable it.

For other versions of Windows refer to this website https://www.elevenforum.com/t/enable-or-disable-screen-edge-swipe-in-windows-11.3717/

