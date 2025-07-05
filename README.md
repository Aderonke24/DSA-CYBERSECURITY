# DSA-CYBERSECURITY
### Capstone project: Cybersecurity on DSA platform
### The project instruction is given below:
---
---

   ### ***Project Type***  
Individual project only. No group work is allowed.
---
---

### Project Breakdown
You are required to complete the following tasks:

***Task 1*** (Compulsory): Set up a fully functional virtual cybersecurity lab.

***Task 2*** (Compulsory): Analyze an Android forensic image and produce a professional investigation report.

***Task 3*** (Optional for Bonus Points): Deploy a virtual firewall to simulate an enterprise-grade network security environment.

---
---
## **Task 1: started by downloading all the executable files needed for this project**

- A. I downloaded and Extract:
- 1. Virtualbox (it didn't work on my system, I opted in for Hyper-V manager on my Windows O/S) [Download Here](https://www.virtualbox.org)


     For Hyper-V


  - I enabled Hyper-V by going to: on the Search bar, type "Turn Windows Features On or Off" to launch Windows Features
     - check the box next to Hyper-V and click Ok.
     - The laptop was restarted to effect the change.
- 2. Windows 10 ISO file (to be installed on one of the virtual machines created on the Hyper-V) for Virtualbox, [Download Here](https://www.microsoft.com/en-us/software-download/windows10)
 - 3. Kali linux [Download Here](https://www.kali.org/get-kali/#kali-platforms)
- B. ## ***CREATION OF TWO VIRTUAL MACHINES***
  - 1. Virtual Machine for Windows 10 (Named: "Lab")
       - Open Hyper-V manager and Click "New" in the left pane and select "Virtul machine", follow the instructions to create the virtual machine.
       - Specify name (Lab) and location
       - specify generation
       - allocate RAM
       - configure Network by choosing the switch
       - connect to virtual Hard Disk
       - install Windows 10 :
          - Right click the new virtual machine (Lab) and select "settings"
          - Expand IDE controller and select DVD Drive
          - click browse to select the downloaded Windows ISO file
          - click Ok to save settings
          - start the virtual Machine and follow the instructions to install Windows 10.
          - after installation,right click on the new virtual machine(Lab) and select "connect"
          - Adjust the display resolution
          - sign in to the new Virtual Machine.
     - 2. Virtual Machine for Kali Linux (Named: "Kali Linux")
       - Open Hyper-V manager and Click "New" in the left pane and select "Virtul machine", follow the instructions to create the virtual machine.
       - Specify name (Kali Linux) and location
       - specify generation
       - allocate RAM
       - configure Network by choosing the switch
       - connect to virtual Hard Disk
       - install Kali Linux :
          - Right click the new virtual machine (Kali Linux) and select "settings"
          - Expand IDE controller and select DVD Drive
          - click browse to select the downloaded Kali Linux VHDX file
          - click Ok to save settings
          - start the virtual Machine, Kali Linux loads automatically because it has been pre-installed in the VHDX image file.
          - right click on the new Virtual machine in Hyper-V manager and select "connect"
          - Adjust the display resolution
          - Log in with the default credentials "kali" for both username and password.
          ### ***FUNCTIONAL VIRTUAL CYBERSECURITY LAB SET UP***
 
     
         - Create a virtual Switch: Private Switch (for communication between the Virtual machines **ONLY** usually for testing attack scenerio and External Switch (Ta gain access to the internet)  
         - Connect both virtual Machines to thesame switch for them to communicate.
           - Right click the Virtual Machine individually
           - select "settings"
           - select "Network Adapter" on the Right pane
           - choose the Virtual switch from the drop down on the Left pane
           - click ok.
         - configure the IP address for the Virtual machines individaully
           - For Kali Linux Virtual machine:
             - on the Root Terminal, Run ``` ifconfig  ```  to see the list of network interfaces and their current settings, IP addresses, netmasks and broadcast addresses.
             - take note of the interface you are to configure e.g., eth0, lo
             - Run ``` ifconfig lo 10.10.10.2 netmask 255.255.255.0 ```  to change the IP address.
           - For Windows 10 Virtual machine:
             - go to Network settings
             - Right click the Adapter and select properties
             - click change network adapter
             - select IPV4
             - check the Static box
             - enter the IP and subnet mask: 10.10.10.1 and 255.255.255.0 respectively.
             - click ok
           - open Root Terminal on kali Linux and Command prompt on Windows virtual machines.
           - ping the IP address (10.10.10.1) of Windows virtual Machine on Kali.
           - ping the IP address of Kali (10.10.10.2) on Windows
         -  if both can communicate through ping command or share file, the virtual security lab has been created.


Command

 ```
 ping 10.10.10.1

 ```

 ```
 ping 10.10.10.2

 ```


---
---

## **Task 2: Analyze an Android forensic image and produce a professional investigation report**



