# IOTA ESP32 integration 

This project install [IOTA simple wallet for ESP32](https://github.com/oopsmonk/iota_cclient_esp32) and all it's requirements.

## Requirement  

* Homebrew or MacPort

### Step 1: Checkout source  

    ```
    git clone https://github.com/magnisinfo/IOTA_ESP32_integration.git    
    ```    

### Step 2: Install requirements and download simple wallet.

    ```
    cd IOTA_ESP32_integration

    #Run this command:
    ./init 
    #or run file "init"

    #You need to run this file twice to setup global variables in ".profile".
    ```   

### Step 3: Configure simple wallet 

```
#Go to {HOME}/IOTA_ESP32/iota_cclient_esp32:
cd ~/IOTA_ESP32/iota_cclient_esp32

#Run this command:
./config 
#or run file "config"

# configure WiFi SSID & Password
[IOTA CClient Configuration] -> [WiFi SSID]
[IOTA CClient Configuration] -> [WiFi Password]
[IOTA CClient Configuration] -> [IRI Node URI]
[IOTA CClient Configuration] -> [Port Number of IRI Node]
```

### Step 4: Build & flash

```
#Run this command:
./flash 
#or run file "flash"

#After build choose flash port:
Choose port to load:
(1) - /dev/cu.Bluetooth-Incoming-Port
(2) - /dev/cu.SLAB_USBtoUART
Write number:
2
```

output:  
```
I (10454) wifi: pm start, type: 1

I (11604) tcpip_adapter: sta ip: 192.168.43.10, mask: 255.255.255.0, gw: 192.168.43.1
I (11604) iota_main: Connected to AP
I (11604) iota_main: IRI Node: nodes.devnet.thetangle.org, port: 443, HTTPS:True

Welcome to IOTA wallet. Write you seed:
>999999999999999999999999999999999999999999999999999999999999999999999999999999999

Choose operation:
(1)-Get account balance
(2)-Send tokens to address
(3)-Send message
>
```
