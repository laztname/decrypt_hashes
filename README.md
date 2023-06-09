# decrypt_hashes

## Usage:
```
$ python decrypt_hash.py -h  
usage: decrypt_hash.py [-h] [-f [HASHES]] [-o [CRACKED_HASHES]]

options:
  -h, --help           show this help message and exit
  -f [HASHES]          Input any hash file separated by newline in format {hash}.
  -o [CRACKED_HASHES]  Stores all hashes and cracked passwords in files.
```


## Setup TOR Requirements for Linux
```
$ sudo vim /etc/tor/torrc

# Uncomment this line
ControlPort 9051
CookieAuthentication 1
```

Needs root privileges to access tor auth file

 ## Example Output:
```
$ python decrypt_hash.py -f h -o de.txt       
[+] Restarting TOR...
Created symlink /home/kali/.config/systemd/user/default.target.wants/homebrew.tor.service → /home/kali/.config/systemd/user/homebrew.tor.service.
[+] New IP: 75.63.67.34
[+] Sending 2 hashes...
[+] Success! Returned 2 passwords!
[+] Cracked 2 hashes:
29be83ff7eedd5ecf5807b6729ef69d237faaf3e:308015359755263
3bdd449dc37efc759e40729c1a071f8084a3d047:rodney20
[+] Cracked passwords written to de.txt
```
