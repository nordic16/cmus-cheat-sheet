# cmus-cheat-sheet
cmus (C* music player) is a simple and reliable CLI music player for UNIX systems.

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

To navigate between pages (such as playlist page, queue page, etc...), one can press a numeric key ranging from `1-6`.

```
1 - Albums/Artists (media is sorted according to the album/artist they belong to)
2 - Media Library (all media)
3 - Playlists (self-explanatory)
4 - Queue (where you can manage the queue)
5 - Browser (the place where you add your media to cmus).
6 - Library Filters (filter media in your library according to your preferences)
7 - Settings (you can bind actions, such as pausing/playing media to different keyboard shortcuts)
```

# Adding music.
To add music, navigate to the browser page by pressing `5`, and go to the directory where your media is stored, and press `a` to add each file to your library.

Alternatively, type `:` then the command `add "path/to/folder"`.
 
