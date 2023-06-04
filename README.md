## An alarm clock for Linux

It uses sudo, rtcwake and pulseaudio.

### sudo rule
Add the following line to the /etc/sudoers file; replace "username" with your username:

```
username	ALL=(ALL:ALL) NOPASSWD:/usr/sbin/rtcwake
```

### optional: install
This is simply a script to be run as user. If you want it in your $PATH, copy it to `~/.locl/bin/`. This is optional.

### how to use
```
vlc-alarm-clock -a <path_to_audio_file> -m <month> -d <day> -t <hh:mm>
```

where `hh:mm` is 24-hour format; year is simply always the current year.
