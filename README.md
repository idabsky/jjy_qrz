function jjy_qrz() works when MSYNC is not TRUE
SNR calculations are not yet solved
  wwv signal(100Hz) :20.8second/60sec.(estimated) 
  jjy signal(1000Hz):38second/60sec.


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

