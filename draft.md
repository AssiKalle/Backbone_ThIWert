# Backbone ThIWert
An AKO Project by Gin Havana and AssiKalle

## 1. Planning:
**1. Goal:**
The goal is to create a stable network radio connection from the HS-Nordhausen to the ThiWert. 

***1.1. Conditions and requirements:***  
1.1.1. Main consideration:

- Choosing mounting location
  - [x] Campus Nordhausen: Library roof
  - [ ] Within ThIWert:
- Budget, cost:

| Name | Amount | Total cost |
| ---- | ---- |---- |
| PoE Antennas Airfiber Ubiquiti 60 LR | 2 | €798 |
| (Battery) APC Back-UPS Es | 1 | €138|

- Time: Estimated time required for full project is one semester.
- Quality requirement
  - Presumably the connection is flawlessly
  - The reliability and a high speed are main issues.
  - [ ] Detail expectation, e.g. bandwidth, etc.

1.1.2. Sub demand and condition:
- Mounting conditions:
  - [x] Distance between location
  - [ ] Safety
  - [ ] Topology
- Technical details:
  - [x] Glass fiber
  - [x] PoE Switch
  - [ ] Choose Laser 5/2.4 GHz
  - [x] PoE Antenna
  - [x] Ipv4/v6
  - [ ] Durability of antenne under weather condition
  - [ ] other details
- Weather condition
  - [ ] Wind speed on install day
- Obstacle between mounting location

***1.2. Premeasured risks:***
- Low budget or hardware has high cost
- In practice it will take more time than limited/expected time
- No suitable mounting point
- Malfunction hardware or inconfigurable software technology
- Bad weather
- To many obstacles interrupting signal
- tbd [^1] due to multiple attempts if fail
[^1]: to be determined.

***1.3. Consequences:***
- How willing is the client to take risks?
- What if the project is unsuccessful?

***1.4. Expectation:***
- [ ] Technical hardwares fit planned budget. 
- [x] Glass fiber technology
- [x] Power over Ethernet technology, e.g. Antenna, Switch, etc.
- [ ] 80m cable
- tbd [^1]

**2. Rough planning:**
- [x] Distance estimation and calculation and in practice
- [x] Look for obstacle theoretically and practically
- [ ] Check weather condition
- [x] Have meetings to research about conditions and requirements as well as demands
- [x] Topographic survey
- [ ] Research about routing device that fits budget
- [ ] Perform test installation
- [ ] tbd [^1]

**3. Detail planning:**  
For distance estimation, Google Earth is optimal. After topographic survey, information has been compared with estimated data for correction.  
Presumably maximum 3 to 4 appointments are required for topology research for exact locations and views of mounting options and possible weather condition. There are also some details needed to notice such as cable access, estimated length of cable, technical devices, etc.  
To reduce additional power suply, it is fairly good if Power over Ethernet is applied. For safety purpose, PoE Antenna should have max 48V DC. The best option to transmit internet signal to end devices is Glass Fiber.  
Test installation and configuration of PoE Antennas in Labor.

tbd [^1]

**4. Contact details:**
1. ThIWert:
   - Prof. Ariane Ruff
   - Admin* Mark Gassmann
2. Medienzentrum:
   - Fred Wagner
3. Supervisor:
   - Prof. Dr.-Ing. Thomas Hühn

## 2. Implementation:

**1. Condition research and preparation:**  
Due to known information, there are two variants from which the antenna(s) can be installed. They are building 18 and building 19. Distance will be measured from south side of both buildings, since ThIWert main building is positioned southern from Campus, and from north side of ThIWert main building. Assuming that installation points can be roughly on the southern wall of buildings 18 and 19 and on northern wall of ThIWert building, the measured/estimated distances via Google Earth are:

|Distance from H18|Distance from H19|Height difference|
| - | - | - |
|1.37 ~ 1.41 km|1.35 ~ 1.39 km|10 ~ 11 m|

There is low chance of any posible obstacle blocking signal.

**2. Topology implementation:**  
1. The first topology research was on November 8th 2021.  
There are 2 options of antenna mounting location at ThIWert:
    1. - [ ] on the roof of the main building
    2. - [ ] on top of the side tower
The first optimal option which had been studied is Library roof's bottom right corner (via Google Map/Earth).

The true distances measured from Library via Google Earth are:
|To main building roof|To heat tower|
| - | - |
|1.45 km|1.4 km|

