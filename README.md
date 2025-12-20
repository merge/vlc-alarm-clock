## An alarm clock for Linux

It uses sudo, rtcwake and alsamixer.

### sudo rule
Add the following line to the /etc/sudoers file; replace "username" with your username:

```
username	ALL=(ALL:ALL) NOPASSWD:/usr/sbin/rtcwake
```

### optional: install
This is simply a script to be run as user. If you want it in your $PATH, copy it to `~/.locl/bin/`. This is optional.

### how to use
```
vlc-alarm-clock -a <path_to_audio_file> -d <day> -t <hh:mm>
```

where `hh:mm` is 24-hour format; `-m month` can be set.
year is simply always the current year. `-a audiofile` can be set.
