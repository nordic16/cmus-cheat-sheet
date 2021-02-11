# cmus-cheat-sheet
A simple cmus cheat sheet made by Nørdic, a fellow Linux fan.
<br>Feel free to point out any sort of typos and grammatical errors, and if you have any suggestions, feel free to add them as well.

# Introduction.
cmus (C* music player) is a simple and reliable CLI music player for UNIX systems.
<br>It's my personal choice when it comes to choosing a CLI music player due to its ease of use, reliability and the features if offers.

# Installation.
This step depends on your package manager (pacman, apt, rpm, etc.).
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

If so, congratulations! Feel free to jump to the next section.

# Overview.
cmus has several features, such as track filtering, playlists and even plugins!

To navigate between pages (such as playlist page, queue page, etc...), one can press a numeric key ranging from `1-7`.

```
1 - Albums/Artists (tracks are sorted according to the album/artist they belong to)
2 - Media Library (all tracks are sorted by user criteria)
3 - Playlists (self-explanatory)
4 - Queue (where you can manage the queue)
5 - Browser (the place where you add your tracks to cmus).
6 - Library Filters (filter tracks in your library according to your preferences)
7 - Settings (you can bind actions, such as pausing/playing tracjs to different keyboard shortcuts)
```

# Adding media to your library.
To add tracks to cmus, navigate to the browser view by pressing `5`, and go to the directory where you stored your tracks stop. Then press `a` to individually add each track to the playlist. 

Alternatively, type `:` then the command `add "path/to/folder"`.

# Playing music from library.
When you're ready to listen to your favorite tracks press 2 then navigate to the one you want to listen to, then press Enter, and cmus should start playing it for you! 

1. To pause/play a track press `c`.
2. To stop media playback press `v`.
3. To play the previously played track press `z`.
4. To play the next track press `b`.
5. To seek 5 seconds use the arrow keys.
6. To seek 1 minute, press `.`/`,`.
6. Volume can be increased/decreased by 10 by pressing `+`/`-`.

Turns out CLI applications aren't as hard as you may have thought, right?

# Managing the queue.
### Automatically
You probably noticed that cmus just stops playing media after being finished with the one you previously played.

In order to prevent that from happening, cmus offers a set of features to manage the queue:

```
shift-C (continue): plays all media in your library (MUST BE ENABLED FOR FLUSHING AND REPEAT TO WORK).
s (shuffle): shuffles your library, playing a randomly selected track.
r (repeat): keeps playing media in your library even after reaching its end.
f (follow): in case of a track change, cmus will select the currently playing track.
``` 
As we can see in the following image, I enabled `continue` (C), `shuffle` (S) and `repeat` (R).

![image](https://user-images.githubusercontent.com/55633950/107123837-cfc3d400-6897-11eb-91d8-e411a0133629.png)

### Manually
If you want to manually queue up tracks, navigate to the track you want to be queued up, then press `e` to append, and `shift-e` to prepend, the selected track to the queue.

<br>The queue is **FIFO**, meaning that the last queued up track will be the last one to be played.

Then, switch to the queue view by typing `4`.

There, you can move up by pressing `p`, down by pressing `shift-p` and even remove tracks from the queue by pressing `shift-d`.

# Playlists.
So, now that you've added tracks to your library, it's time to organize them into playlists.
<br>Cmus creates 1 playlist by default (it's ironic because the playlist itself is called "default").
<br>Start by switching to the playlist view (press `3`), and type `:`,  followed by the command `pl-create [NAME]` then press space. You should see an `*` on the left: that indicates the **currently selected playlist**.

<br>To alternate between track/playlist navigation, press `TAB`.
<br>Now, switch back to the library view (press `2`), and press `y` to individually add tracks to the **currently selected playlist**, then go back to the playlist view, and open your new playlist.
<br>The keyboard shortcuts on the playlist view are the same as the ones on the queue view:

```
p to move the highlighted track down.
shift-P to move the highlighted track up.
shift-D to remove tracks from the playlist.
```

When you're ready to play an entire playlist, make sure you have Continue enabled (press `shift-C`) and play a random track within the playlist.
<br>**Note:** Cmus has support for multiple playlists, all you need to do is repeat the same steps for each new playlist.

**TODO**
1. Playlists // DONE
2. Filters
3. Settings
4. Other cool features
