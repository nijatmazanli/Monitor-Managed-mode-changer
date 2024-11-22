# Monitor/Managed mode changer

This code helps us change the Wi-Fi card state(monitor to manage or on the contrary)

## Download and set up

First copy or get code from the GitHub repository

1. Execute the following command in the terminal:

```bash
git clone https://github.com/poseydonianexe/Monitor-Managed-mode-changer.git
cd Monitor-Managed-mode-changer
chmod +x monitor-mode.py
```

2. Then run the code
```bash
./monitor-mode.py
```


Note:: You can add shortcuts to the system using this command
```bash
sudo cp monitor-mode.py /usr/bin
```
## Modes (manual or cli)

We have two modes. You can see these in the help menu.

```text 
┌──(.venv)─(user㉿user)-[~]
└─$ ./monitor-mode.py -h      
Usage: monitor-mode.py [options]

Options:
  -h, --help    show this help message and exit
  -i INTERFACE  Enable/Disable Monitor mode
```

This is a list of them:

* Manual mode
```bash
 ./monitor-mode.py
  ```
: In manual mode, you can see a list of active interfaces like this:

```text
┌──(.venv)─(user㉿user)-[~]
└─$ ./monitor-mode.py
Iface      MTU    RX-OK RX-ERR RX-DRP RX-OVR    TX-OK TX-ERR TX-DRP TX-OVR Flg
<intfc>          65536        0      0      0 0             0      0      0      0 BMU
<intfc>          65536      697      0      0 0           697      0      0      0 LRU
<intfc>          65536        0      0      0 0            92      0      0      0 BMRU
<intfc>          65536        0      0      0 0            92      0      0      0 BMRU
<intfc>          65536  1386150      0      0 0        481192      0      0      0 BMRU
wlan1 (Target interface)       65536    25329      0  23199 0           189      0      0      0 ABPNRU
Select the interface :: (Target interface)
```

Then the program does it automatically. If your device is in managed mode, the program changes it to manual mode or vice versa.

* Normal mode
  ```bash
  ./monitor-mode.py -i <interface>
  ```
   : In normal mode, just write ```text -i <interface name> ```
  after the program name. Then the program does it automatically. If your device is in managed mode, the script changes it to
  manual mode or vice versa.

Each mode change time you see this kind of text:
```text
Enabled monitor mode in  wlan1
```
or
```text
Enabled manager mode in  wlan1

```

## What is this? 
Nowadays I have problems in enabling monitor mode. I wrote this code and put it on Github to help you. If you have any code-related issues, start an issue.
