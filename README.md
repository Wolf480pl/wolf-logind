A WIP proof-of-concept of systemd-logind replacement done in a more unix way.

Requires execline and s6 from [skarnet].

`/run/wolf-login/event` must be set up as a fifodir

PAM configuration:
```
session		optional	pam_exec.so seteuid log=/tmp/pam.log /path/to/wolf-session-pam
```

[skarnet]: https://skarnet.org/poweredby.html
