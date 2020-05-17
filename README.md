# oofvideosync
for syncing video playback on multiple machines on the network

This requires mplayer to run. It doesn't need to compile, it's just a few scripts.
It should run on any system that has mplayer installed and should play any file mplayer can play.

mplayer is a command line video player that has been around a long time. There's better documentation on mplayer than I can write here, so I'm not going to get into it. Long story short, you need mplayer installed. Mplayer did all the hard work of getting videos to sync over the network. Read about it here: http://www.mplayerhq.hu/DOCS/HTML/en/networksync.html


# clientstart

This starts the client mplayer command. You can run the command to get an interactive mode, or you can just call it like this:
`clientstart /path/to/video -n <network address>`
(Sorry none of that is written yet, still working on it)

Examples:

Interactive mode
`clientstart`

One line:
`clientstart /Users/username/Movies/video.mp4 -n 192.168.0.255`

# serverstart
`serverstart`

One line
`serverstart /Users/username/Movies/video.mp4 -n 192.168.0.255`
