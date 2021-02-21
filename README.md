*Feel free to point out any sort of typos and/or grammatical errors, and if you have any suggestions, feel free to make a pull request.*

# Introduction.
When I started using Linux, I immediatly asked myself what music player I wanted to use to satisfy my need for music (Spotify didn't count, as I didn't want to keep paying for it).
<br>A quick research pointed me towards a great music player called **cmus** and, after using it for a while, I decided to write a cheat sheet on it that covers the installation, configuration and usage processes.

It's my personal choice when it comes to choosing a music player for Linux due to its ease of use, reliability and the features if offers.

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
In order to open cmus, just type `cmus` on your favorite shell, and it should open!

If not, make sure cmus is installed through the command `cmus --version`.

If so, congratulations! Feel free to jump to the next section.

# Overview.
cmus has several features, such as track filtering, playlists and even plugins!
<br>cmus is split into several views, such as the playlist view, settings view, and library view!
<br>To switch between views, one can use the following keys:

-  Albums/Artists (tracks are sorted according to the album/artist they belong to)
-  Media Library (all tracks are sorted by user criteria)
-  Playlists (self-explanatory)
-  Queue (where you can manage the queue)
-  Browser (the place where you add your tracks to cmus).
-  Library Filters (filter tracks in your library according to your preferences)
-  Settings (you can bind actions to different keyboard shortcuts)


# Adding media to your library.
In order to add tracks to your library, navigate to the browser view by pressing `5`, and go to the directory where you stored your tracks stop. Then press `a` to individually add each track to the playlist. 

Alternatively, type `:` then the command `add "path/to/folder"`.

# Playing music from library.
When you're ready to listen to your favorite tracks press 2 then navigate to the one you want to listen to, then press Enter, and cmus should start playing it for you! 

Can't find a specific track? Type `/` followed by the track's name and it should highlight the first match, if there's any. You can navigate to the next match by pressing `n` and to the previous by pressing `N` (exactly like vim).

- To pause/play a track press `c`.
- To stop media playback press `v`.
- To play the previously played track press `z`.
- To play the next track press `b`.
- To seek 5 seconds use the arrow keys.
- To seek 1 minute, press `.`/`,`.
- Volume can be increased/decreased by 10 by pressing `+`/`-`.

**Pro tip:** to shuffle your tracks on the library view, type `:rand`!
<br>Turns out CLI applications aren't as hard as you may have thought, right?

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
If you want to manually queue up tracks, navigate to the track you want to be queued up, then press `e` to append, and `shift-e` to prepend, that track to the queue.
<br>The queue is **FIFO** ([first in, first out](https://en.wikipedia.org/wiki/FIFO_(computing_and_electronics))), meaning that unless you prepend it, the last queued track will be the last one to be played.

In the queue view, you can change the order the highlighted track (use the arrow keys to move up/down): up by pressing `p`, down by pressing `shift-p`. You can also remove the highlighted track by pressing `shift-d`.

# Playlists.
So, now that you've added tracks to your library, it's time to organize them into playlists.
<br>Cmus creates 1 playlist by default (it's ironic because the playlist itself is called "default").
<br>Start by switching to the playlist view (press `3`), and type `:`, followed by the command `pl-create [NAME]` then press space. You should see an `*` (asterisk) on the left: that indicates the **currently selected playlist**.

<br>To alternate between track/playlist navigation, press `TAB`.
<br>Now, switch back to the library view (press `2`), and press `y` to individually add tracks to the **currently selected playlist**, then go back to the playlist view, and open your new playlist.
<br>The keyboard shortcuts in the playlist view are the same as in the queue view:

- `p` to move the highlighted track down.
- `shift-P` to move the highlighted track up.
- `shift-D` to remove tracks from the playlist.


When you're ready to play an entire playlist, make sure you have Continue enabled (press `shift-C`) and play a random track within the playlist.
<br>**Note:** Cmus has support for multiple playlists, all you need to do is repeat the same steps for each new playlist.

# Settings
Now that you're acquainted to cmus, it's time to tweak it a little bit.
### Changing our theme
Open `cmus`, then type `:colorscheme` preceded by `Ctrl-d`. This will print a list of available themes (stored in `/usr/share/cmus`) you can choose!
<br>At the time of writing, I'm using the one called `dracula`, which I'm very fond of. 

**TODO**
1. Playlists // DONE
2. Filters
3. Settings // On it
4. Other cool features
