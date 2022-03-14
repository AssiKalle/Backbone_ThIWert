# Backbone ThIWert
An AKO Project by Gin Havana and AssiKalle

# Table of contents:
1. Introduction
2. Planning:  
2.1. Conditions and requirements:  
  2.1.1. Main consideration  
  2.1.2. Requirements  
2.2. Etwas
3. Implementation
4. Validation
5. References

## 1. Introduction:
The [Thüringer Innovationszentrum für Wertstoffe (ThIWert)](https://www.hs-nordhausen.de/forschung/thiwert/) is a partner of Thuringian industry and commerce and also of regional and supra-regional research institutions, colleges and universities, funded by the Free State of Thuringia and is co-financed by the European Regional Development Fund (ERDF). There should be Internet service provided for ThIWert building by individual ISP, however being a part of Hochschule Nordhausen, it is neccessary that ThIWert connects directly to Campus and is able to use the Internet through Campus's server.

## 2. Planning:
The goal for this project is to create a stable, highspeed internet connection between the HS-Nordhausen and the ThIWert. 

**2.1. Conditions and requirements:**

***2.1.1. Main consideration:***
- Location:

| Mounting location | Campus Nordhausen | ThIWert |
| - | - | - |
| Chosen | Library roof | still provition |
- Budget, cost:

| Name | Amount | Total cost |
| ---- | ---- |---- |
| PoE Antennas Airfiber Ubiquiti 60 LR | 2 | €798 |
| (Battery) APC Back-UPS Es | 1 | €138|

- Time: Estimated time required for full project is one semester.

***2.1.2. Requirements:***

Firstly, it is required that the connection between LAN Network in ThIWert and Campus Nordhausen is flawless and reliable, in other word it is stable with least interruption.

It is also expected that with this connection, the internet speed should also be highspeed. To achieve this expectation, there are some advance technical requirements that need to be fullfilled. The first technical requirement is glass fiber as medium for cabling. Since glass cores are efficient at transmitting light and allow for significantly higher transfer speeds, glass fibers can be used over long sensing distances.  
Next is Power Over Ethernet (PoE) technology for many cost efficient reasons: There is no need for a separate electrical supply line so there is a substantial reduction in installation labor cost. Secondly, the infrastructure of PoE is quite safe. Power Sourcing Equipment (PSE) devices only supply power when they detect the presence of a PoE-enabled device. Otherwise, there is no power delivered along the line keeping both users and the equipment safe from shocks and overloads. Furthermore, PoE devices can be enabled to automatically shut down at night, remotely reset to collect relevant information from network devices such as servers, printers, hubs, switches. All of this can be managed efficiently through a Simple Network Management Protocol (SNMP). And finally, a PoE system can be attached to an uninterruptible power supply (UPS). This fact means that mission-critical systems can be assured of a constant power supply even if regular electrical service is interrupted.  
The last technical requirement and also expectation is the established connection can be reach and maintain between 2 Antennas with signal frequency of 60 GHz. However it is also acceptable if the connection can not be established with 60 GHz and only with 2.4/5GHz.

The durability of the signal under different weather conditions as well as possible obstacle between antennas mounting locations should be noticed.

***2.1.3. Predicted risks:***

With all the requirements, it is predicted that the budget will not fit the cost for hardwares. In this situation it is acceptable that some technical requirements can not be met. It is also predicted to taken more time to finish the project because project had started in winter, therefore it is highly possible that the weather condition will not support the implementation. There can be some problems occur in preparation phase such as malfunction hardware or inconfigurable software technology, which also cost more time and budget to replace, repair or reconfig. In execution phase, it is expected to have to many obstacles between ThIWert and campus interrupting signal, or there are no suitable mounting point.

**2.2 Rough planning:**
- [x] Distance estimation and calculation and in practice
- [x] Look for obstacle theoretically and practically
- [x] Check weather condition
- [x] Have meetings to research about conditions and requirements as well as demands
- [x] Topographic survey
- [x] Research about routing device that fits budget
- [x] Perform test installation

**2.3. Detail planning:**  
For distance estimation, Google Earth is optimal. After topographic survey, information has been compared with estimated data for correction.  
Presumably maximum 3 to 4 appointments are required for topology research for exact locations and views as well as signal direction of mounting options and possible weather condition. There are also some details needed to notice such as cable access, estimated length of cable, technical devices, etc.  
To reduce additional power suply, it is fairly good if Power over Ethernet technology is applied. For safety purpose, PoE Antenna should have max 48V DC. The best option to transmit internet signal to end devices is Glass Fiber.  
Test installation and configuration of PoE Antennas should be prepared in Labor.
Practical installations should also take 3 to 4 appointments to adjust technical details e.g. signal direction, practical devices configuration, etc.
Performance and durability test should be performed after practical installations.

**2. Topology planning:** 
There are 2 options of antenna mounting location at ThIWert:
    1. On the roof of the main building
    2. On top of the side tower  
The first optimal option which had been studied is Library roof's bottom right corner (via Google Map/Earth).

The true distances measured from Library via Google Earth are:
|To main building roof|To heat tower|
| - | - |
|1.45 km|1.4 km|

![Ggl_Earth-lib-main](https://user-images.githubusercontent.com/73235656/148754880-eb0698a9-0673-4b60-ab5e-603409d5ca8a.png) [^2]
[^2]: Distance to main building roof.

![Ggl_Earth-lib-tower](https://user-images.githubusercontent.com/73235656/148755349-722fc940-5aa9-4718-9bc3-a41f31d546a9.png)[^3]
[^3]: Distance to heat tower.

There are 2 server containers that have PoE Switch wired to each other by Glass Fiber cable (? need reconfirmation):
  1. On the second floor of main building, in technical room.  
<img src="https://user-images.githubusercontent.com/66717834/142770168-a310233f-71ac-486b-8e06-2ad119a2a335.jpg" alt="2021_11_08_ThIWert_main-building-server-box-with-glasfaser" width="350"/>&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/66717834/142770181-754292b9-e235-41f8-8eaf-fb94df8c03fa.jpg" alt="2021_11_08_ThIWert_main-building-server-box-with-glasfaser1" width="350"/>  
There is server box wired directly to the roof of the same building through third floor, connected to an existing antenna on the opposite direction to campus.  
<img src="https://user-images.githubusercontent.com/66717834/142770314-19352f52-9759-4e25-ba16-da2346538732.jpg" alt="2021_11_08_ThIWert_Roof_example-antenna" width="350"/>

  2. In the main hall near entrance to labor and also near entrance to main building.  
<img src="https://user-images.githubusercontent.com/66717834/142770735-e710415a-bab3-4bb0-8c4d-f59007579c55.jpg" alt="2021_11_08_ThIWert_Server-case-main-hall" width="300"/>&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/66717834/142770768-8eac2527-e6ad-4c2a-8e92-786f55840c3c.jpg" alt="2021_11_08_ThIWert_POE-Switch-Fastiron-Edge-2402-POE" width="500"/>

**4. Contact details:**
1. ThIWert:
   - Prof. Ariane Ruff
   - Admin* Mark Gassmann
2. Medienzentrum:
   - Fred Wagner
3. Supervisor:
   - Prof. Dr.-Ing. Thomas Hühn

## 3. Implementation:

**3.1. Condition research and preparation:**  
Due to known information, there are two variants from which the antenna(s) can be installed. They are building 18 and building 19. Distance will be measured from south side of both buildings, since ThIWert main building is positioned southern from Campus, and from north side of ThIWert main building. Assuming that installation points can be roughly on the southern wall of buildings 18 and 19 and on northern wall of ThIWert building, the measured/estimated distances via Google Earth are:

|Distance from H18|Distance from H19|Height difference|
| - | - | - |
|1.37 ~ 1.41 km|1.35 ~ 1.39 km|10 ~ 11 m|

There is low chance of any posible obstacle blocking signal.

**3.2. Practical risks and difficulties:**
After the first topology study on November 8th 2021, some difficulties have been notice:

- For the mounting option on the roof of ThIWert main building, it is very easy for technician to install antenna. However the roof area does not belong to ThIWert but to the landlord. There is no confirmed information that the roof is available for antenna installation, yet rumor that the landlord is planning on using the roof for something else (? need reconfirmation). Another difficulty is that even if the roof is available, from the study experience and proofs such as photos of views to estimate initial signal direction in addition with Google Earth view comparision, there is high chance of obstacles, most obvious trees, blocking the signal wave.
![Ggl_Earth-signal-blockers](https://user-images.githubusercontent.com/66717834/142770088-7826b05e-a090-480d-961d-1851048cf623.png)
*the bold area has the most potential of obstacles (trees, etc.) blocking signal*
![2021_11_08_ThIWert_view-to-campus-horizontal_true-POV](https://user-images.githubusercontent.com/66717834/142769629-734763b0-18b0-430f-baf0-5993ff730ff3.jpg)
![Ggl_Earth-signal-pov](https://user-images.githubusercontent.com/66717834/142769712-cfa2c279-1a2b-4135-bf6f-6e36c6256cab.png)

- For the mounting option on top of the heat tower, some risks have first been notice. The tower is very high with mostly no protective devices or method. Weather condition is also in concern. Technician has to climb up the tower which requires hiring professional technician and safety gears or personal protective equiments, which demand  extra cost. The distance between the tower and server box is also far. This option is therefore high risk high cost and should only be deadend solution.
    
- For mounting option in campus, tbd [^1]

https://user-images.githubusercontent.com/66717834/142772420-a6c32e5f-44b6-4808-81d0-4b37938e5b4f.mp4

**3.3. Installation:**
1. Prediction:
After discussing with supervisor, the conclusion is that Laser 60 GHz is theoretically impossible to transmit signal direct through objectives like trees, so the first solution is using Laser 5 GHz and if it is still not possible then Laser 2.4 GHz. There are 2 sample antennas 5 GHz in Labor so that a temporary installation is possible.
In ThIWert, there are 2 possible place on the roof of main building that will be tested for mounting: On the wall of the small entrance or on the ground of the roof.
Antenna will also be set on the top of the staircase next to the entrance of the library (possible nearest to the planning mounting point)

2. Preparation for Live Experiment:  
Design Hardware and Software setup:  

| -------- | PoE antennas (GHz) | Device IPv4      | ethernet0 IPv4 | username | password       | Firmware                          |
| -------- | ------------------ | ---------------- | -------------- | -------- | -------------- | --------------------------------- |
| THIWert       | 5                  | 192.168.88.3/24  | 192.168.88.110 | root     | Sommer4        | --------------------------------- |
| THIWert | 60                 | 192.168.88.30/24 | 192.168.88.30  | root     | Nordhausen2021 | GP.V2.6.0-RC.46590.211230.1238 |
| HS | 5                  | 192.168.88.4/24  | 192.168.88.100 | root     | Sommer4        | --------------------------------- |
| HS | 60                 | 192.168.88.20/24 | 192.168.88.40  | root     | Nordhausen2021 | GP.V2.6.0-RC.46590.211230.1238 |

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

## 4. Validation:
### 1. First attempt January 24th 2022:
1. Installation in ThIWert (A good provision):  
The appointment meeting for mounting atempt is 8 am and it is expected to take 1 to 2 hour(s) to finish. Two antennas, each for different bandwidth 
After arriving at ThIWert and on the roof, it is required that we recheck the photos for estimated signal direction. Thomas has suggested that we choose the closer edge of the entrance to Campus direction as first mounting option, which is 380cm away from the entrance. Thomas has also help with the drilling through a 27cm thick wall to set up the antenna holder and a way for 2 testing cables to go through.

<img alt="Thomas-drilling" src="https://user-images.githubusercontent.com/66717834/151765358-a33526f1-06ca-4c34-8fc2-c19f1ff9f60e.jpeg" width="500px">

After fixing the antenna holder, 2 antennas are mounted where the 5GHz is set below and the 60GHz is set above.

<img alt="Test-build" src="https://user-images.githubusercontent.com/66717834/151766715-7e5c6d60-954d-45b8-8580-06cb050e2096.jpeg" width="450px"><img alt="Test-build1" src="https://user-images.githubusercontent.com/66717834/151767057-0be70c3d-3cfd-4e9c-9ef3-3527e34b0458.jpeg" width="450px">

Signal direction is estimated by placing one head of the drill fix on the antenna holder and pointing the other head following the pre-estimated direction with Google Earth.

<img alt="Estimated-direction" src="https://user-images.githubusercontent.com/66717834/151767803-75076df3-8cb3-49b0-9b86-37dc4e5c1354.jpeg" height="600px">

After plugging in the two cables, Thomas set up the position for the cable to run straight to the POE Switches Lan Port while the POE Port is connected to a 4900 TPLink Router as Power and Internet source. Two cables are binded together from which the cable connect to the 60GHz is marked blue and the other is mark red. Valerius has examined and verified through the web interface that both antenna function correctly. These antennas will be tested as transmitter.

2. Antenna temporary set up and signal testing in Campus:  
Thomas has asked the house keeper for a big tripod to temporary set up antenna on top of staircase. Due to visible obstacles only antenna 5GHz has been used for testing as receiver. Power is provided by uninterrupted power suplier (UPS). Signal strength is tested by adjusting tripod position and antenna direction and displayed on Valerius laptop web interface. It is recorded that minimum average for constant signal strength can vary between 1 to 7 Mbps and maximum average can reach between 40 to 70 Mbps and then decrease. There are two times the signal has jumped up to 330 Mpbs for shorter than a second. 

3. Conclusion:  
Bad weather condition and clearly visible obstacles are the most possible reason for bad signal records. Secondary reason can be incorrect set up antennas direction between ThIWert and staircase in Campus.

4. Solution:  
First solution is another performance test on the roof of library where the vision is clearer with less chance of obstacles. Additional solution is to re-adjust antennas direction in ThIWert.
## 5. References:
References collection:https://www.zotero.org/groups/4479602/backbone_thiwert/library
