# Backbone ThIWert
An AKO Project by Gin Havana and AssiKalle

## I. Planning:
**1. Goal:**
The goal is to create a stable network radio connection from the HS-Nordhausen to the ThiWert. The best option should be glass fiber technology and Power over Ethernet if possible.

***1.1. Conditions and requirements:***  
1.1.1. Main consideration:
- Choosing mounting location
  - [x] Which building? Options are building 18, 19 and ThIWert
  - [x] Particular location
- Budget, cost
  - [ ] Maximum budget number
  - [ ] Number of devices needed
- Time
  - Presumably 2 months
  - [ ] Ask for time limit
- Quality requirement
  - Presumably the connection is flawlessly
  - The reliability and a high speed are main issues.
  - [ ] Detail expectation, e.g. bandwidth, etc.

1.1.2. Sub demand and condition:
- Technical details:
  - [x] Glass fiber switch
  - [ ] Ipv4/v6
  - [ ] Mac maybe
  - [ ] other details
- Weather condition
- Obstacle between to access points

***1.2. Premeasured risks:***
- Low budget or hardware has high cost
- In practice it will take more time than limited/expected time
- No suitable mounting point
- Malfunction hardware or inconfigurable software technology
- Bad weather
- To many obstacles interrupting signal
- tbd [^1] due to multiple attempts if fail
[^1]: to be determined.

For mounting option on the roof of the main building, the first difficulty is that the roof does not belong to ThIWert but to landlord and ThIWert does not know exactly if it is available for mounting. For mounting option on top of the heat tower, there are some possible safety risks such as climbing up the tower (? height) and weather condition halfway as well as on the top.

***1.3. Consequences:***
- How willing is the client to take risks?
- What if the project is unsuccessful?

***1.4. Expectation:***
- [ ] Technical hardwares fit planned budget. 
- [x] Glass fiber technology
- [ ] Power over Ethernet technology, e.g. Antenna, Switch, etc.
- [ ] 80m cable is enough
- tbd [^1]

***1.5. Contact details:***  
  1. ThIWert:
     - Prof. Ariane Ruff
     - Admin* Mark Gassmann
  2. Medienzentrum:
     - Fred Wagner
  3. Supervisor:
     - Prof. Dr.-Ing. Thomas Hühn

**2. Rough planning:**
- [x] Distance estimation and calculation and in practice (via Google Earth)
- [x] Height difference (via Google Earth)
- [x] Look for obstacle theoretically and practically
- [ ] Check weather condition
- [ ] Have a meeting to research about conditions and requirements as well as demands
- [ ] Topographic survey
- [ ] Research about routing device that fits budget
- [ ] tbd [^1]

**3. Detail planning:**
- [ ] Research for obstacles e.g. trees or buildings that blocking the direct signal. Can be done by measuring on Google Earth.
- [ ] tbd [^1]

## II. Implementation:
**1. Condition research:**  
Due to known information, there are two variants from which the antenna(s) can be installed. They are building 18 and building 19. Distance will be measured from south side of both buildings, since ThIWert main building ist positioned southern from Campus, and from north side of ThIWert main building. Assuming that installation points can be roughly on the southern wall of buildings 18 and 19 and on northern wall of ThIWert building, the measured/estimated distances via Google Earth are:

|Distance from H18|Distance from H19|Height difference
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

![Ggl_Earth-lib-main](https://user-images.githubusercontent.com/66717834/142769870-bb3dea9f-3266-4d89-a3d2-daaebadc317f.png)
![Ggl_Earth-lib-tower](https://user-images.githubusercontent.com/66717834/142769886-6b143490-8d0b-4b3e-be97-543b18d1b65b.png)


Height difference from library roof (192+ m):
|To main building roof|To heat tower top|
| - | - |
|177+ m|177+ m|

There are 2 server containers that have PoW Switch wired to each other by Glass Fiber cable (? need reconfirmation):
    1. On the second floor of main building, in technical room. There is server box wired directly to the roof of the same building through third floor.
    2. In the main hall near entrance to labor and also near entrance to main building.
    
**3. Practical risks and difficulties:**
1. After the first topology study on November 8th 2021, some difficulties have been notice:
    1. For the mounting option on the roof of ThIWert main building, it is very easy for technician to install antenna. However the roof area does not belong to ThIWert but to landlord. There is no confirmed information that the roof is available for antenna installation, yet rumor that the landlord is planning on using the roof for something else (? need reconfirmation). Another difficulty is that even if the roof is available, from the study experience and proofs such as photos of views to estimate initial signal direction in addition with Google Earth view comparision, there is high chance of obstacles, most obvious trees, blocking the signal wave.
![Ggl_Earth-signal-blockers](https://user-images.githubusercontent.com/66717834/142770088-7826b05e-a090-480d-961d-1851048cf623.png)
*the bold area has the most potential of obstacles (trees, etc.) blocking signal*
![2021_11_08_ThIWert_view-to-campus-horizontal_true-POV](https://user-images.githubusercontent.com/66717834/142769629-734763b0-18b0-430f-baf0-5993ff730ff3.jpg)
![Ggl_Earth-signal-pov](https://user-images.githubusercontent.com/66717834/142769712-cfa2c279-1a2b-4135-bf6f-6e36c6256cab.png)



