
**OSI Model**
1. Physical layer - does the transportation of the bytes through cables in form of electric signals which then gets converted to digital data then passed on to the data link layer thus the name physical 
2. Data link layer -if the transfer of data is within an network it uses the mac addr which comes with the data packet to determine the destination addr  and send the data Accordingly and source addr if it needs to reply to the sender switches and hubs are used in this layer 
3. Network layer -similar to the data link layer but this time it’s between different networks and instead of mac addr ip addr are used to find the destination of the data and also the source addr for replying routers are used in this layer 
4. Transport layer -the data cant be sent whole so it’s sent in blocks and thus this is the layer where it gets arranged in the order and as disassembled when sending the data 
5. Session layer - as the name suggests it maintains the session between the browser client and the server though cookies and also this where the email client knows which data should be sent to different applications this is done through destination ports and source ports if the app Wants to send smh to the server 
6. Presentation layer - what this layer does that makes the data readable by converting the data from an unsupported format to an which is supported by the email client but since today’s browser clients can read most of the data this is pretty useless in most cases 
7. Application layer -this refers to the actual application to which the users interact 

The packets sent are in the form of one’s and zeros whether through electrical signals as on and off through coax or twisted pair, light source as on or off from fibre optic and if it’s through wireless it’s through RF(radio frequency)signals and these aren’t sent in whole they are an chunks (1500 bytes) 

An MAC addr is an 48 bit unique hexadecimal for an NIC(network interface card) which gives itself an addr 

The first part contains the manufacturer identifier(24 bit) 
And the Second part is the unique identifier of that NIC

 It is used to know whether an packet is sent to it or any other device on the network these have src mac addr and dest addr
 And CRC(cyclic redundancy check) which sees whether it’s an bad packet or not and if it’s an bad one it’s then resent 

![[Pasted image 20250227071622.png]]

One example where this is used is that when an device is newly connected to an network to know the mac addr of all the other devices on that network it sends out an broadcast message 

But when communicating between two different networks MAC addresses aren’t helpful as they
1. Cause too much broadcast traffic when more computers are added 
2. Can’t identify the devices in different networks 

This is where logical addressing is used which is mostly IP addressing 
Which is not burned In to the NIC as mac does and in this routers are used to connect to another network and these routers store the ip addresses of other networks amd these are stored In an table called routing table and an ip packet doesn’t change 

![[Pasted image 20250227161037.png]]
TCP does the checking of packets whether it’s successfully sent to the destination if it’s lost TCP sends that particular packet again 

**Network** **topologies**
There are two types of network topologies 
1. Physical topology -this actually shows the connections of the devices in an particular network (their locations, how it’s connected, etc…)
2. Logical topology - this shows how the data is actually transmitted between devices in an network 
Bus topology: an single cable to which all the devices are connected 
- Single point of failure(cables)
- The cable’s bandwidth is shared between the devices connected to the network 

Ring topology:
- As the name suggests the devices are connected in rings 

![[Pasted image 20250227164412.png]]

- when the cables between the devices fail only the devices on either side would get affected 
- Nowadays this is hardly in use

 Star topology(hub and spoke)
 - it’s an commonly used topology compared to the others we have seen here 
 - It has an centralised system from which the data is transferred in the network (usually an switch or an hub is used)
 - Has an single point of failure 

Mesh topology 
- As the name suggests mesh is an mess of cables 
- It connects every device to every others in the network 
- If any failure occurs in the cable near an computer only that computer is affected thus high availability 

Hybrid topology
- uses two different topology and merge them to suit their needs

Star bus topology 
- Combines capabilities of both star and bus topologies


**CABLES**

Coaxial cable 
- Rated through radio grade (RG)
- The most common cable used today is RG-6 and the one used before is RG-59
- One of the oldest cables used 
- Has two types F-type and BNC type(usually not used)
- it comprises of 4 parts 
1. Inner core (copper)
2. Insulator
3. Outer core 
4. Outer sheathing(PVC)
- There’s also another type of cable called twinax cable which has two cores an inner core and an outer core 