![Ggl_Earth-lib-main](https://user-images.githubusercontent.com/66717834/142769870-bb3dea9f-3266-4d89-a3d2-daaebadc317f.png) [^2]
[^2]: Distance to main building roof.

![Ggl_Earth-lib-tower](https://user-images.githubusercontent.com/66717834/142769886-6b143490-8d0b-4b3e-be97-543b18d1b65b.png)[^3]
[^3]: Distance to heat tower.

There are 2 server containers that have PoE Switch wired to each other by Glass Fiber cable (? need reconfirmation):
  1. On the second floor of main building, in technical room.  
<img src="https://user-images.githubusercontent.com/66717834/142770168-a310233f-71ac-486b-8e06-2ad119a2a335.jpg" alt="2021_11_08_ThIWert_main-building-server-box-with-glasfaser" width="350"/>&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/66717834/142770181-754292b9-e235-41f8-8eaf-fb94df8c03fa.jpg" alt="2021_11_08_ThIWert_main-building-server-box-with-glasfaser1" width="350"/>  
There is server box wired directly to the roof of the same building through third floor, connected to an existing antenna on the opposite direction to campus.  
<img src="https://user-images.githubusercontent.com/66717834/142770314-19352f52-9759-4e25-ba16-da2346538732.jpg" alt="2021_11_08_ThIWert_Roof_example-antenna" width="350"/>

  2. In the main hall near entrance to labor and also near entrance to main building.  
<img src="https://user-images.githubusercontent.com/66717834/142770735-e710415a-bab3-4bb0-8c4d-f59007579c55.jpg" alt="2021_11_08_ThIWert_Server-case-main-hall" width="300"/>&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/66717834/142770768-8eac2527-e6ad-4c2a-8e92-786f55840c3c.jpg" alt="2021_11_08_ThIWert_POE-Switch-Fastiron-Edge-2402-POE" width="500"/>

**3. Practical risks and difficulties:**
After the first topology study on November 8th 2021, some difficulties have been notice:

1. For the mounting option on the roof of ThIWert main building, it is very easy for technician to install antenna. However the roof area does not belong to ThIWert but to the landlord. There is no confirmed information that the roof is available for antenna installation, yet rumor that the landlord is planning on using the roof for something else (? need reconfirmation). Another difficulty is that even if the roof is available, from the study experience and proofs such as photos of views to estimate initial signal direction in addition with Google Earth view comparision, there is high chance of obstacles, most obvious trees, blocking the signal wave.
![Ggl_Earth-signal-blockers](https://user-images.githubusercontent.com/66717834/142770088-7826b05e-a090-480d-961d-1851048cf623.png)
*the bold area has the most potential of obstacles (trees, etc.) blocking signal*
![2021_11_08_ThIWert_view-to-campus-horizontal_true-POV](https://user-images.githubusercontent.com/66717834/142769629-734763b0-18b0-430f-baf0-5993ff730ff3.jpg)
![Ggl_Earth-signal-pov](https://user-images.githubusercontent.com/66717834/142769712-cfa2c279-1a2b-4135-bf6f-6e36c6256cab.png)

2. For the mounting option on top of the heat tower, some risks have first been notice. The tower is very high with mostly no protective devices or method. Weather condition is also in concern. Technician has to climb up the tower which requires hiring professional technician and safety gears or personal protective equiments, which demand  extra cost. The distance between the tower and server box is also far. This option is therefore high risk high cost and should only be deadend solution.
    
3. For mounting option in campus, tbd [^1]

https://user-images.githubusercontent.com/66717834/142772420-a6c32e5f-44b6-4808-81d0-4b37938e5b4f.mp4

**4. Installation:**
1. Solution:
After discussing with supervisor, the conclusion is that Laser 60 GHz is theoretically impossible to transmit signal direct through objectives like trees, so the first solution is using Laser 5 GHz and if it is still not possible then Laser 2.4 GHz. There are 2 sample antennas 5 GHz in Labor so that a temporary installation is possible.
In ThIWert, there are 2 possible place on the roof of main building that will be tested for mounting: On the wall of the small entrance or on the ground of the roof.
Antenna will also be set on the top of the staircase next to the entrance of the library (possible nearest to the planning mounting point)

2. Preparation for Live Experiment:  
Design Hardware and Software setup:  

| -------- | PoE antennas (GHz) | Device IPv4      | ethernet0 IPv4 | username | password       | Firmware                          |
| -------- | ------------------ | ---------------- | -------------- | -------- | -------------- | --------------------------------- |
| DH       | 5                  | 192.168.88.3/24  | 192.168.88.110 | root     | Sommer4        | --------------------------------- |
| -------- | 60                 | 192.168.88.20/24 | 192.168.88.30  | root     | Nordhausen2021 | GP.V2.6.0-BETA3.46505.211208.1235 |
| Valerius | 5                  | 192.168.88.4/24  | 192.168.88.100 | root     | Sommer4        | --------------------------------- |
| -------- | 60                 | 192.168.88.20/24 | 192.168.88.40  | root     | Nordhausen2021 | GP.V2.6.0-BETA3.46505.211208.1235 |

*2.1. Update November 29th 2021:*  
Thomas the supervisor had ordered an uninterrupted power suply (UPS) for Installation Test.  
Plan for pratical test installation has also been drafted:  
- 1 antenna is planned to be set on top of staircase in Campus next to the Library, aka neareast posible test position.
- 1 antenna is planned to be set on either floor of ThIWert roof or on the wall of the small entrance to the roof.
  
Connection between 2 antennas must be configured and tested. After sending pings to each other's antenna no package loss is recorded.  
    
Configuration is performed by Windows Commandline/PowerShell and WSL Ubuntu. We use 'iperf' commandline, where one opens a connection as server via Ubuntu
 
| Software               | Server create        | Client connect                  |
| ---------------------- | -------------------- | ------------------------------- |
| Windows Cmd/Powershell | iperf3.exe -s [ipv4] | iperf3.exe -c [ipv4] -p [port]  |
| WSL Ubuntu             | iperf3 -s [ipv4]     | iperf3 -c [ipv4] -p [port]      |

There was 1 unknown technical issue that at some early attempts we couldn't ping directly to each other, only to the antennas. Both devices could also not connect to each other via iperf3. Connection between admin devices (laptops) through switch is still working.
  
*2.2. Update December 6th 2021:*
After whole session trying to find the cause for not connectable, we have found out that the problem was that cables were loosely plugged in PoE Antennas outlets, so that not all lamps lighted up and the Antennas did not function properly, particularly did not generate signal. After few attempts with different cables and holding positions, we manage to light up all the router lamps. Therefore connection has been established as shown from 2 photos above.
  
*2.3. Update December 13th 2021:*
Thomas has ordered 2 new antennas Airfiber Ubiquiti 60LR for test performance with radio signal 60GHz.

## 3. Operating: not yet
