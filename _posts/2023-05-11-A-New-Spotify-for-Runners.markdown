---
layout: post
title:  "Spotify Playlist Seggregation for Runners: Spotify Stride"
description: 
date:   2023-05-11 08:24:51 +0200
---

# Introduction

The idea is to seggregate your spotify playlist into different playlists, according to the pace you are running at the moment.

# Primary Features

1. Pace splits to consider: 
    a. Slow
    b. Medium
    c. Fast

2. Sort will be based upon the BPM (Spotify Metadata) of the song.

3. Store Analytics and release Spotify Wrap every month

4. Beta: Toggle feature to renew your playlist with new Songs


# App Frontend (Version 1.0)

1.  A Login page (no independent SignUp) using Spotify Credentials

2.  A Home page 
    a. Display a dropdown menu, to choose form among the playlists present in the spotify app, (can choose multiple)
    b. Horizontal Scroll View to change pace setting, each view will have a display of all songs in the setting, the playing song highlighted, the user can also change the song to be played, songs will be played one after the other (Shuffle capability should be added)
    d. No controls will be displayed (Spotify displays its own controls over the App) - Play, Pause, Skip Forward, Description
    e. When playing from a specific playlist, if a song in the playlist has exceeded 3 plays, then we remove the song from the playlist 
        and add a new song according the Spotify Recommendation API
    
# Working

A selected song would be played for x seconds without interruption. When x minutes are up, then we choose the next song from the playlist
according to the pace setting. The song will be played for x seconds and the process repeats.
The x can be configured by the user, default would be 45 seconds.w
# No backend required