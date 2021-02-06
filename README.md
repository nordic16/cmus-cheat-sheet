# cmus-cheat-sheet
A simple cmus cheat sheet made by Nørdic, a fellow Linux fan.
<br>Feel free to point out any sort of typos and grammatical errors, and if you have any suggestions, feel free to add them as well.

# Introduction
cmus (C* music player) is a simple and reliable CLI music player for UNIX systems.
<br>It's my personal choice when it comes to choose a CLI music player due to its ease of use, reliability and the features if offers.

# Installation.

This step depends on your package manager.
#### For arch-based distros:
```
sudo pacman -S cmus
```

#### For Debian-based distros
```
sudo apt install cmus
```

# Setup.
In order to open cmus, just type `cmus` on your favorite shell, and this window should show up.
![image](https://user-images.githubusercontent.com/55633950/107118230-8499c900-6877-11eb-8e0d-29af49c7d29a.png)

If not, make sure cmus is installed through the command ```cmus --version```.

Congratulations, you've just installed cmus! Now it's time for an overview of how it works!

# Overview
cmus has several features, such as music filtering, playlists and even plugins!

To navigate between pages (such as playlist page, queue page, etc...), one can press a numeric key ranging from `1-7`.

```
1 - Albums/Artists (media is sorted according to the album/artist they belong to)
2 - Media Library (all media sorted by user criteria)
3 - Playlists (self-explanatory)
4 - Queue (where you can manage the queue)
5 - Browser (the place where you add your media to cmus).
6 - Library Filters (filter media in your library according to your preferences)
7 - Settings (you can bind actions, such as pausing/playing media to different keyboard shortcuts)
```

# Adding media to your library.
To add tracks to cmus, navigate to the browser view by pressing `5`, and go to the directory where your media is stored. Then press `a` to add media to your library.

Alternatively, type `:` then the command `add "path/to/folder"`.

# Playing music from library.
When you're ready to listen to your favorite tracks press 2 then navigate to the one you want to listen to, then press Enter, and cmus should start playing it for you! 

1. To pause/play a track press `c`.
2. To stop media playback press `v`.
3. To play the previously played track press `z`.
4. To play the next track press `b`.
5. To seek 5 seconds use the arrow keys.
6. Volume can be increased/decreased by 10 by pressing `+`/`-`.

Turns out CLI applications aren't as hard as you may've thought, right?

# Managing the queue.
You probably noticed that cmus just stops playing media after being finished with the one you previously played.

In order to prevent that from happening, cmus offers a set of features to manage the queue:

```
shift-C: plays all media in your library (MUST BE ENABLED FOR FLUSHING AND REPEAT TO WORK).
s: shuffles your library, playing a randomly selected track.
r: keeps playing media in your library even after reaching its end.
f: in case of a track change, cmus will select the currently playing track.
``` 


If you want to manually queue up tracks, navigate to the track you want to be queued up, then press `e`. 
<br>The queue is **FIFO**, meaning that the last queued up track will be the last one to be played.
