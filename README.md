# osx_hacks
various hacks on osx for performance



# LOW PROIRITY I/O THROTTLE
sudo fs_usage | grep THROTTLED

check:

sysctl -a | grep throttle_enabled


test:

sudo sysctl -w debug.lowpri_thorttle_enabled=0

permanent:

sudo sh -c 'echo debug.lowpri_throttle-enabled=0 >> /etc/sysctl.conf'

and a video

https://asciinema.org/a/9am696gui0jpnvh4hvduv6clw
