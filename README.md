# Monitor/Managed mode changer

This code helps us change wifi card state(monitor to managed, or or on the contrary)

* Do this
* Deal with that

## Download and set up

First copy or get code from github repository

1. Execute the following command in the terminal:

   ```bash
   git clone https://github.com/poseydonianexe/Monitor-Managed-mode-changer.git
   cd Monitor-Managed-mode-changer
   chmod +x monitor-mode.py
   ```

2. Then run the code ```bash ./monitor-mode.py```


Note :: You can add shostcut to system using this commmand ```bash sudo cp monitor-mode.py /usr/bin```
## Modes (manual or cli)

We have two modes. You can see these in help menu

```text 
┌──(.venv)─(user㉿user)-[~]
└─$ ./monitor-mode.py -h      
Usage: monitor-mode.py [options]

Options:
  -h, --help    show this help message and exit
  -i INTERFACE  Enable/Disable Monitor mode
```

This is list of them:

* Manual mode ```bash ./monitor-mode.py``` : In manual mode, you can see list of active interfaces like this:

```text
┌──(.venv)─(user㉿user)-[~]
└─$ ifconfig -s
Iface      MTU    RX-OK RX-ERR RX-DRP RX-OVR    TX-OK TX-ERR TX-DRP TX-OVR Flg
<intfc>          65536        0      0      0 0             0      0      0      0 BMU
<intfc>         65536      697      0      0 0           697      0      0      0 LRU
<intfc>          65536        0      0      0 0            92      0      0      0 BMRU
<intfc>          65536        0      0      0 0            92      0      0      0 BMRU
<intfc>          65536  1386150      0      0 0        481192      0      0      0 BMRU
wlan1 (Taret interface)       65536    25329      0  23199 0           189      0      0      0 ABPNRU
Select the interface :: (Target interface)
```

Then program does it automatically. If your device is in managed mode, program changes it to manual mode or vice versa.

* Normal mode ```bash ./monitor-mode.py -i <interface>``` : In normal mode, just write ```text -i <interface name> ```
  after the program name. Then program does it automatically. If your device is in managed mode, program changes it to
  manual mode or vice versa.

Each mode chaning time you see this kind of text:
```text
Enabled monitor mode in  wlan1
```
or
```text
Enabled manager mode in  wlan1

```

## What is this? {id="what-is-this"}

Nowadays I have problems in enabling monotor mode. I write this code and put it on Github to help you. If you heve any issue raleated with code, start an isseue on Github using this [link](https://github.com/poseydonianexe/Monitor-Managed-mode-changer/issues) 
<seealso>
<!--Give some related links to how-to articles-->
</seealso>
