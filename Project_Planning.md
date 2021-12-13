    1. Update November 29th 2021: Thomas the supervisor had ordered an uninterrupted power suply (UPS) for Installation Test.
  Design Hardware and Software setup: 
  - 2 PoE antennas with ip 
  ```
  192.168.88.3/24
  ```
  and
  ```
  192.168.88.4/24
  ```
  
  Plan for pratical test installation has also been drafted:
  - 1 antenna is planned to be set on top of staircase in Campus next to the Library, aka neareast posible test position.
  - 1 antenna is planned to be set on either floor of ThIWert roof or on the wall of the small entrance to the roof.
  
  Connection between 2 antennas must be configured and tested.
  After power plugged in and antennas wired to laptops, we have to set our own ethernet0 ipv4. I choose 
  ```
  192.168.88.110
  ```
  and AssiKalle choose
  ```
  192.168.88.100
  ```
  We ping to each other's antenna at 192.168.88.3 and 192.168.88.4 respectively. There is no package loss.
  Devices interface is accessed via
  ```
  192.168.88.3
  ```
  and
  ```
  192.168.88.4
  ```
  with username:
  ```
  root
  ```
  and password:
  ```
  Sommer4
  ```
  Configuration is performed by Windows Commandline/PowerShell and WSL Ubuntu. We use iperf commandline, where one opens a connection as server via Ubuntu
  ```
  iperf3 -s [ipv4]
  ```
  or PowerShell/Cmd
  ```
  iperf3.exe -s [ipv4]
  ```
  ![iperf-s-110](https://user-images.githubusercontent.com/66717834/145724225-11863f88-76f1-41d3-9ecf-4fe693fffced.jpeg)
  
  and the other connects to that server as client via Ubuntu
  ```
  iperf3 -c [ipv4] -p [port]  
  ```
  or via PowerShell/Cmd
  ```
  iperf3.exe -c [ipv4] -p [port]  
  ```
  ![iperf-c](https://user-images.githubusercontent.com/66717834/145724197-73d7d01e-2b3e-41ef-bdb0-2e146d75343d.jpeg)

  There was 1 unknown technical issue that at some early attempts we couldn't ping directly to each other, only to the antennas. Both devices could also not connect to each other via iperf3.
  
    2. Update December 6th 2021:
  After whole session trying to find the cause for not connectable, we have found out that the problem was that cables were loosely plugged in PoE Antennas outlets, so that not all lamps lighted up and the Antennas did not function properly, particularly did not generate signal. After few attempts with different cables and holding positions, we manage to light up all the router lamps. Therefore connection has been established as shown from 2 photos above.
    3. Update December 13th 2021:
  Thomas has ordered 2 new antennas Airfiber Ubiquiti 60LR for test performance with radio signal 60GHz. After assembling components we have to set up new username
  ```
  root
  ```
  and new password
  ```
  Nordhausen2021
  ```
  for the 2 antennas.
  The default ip for this device is
  ```
  192.168.88.20/24
  ```
  so I set one to
  ```
  192.168.88.30
  ```
  and the other to
  ```
  192.168.88.40
  ```
  Following Thomas instruction, I have update the Firmware to both antennas to 
  ```
  GP.V2.6.0-BETA3.46505.211208.1235
  ```