**Twisted** **pair** **cable**
- has two types of twisted pair 
1. Shielded twisted pair 
2. Unshielded twisted pair (which as extra layer of protection of the twisted pairs of cables inside the PVC)
- One Of the most used types of cables 
- It’s basically 4 pairs of cables twisted together and covered with an PVC sheathing inside the cables there is an thin copper core similar to coaxial cable 
- Comprises of
1. Thin cores 
2. The cables which covers the cores
3. PVC sheathing 
- Connected through an RJ-45 connector 
- The speeds of the twisted pair are categorised by CAT ratings 
- ![[Pasted image 20250301070443.png]]

Fiber optic 
- Along with twisted pair this is also one of the commonly used cabling 
- There are two types of fiber optic cables 
1. Multi-mode -it uses led as an light source and it travels less distances than single mode 
2. Single mode -it uses laser as an light source and it travels long distances 
- And fiber optic cables can be both half duplex and full duplex in half duplex has capability to only send or receive at one point of time whereas full duplex can do both receive and send at the same time 
- Multi-mode has orange coloured cables and single mode has yellow coloured cables 
- The different types of connecters found in fibre optics are 
1. ST connector 
2. SC connector 
3. ST connector 
4. FC connector 
5. LC connector 
6. MT-RJ connector 

Fire ratings 
1. Plenum-high resistance to fire (used to run wires between the roof and the drop ceiling )
2. Riser - medium resistant to fire (used to run wires between floors )
3. PVC - no resistance to fire 

Ethernet in its lowest level an book called IEEE 802.3 which contains the all the things you need to create an Ethernet network 
And through the years even if the book is changed the frame which contains the data haven’t changed so it’s all the same

# 10BASE5
Here 10 means the speed of the connection in mbps
and base means all the bandwidth is used in the connection and the last “5” means the length of the network here 5 means 500 meters and n


Frame check sequence is the same as CRC
![[Pasted image 20250305071711.png]]

Carrier sense multiple access/collision detection (csma/cd)
Used to detect collisions in an network where an hub is used and all the computers in that network doesnt send any Data till the randomly generated time which is in milliseconds 

**Connecting switch**
- Doing this will increase the size of our network 
- to connect two switches together we use cross through cables which has 568A on one side and 568B on the other side
- for other situations an straight through cable Is used 
- Im some switches you can find an uplink which when activated will make the port near to it so that even an straight through cables will work for connecting switches
- nowadays the switches just auto senses what is connected to it and changes accordingly 
- and it also resolves if there’s an switching loop

![[Pasted image 20250307072335.png]]
And the protocol which is used is STP(spanning tree protocol) which uses bridge protocol data units which is an frame and uses this to determine where there is an switching loop or not 

**100BASET**

- Replaced 10BASET and to use this new speed there was an need to upgrade to switches instead of hubs 
- moving from half duplex to full duplex also occurred during this time 
100BaseT4
- Used cat3
- Can contain 1024 nodes 
- Hubs are used 
- The max distance between two nodes is 100m 
- 100 mbps and for the first time used all four pairs of the twisted pair cable and its half duplex 
100BaseTX
- everything is the same except cat5e is used for cables and only utilities two of the four pair of the UTP
- Full duplex 
- Now this is just called 100BaseT
100BaseFX
- uses multimode fiber cables
- max distance is 2km
- Other specs are the same 

**Transceivers** aka adapters 
In utp there was no need of these since all used the same RJ45 connector but in fiber optics there was many different connectors 
SC, ST, etc.. and this made it hard to use different connectors on s single switch thus these modules were made to make it compatible 
**Types**
- GBIC - gigabit interface converter (used for SC and ST)
- SFP-small form factor pluggable (used for LC)
- SFP+ - the same as SFP but it’s improved 
- QSFP-quad small factor pluggable used for 40gigabit connections 