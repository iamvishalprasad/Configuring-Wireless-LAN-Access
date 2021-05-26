# Configuring Wireless LAN Access

## Introduction

#### Wireless LAN

Wireless LANs (WLANs) are wireless computer networks that use high-frequency radio waves instead of cables for connecting the devices within a limited area forming LAN (Local Area Network). Users connected by wireless LANs can move around within this limited area such as home, school, campus, office building, railway platform, etc.

## Component of WLANs
The components of WLAN architecture as laid down in IEEE 802.11 are −

**Stations (STA) −** Stations consist of all devices and equipment that are connected to the wireless LAN. Each station has a wireless network interface controller. A station can be of two types − Wireless Access Point (WAP or AP) & Client

**Basic Service Set (BSS) −** A basic service set is a group of stations communicating at the physical layer level. BSS can be of two categories −
- Infrastructure BSS
- Independent BSS

**Extended Service Set (ESS) −** It is a set of all connected BSS.

**Distribution System (DS) −** It connects access points in ESS.

![Distribution System](https://user-images.githubusercontent.com/77826589/118360169-1ebe8b00-b5a4-11eb-8b12-2a5ede61b8a1.jpg)

## Types of wireless LANs

WLANs, as standardized by IEEE 802.11, operate in two basic modes, infrastructure, and ad hoc mode.

- **Infrastructure Mode −** Mobile devices or clients connect to an access point (AP) that in turn connects via a bridge to the LAN or Internet. The client transmits frames to other clients via the AP.

- **Ad Hoc Mode −** Clients transmit frames directly to each other in a peer-to-peer fashion.

## Advantages of WLANs
- They provide clutter-free homes, offices and other networked places.
- The LANs are scalable in nature, i.e. devices may be added or removed from the network at greater ease than wired LANs.
- The system is portable within the network coverage. Access to the network is not bounded by the length of the cables.
- Installation and setup are much easier than wired counterparts.
- The equipment and setup costs are reduced.

## Disadvantages of WLANs
- Since radio waves are used for communications, the signals are noisier with more interference from nearby systems.
- Greater care is needed for encrypting information. Also, they are more prone to errors. So, they require greater bandwidth than the wired LANs.
- WLANs are slower than wired LANs.

## Application of WLANs
- Wireless LANs have a great deal of applications. Modern implementations of WLANs range from small in-home networks to large, campus-sized ones to completely mobile networks on airplanes and trains.
- Users can access the Internet from WLAN hotspots in restaurants, hotels, and now with portable devices that connect to 3G or 4G networks. Oftentimes these types of public access points require no registration or password to join the network. Others can be accessed once registration has occurred or a fee is paid.
- Existing Wireless LAN infrastructures can also be used to work as indoor positioning systems with no modification to the existing hardware.

## Topology
#### Packet Tracer - Configuring Wireless LAN Access

![Topology](https://user-images.githubusercontent.com/77826589/118360461-46fab980-b5a5-11eb-89af-2b67605a3372.png)

### Addressing Table

![Addressing Table](https://user-images.githubusercontent.com/77826589/118360494-84f7dd80-b5a5-11eb-9e3e-64bc0b55fd8c.png)

## Configuration Wireless LAN Access
#### Objective

Part 1 : Configure a Wireless Router

Part 2 : Configure a Wireless Client

Part 3 : Verify Connectivity

#### Scenario

In this activity, you will configure a Linksys wireless router, allowing for remote access from PCs as well as wireless connectivity with WPA2 security. You will manually configure PC wireless connectivity by entering the Linksys router SSID and password.

#### Part 1 : Configure a Wireless Router
```ruby
Step 1 : Connect the Internet interface of WRS2 to S1.
- Connect the WRS2 Internet interface to the S1 F0/7 interface.

Step 2 : Configure the Internet connection type.
- Click WRS2 > GUI tab.
- Set the Internet Connection type to Static IP.
- Configure the IP addressing according to the Addressing Table.

Step 3 : Configure the network setup.
- Scroll down to Network Setup. For the Router IP option, set the IP address to 172.17.40.1 and the subnet mask to 255.255.255.0.
- Enable the DHCP server.
- Scroll to the bottom of the page and click Save Settings.

Step 4 : Configure wireless access and security.
- At the top of the window, click Wireless. Set the Network Mode to Wireless-N Only and change the SSID to WRS_LAN.
- Disable SSID Broadcast and click Save Settings.
- Click the Wireless Security option.
- Change the Security Mode from Disabled to WPA2 Personal.
- Configure cisco123 as the passphrase.
- Scroll to the bottom of the page and click Save Settings
```

#### Part 2 : Configure a Wireless Client
```ruby
Step 1 : Configure PC3 for wireless connectivity.

Because SSID broadcast is disabled, you must manually configure PC3 with the correct SSID and passphrase to establish a connection with the router.

- Click PC3 > Desktop > PC Wireless.
- Click the Profiles tab.
- Click New.
- Name the new profile Wireless Access.
- On the next screen, click Advanced Setup. Then manually enter the SSID of WRS_LAN on Wireless Network Name. Click Next.
- Choose Obtain network settings automatically (DHCP) as the network settings, and then click Next.
- On Wireless Security, choose WPA2-Personal as the method of encryption and click Next.
- Enter the passphrase cisco123 and click Next.
- Click Save and then click Connect to Network

Step 2 : Verify PC3 wireless connectivity and IP addressing configuration.

The Signal Strength and Link Quality indicators should show that you have a strong signal. Click More Information to see details of the connection including IP addressing information. Close the PC Wireless configuration window.
```

#### Part 3 : Verify Connectivity
```ruby
All the PCs should have connectivity with one another.
```

## Outcome

![1](https://user-images.githubusercontent.com/77826589/118361147-a1951500-b5a7-11eb-838a-97c0f5171674.png)
| :--: |
![2](https://user-images.githubusercontent.com/77826589/118361163-aa85e680-b5a7-11eb-85a9-4e4f0637c1da.png)

## References
- https://courses.cs.ut.ee/MTAT.08.004/2016_spring/uploads/Main/Configuring%20Wireless%20LAN%20access.pdf
- https://en.wikipedia.org/wiki/Wireless_access_point
- https://www.cisco.com/c/en/us/support/docs/wireless-mobility/wireless-lan-wlan/68005-wlan-connect.html
