add to ntp.conf
server 127.127.36.1
fudge 127.127.36.1 stratum 14 flag2 0 flag3 0 flag4 1
#(equal as refclock_wwv  This is another refclock driver.)

function jjy_qrz() works when MSYNC is not TRUE
SNR calculations are not yet solved
  wwv signal(100Hz) :20.8second/60sec.(estimated) 
  jjy signal(1000Hz):38second/60sec.
Precision is decreased from original refclock driver by second sync methods.This may be due to individual hardware

Status(11/24/2005)
MSYNC  work sometimes the threshold is exceeded and the process fails. In that case restart ntpd. 
SSYNC  work debug code still remains
DSYNC  work
INSYNC work

Status(10/25/2005)
MSYNC  work immediately  
SSYNC  not work
DSYNC  work
FGATE  not work
DGATE  Keep SYNC flg while avoiding error
BGATE  error occur

Status(10/13/2005)
MSYNC  force engaged 
SSYNC  not work
DSYNC  unstable
FGATE  not work
DGATE  error occur

Thanks to

https://akebi.jp/temp/jjy/

and ka9q
,just type on urban distro_pulseAudio(Warning:outputs) 
WWV-master$ ./wwvsim | paplay --rate=16000
https://github.com/jj1bdx/WWV/tree/master
https://wwv.mcodes.org/

