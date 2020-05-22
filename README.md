# oofvideosync
for syncing video playback on multiple machines on the network

This is a work in progress and as of May 2020 still doesn't work well. 

This requires mplayer or omxplayer (omxplayer preferred, but omxplayer is only for raspberry pis, mplayer is crossplatform but harder to get to work right) to run. It doesn't need to compile, it's just a few scripts.

If using omplayer, you'll also need omxplayer-sync: https://github.com/turingmachine/omxplayer-sync

Before using it the first time:

`apt-get install libpcre3 fonts-freefont-ttf fbset libssh-4 python3-dbus omxplayer`
`wget -O /usr/bin/omxplayer-sync https://github.com/turingmachine/omxplayer-sync/raw/master/omxplayer-sync`
`chmod 0755 /usr/bin/omxplayer-sync`

If using mplayer, it should run on any system that has mplayer installed and should play any file mplayer can play.

mplayer is a command line video player that has been around a long time. There's better documentation on mplayer than I can write here, so I'm not going to get into it. Long story short, you need mplayer installed. Mplayer did all the hard work of getting videos to sync over the network. Read about it here: http://www.mplayerhq.hu/DOCS/HTML/en/networksync.html


# clientstart

This starts the client mplayer command. You can run the command to get an interactive mode, or you can just call it like this:
`clientstart /path/to/video -n <network address>`
(Sorry none of that is written yet, still working on it)

Examples:

Run with default
`clientstart`

Or specify a video file:
`clientstart /Users/username/Movies/video.mp4 -n 192.168.0.255`

# serverstart
`serverstart`

Or specify a video file:
`serverstart /Users/username/Movies/video.mp4 -n 192.168.0.255`

Note: When using omxplayer, both files must have the same filenamei

To get this to run automatically on launch:
`nano /etc/rc.local`
Then add the script before the last line

