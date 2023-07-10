# Wacky-tech-diary
NTB45's diary of wacky tech stuff
This place will have all my issues and errors and if found, their fixes here

I made it for small issues for which making a whole guide would be wasteful of resources


## Metal Gear Rising Revengence Crashing on launch on Intel GPU

### Intel with their infinite wisdom dropped support for directX9 and below stuff on intel Arc gpus and 12th gen integrated Iris graphics and up.

but no hope lost, you can run it from DXVK vulkan linux style

I suggested DXVK instead of D3D9on12 because its much easier to use and i heard from a lot of sources that it is faster.

download DXVK dlls from this repo https://github.com/doitsujin/dxvk/releases

Unzip/untar it (you may need to unzip the tar twice)

you got 2 folders there

32 bit is for 32 bit games

64 bit is for 64 bit games

go find out what your game uses, use pcgamingwiki.com for that, great site

then paste(probably overwrite, if overwriting, back the original game dlls up) the dlls in the same folder where the game's .exe is

if you want to be sure, paste it in other places you find a .dll file to, just to be safe, extra dlls at places that dont need it wouldn't hurt

and boom

game running

For me the error was that the game just launched, made a window, initialised a white screen, and crashed

if yours crash after that god knows whats wrong.
