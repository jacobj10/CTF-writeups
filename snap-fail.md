#snap-fail
###200 - Reversing

###Files
snap-fail.tar.gz

###Writeup
```bash
0:50:02 Downloads tar xvf snap-fail.tar.gz 
snap-fail/
snap-fail/dump.pcap
snap-fail/snap-fail.apk
``` 

I unzipped the apk only to find what appeared to be an AS project. Just to be safe and not ignore the obvious, I ran
`grep -r flag` in the  directory and got the output
```bash
0:51:26 snap-fail grep -r flag
META-INF/CERT.SF:Name: res/drawable/flag.png
META-INF/MANIFEST.MF:Name: res/drawable/flag.png
Binary file resources.arsc matches
Binary file classes.dex matches
Binary file snap-fail.apk matches
```

Navigating to res/drawable/flag.png reveals the flag:

greyhatctf{don't_hard_code_keys_bois}

