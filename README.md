# simple-screencast
a screencast program written in simple bash script

Take a screencast of a window in X Windows System environment

# Required Packages

imagemagick
ffmpeg

# Usgae

First, get the ID of the target window.

```command.log:
$ xwininfo | awk '($0 ~ "^xwininfo: Window id: "){print $4}'
# This program blocks here and it shows the ID as follows when you click the target window
0x4400002
$
```

Let's take a screencast by _simple-screencast_.

```command.log:
$ ./simple-screencast 0x4400002 10 5
...
$ 
```

1st argument is the ID of the target window.
2nd one means the frame rate. 3rd one is the length of the screencast in seconds.

Then you got the screencast as _test.mp4_.

# Sample

See [this page](http://satoru-takeuchi.org/misc/simple-screencast.html).
It's a screencast of a terminal emulater on which I wrote and run a
hello world program written in golang.
