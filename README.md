UROV
1.	CHAPTER 1                                                                                      	
      Introduction				 
2.	CHAPTER 2                                                           				
2.1 Applications                                                   
2.2 Leading Particular and General Data
3.	CHAPTER 3                                                         				
     Underwater setup and operation guide						 
4.	CHAPTER 4                                                                                         	
     System Specification							
5.	CHAPTER 5                                                                                         	
5.1 Operating Instruction For Use And installation			15
5.2 Joystick Controls                                                                           	
5.3 Button Functions                                                                           	
5.4 Modes                                                                                          	
6.	CHAPTER 7                                                                                       	
   AQUANAUT Charging details

7.	APPENDIX – Mechanical drawings                                                	
              



<img width="940" height="688" alt="Image" src="https://github.com/user-attachments/assets/aa44f9ff-a355-466b-aa2c-0411caac0206" />


The Underwater Remotely Operated Vehicle (AQUANAUT 30 V3) has been designed and developed as a platform for underwater inspection. The system is tethered vide an electrical cable of 100m length allowing for easily deploy-ability over an area. The AQUANAUT 30 V3 consists of an aluminum chassis as the outer frame of the platform thereby making it rugged, reliable, and giving it long life.
The AQUANAUT 30 V3 is self-contained with its power source, control electronics, communication and navigation hardware placed in its central tube. The AQUANAUT 30 V3 has eight thrusters on-board designed in such a plane and geometry, thereby allowing easy maneuverability to the underwater craft, 6 degrees of freedom. The platform can therefore be easily deployed for underwater inspection.
The thrusters are placed within the frame, hence protecting them from mechanical damage during operations or mission. The rechargeable batteries provide good endurance up to 2hrs.
The AQUANAUT 30 V3 has four powerful lights provided in front and allows the on-board high resolution camera to effective view and record the underwater video as it traverses over the structures.    
The AQUANAUT 30 V3 is controlled from the surface using a 100m  tether cable wound on a light weight cable drum. The underwater craft is controlled from the surface using a Ground Control Station (GCS) which is based on a Laptop with the Human Machine Interface Software allowing the operator to easily control the craft as well as view the on-board system performance and view the streaming video during inspection. The rov also has recording option to record the live video. 
CHAPTER-2

2.1 Applications of AQUANAUT 30 V3 
The AQUANAUT 30 V3 is an advanced underwater rover specifically designed for a range of demanding applications such as dam wall inspections, ship hull monitoring, and underwater research. This highly capable system eliminates the need for human intervention in hazardous underwater environments, making it an essential tool for inspection and exploration tasks.
Dam Wall Inspections: Enables thorough examination of submerged structures to identify cracks, erosion, and other potential issues.
Ship Hull Monitoring: Provides close-up inspections of ship hulls for maintenance and safety checks without requiring divers.
Underwater Research: Facilitates the study of aquatic ecosystems, underwater habitats, and geological formations, supporting scientific discovery.
2.2 Leading Particulars and General Data
The Aqua Naut 30 V3 is a robust underwater rover designed for inspections at depths of up to 30 meters. This versatile vehicle is equipped with 8 thrusters that provide 6 degrees of freedom, allowing precise movement in all directions. It can operate continuously for up to 1.5 hours, delivering streaming real-time video to the Ground Control Station on the surface.
The rover is constructed using a durable combination of aluminum and acrylic tube weighing around 9 kg. This weight enhances stability in water, even in challenging conditions. AQUANAUT 30 V3 can achieve a speed of 1.5 knots in still waters, making it effective for a range of underwater tasks. 
For visibility, the rover is outfitted with four powerful 4 lights, each providing 1500 lumens of illumination. To monitor depth, a pressure sensor is integrated into the frame, providing accurate real-time data as the rover dives down. Communication is handled through a tether cable, which connects to a cable drum. From the cable drum, a cable leads to the GCS computer. The system is easily controlled using an Operator Console, offering intuitive operation.
The cable drum also features a toggle switch for powering the rover on and off, ensuring quick and easy deployment. With its practical design and advanced capabilities, the Aqua Naut 30 is an excellent solution for a wide range of underwater inspection applications.

 
CHAPTER-3

Underwater ROV Setup and Operation Guide
Hardware Components
•	Pixhawk flight controller
•	Raspberry Pi (with BlueOS installed)
•	ESCs and thrusters
•	Camera (e.g., USB camera)
•	Lights (LEDs or waterproof lamps)
•	Power source
•	Cable drum 
•	Computer with QGroundControl 
•	Pressure sensor 
•	battery

1. Software Setup
1.1 Install BlueOS on Raspberry Pi
1.	Flash BlueOS to a microSD card using raspberry pi imager. (BlueOS will be available on bluerobotics official site) 
Install bule0S to your laptop
Then install raspberry pi imager (for flashing OS) 
now you want to take an empty SD card insert to a SD card reader and connect to your laptop 
open raspberry pi imager under raspberry pi device chooses raspberry pi 4, under operating system select the blueOS (click choose OS -> use custom -> goes to device and select from the location where you installed)
then choose your storage (the SD card in which you want to flash) 
click next to flash the OS

<img width="448" height="252" alt="image" src="https://github.com/user-attachments/assets/b445d6b0-74fa-4a17-baa8-7e81f423e906" />

3.	Insert the SD card into the Raspberry Pi.
4.	Power up and connect to BlueOS via browser (http://192.168.2.2:8080 or appropriate IP).
1.2 Install and Configure ArduSub
•	Connect Pixhawk to pc using a USB cable and open Qground control, there will a Q icon on the left top corner click on that icon and click vehicle setup there you can see a firmware tab open to install the firmware 
<img width="550" height="309" alt="image" src="https://github.com/user-attachments/assets/3a6ea5e6-3847-4376-9e48-fc0a634bea01" />

2. QGroundControl (QGC) Setup
2.1 Connect to QGround Control
•	Open QGC on your PC. Go to vehicle setup now you want to calibrate sensors   
3. Compass & Accelerometer Calibration
1.	In QGC, go to Vehicle Setup > Sensors.
<img width="585" height="329" alt="image" src="https://github.com/user-attachments/assets/acd27c2d-4af0-42b2-b176-13a0143dba03" />
2.	Click acceletrometer.
3.	Follow the instructions (rotate the vehicle in all axes).
<img width="568" height="343" alt="image" src="https://github.com/user-attachments/assets/b7ef719d-a63a-4f2f-aa57-2fff72505e18" />
Save and reboot 
4.	After accelerometer calibration do compass calibration calibration 
       5.  Start the individual calibration steps by clicking one of the buttons to the left.
Rotate the vehicle randomly around all axes until the progress bar fills all the way to the right.

<img width="567" height="349" alt="image" src="https://github.com/user-attachments/assets/f232268c-cda9-40a0-a6b3-f34d5763a62e" />
              Save and reboot.
4. Joystick/Gamepad Calibration
1.	Connect your joystick/gamepad to your PC.
2.	In QGC, go to Vehicle Setup > Joystick.
3.	Select your joystick and click Calibrate.
The Operator Console may require calibration before you can enable it for use in AQUANAUT HMI. If your Operator Console requires calibration, the Joystick tab on the Vehicle Settings page will be yellow, and you should follow these steps to calibrate your console. If your console does not require calibration, the Joystick tab will not be yellow, and you can skip this step!
1. Go to the Vehicle Settings page in AQUANAUT HMI, then click on the red Joystick tab in the sidebar on the left. If you do not see a Joystick tab, this indicates that the Console is not detected by HMI or not connected to the computer.
2. When the Operator Console is connected, in the Joystick tab, on General settings, Tick the checkbox that says Enable Joystick.
4.	  Click Calibration settings, then click Start.
  <img width="940" height="608" alt="image" src="https://github.com/user-attachments/assets/fb5e4553-c474-4e78-a951-867eb07ca468" />

  5.	4. Follow the step-by-step instructions and move the sticks as indicated in AQUANAUT HMI.
6.	When completed, the Joystick tab will no longer be red, and the Enabled checkbox on the Joystick page will be enabled.

7.	Follow the prompts to calibrate axes and buttons.
8.	Assign joystick buttons for functions (e.g., arming, mode change, lights).


Button Setup 
The default button setup for the AQUANAUT 30 V3 is shown below:
<img width="367" height="231" alt="image" src="https://github.com/user-attachments/assets/5f6acd81-f6f0-4d7d-9c34-92c255c7ffcc" />
The button layout can be configured in the Joystick tab on the Vehicle Setup page under Button Assignment.
1. Go to the Vehicle Setup menu then select Joystick from the sidebar.
2. Under Button Assignment, AQUANAUT HMI shows a list of all the buttons and their assigned functions.
3. Press the button that you want to change on the controller. The corresponding button number in the list will light up next to the functions that are assigned to it. The functions are listed in two columns labelled Function and Shift Function.
•	The function listed in the first Function column is triggered when the button is pressed normally.
•	The function listed in the second Shift Function column is triggered when the button is pressed while the Shift button is held down.
•	The default shift button is the HOME button on the EvoFox controller.
4. Select the desired function and shift function for the button from the dropdowns to the right of the button number. Be aware that not all button functions that are displayed are supported. A list of the most common button functions is provided below.
Below is a list of the common button functions and the associated button function parameter as it is displayed in the AQUANAUT HMI dropdown.

5. Assigning Channels for Lights
1.	In QGC, go to Vehicle Setup > light tab
2.	Connect the light pwm pin signal to Pixhawk aux pins say 1 on the qgc light tab chose channel 9
3.	 Assign a joystick button to control lights under Joystick Button Actions.
                    

<img width="591" height="332" alt="image" src="https://github.com/user-attachments/assets/cb090de5-0464-4a62-a4ef-4851455cb277" />


6. Frame setup
•	In QGC > Vehicle Setup > frame 
Select 8 thruster configuration frame for Aquanaut 30 v3
   
<img width="658" height="370" alt="image" src="https://github.com/user-attachments/assets/6c3b4c51-2429-4c62-a08e-bccd1666363f" />

7. Power setup
1.	In QGC, go to Vehicle Setup > power
 1. Wiring Check
Ensure the Power Module (e.g., 3DR-style or Mauch, etc.) is properly connected to your Pixhawk:
<img width="273" height="324" alt="image" src="https://github.com/user-attachments/assets/a0216f02-ed60-4539-a560-506af3298c21" />
•	Power Module → Power port of the flight controller.
•	The module measures voltage and current and sends it via the analog signal (depending on module).

 2. Open QGroundControl → Power Setup
1.	Connect your pixhawk to QGroundControl (via USB)
2.	Go to the "Power" tab:
QGroundControl → Vehicle Setup → Power
           3. Battery Configuration
1.	Set Battery Number 1:
o	Battery chemistry: LiPo
o	Number of cells: 4
o	Full voltage per cell: 4.2 V
o	Empty voltage per cell: 3.5 V (or 3.3 V for aggressive cutoff)
2.	Total full voltage = 4.2 V × 4 = 16.8 V
Total empty voltage = 3.5 V × 4 = 14.0 V

 4. Power Sensor Configuration
1.	Under Power Setup
o	select Analog Voltage and Current
2.	If using a custom power module, you may need to manually enter:
o	Voltage divider
o	Amps per volt
Example values (for standard 3DR Power Module):
•	Voltage Divider: 10.1
•	Amps per Volt: 17.0

 5. Calibrate Voltage and Current (optional but recommended)
•	Use a multimeter to measure actual battery voltage and current draw.
•	Adjust the voltage divider and amps per volt until QGC shows accurate readings.
1. In QGC Vehicle Setup, click on the Power tab in the left sidebar.
<img width="940" height="590" alt="image" src="https://github.com/user-attachments/assets/e342a26f-1603-46e6-954b-6fdf86818ac0" />

2. Select “Analog Voltage and Current” from the Battery monitor dropdown.
3. Select the correct option from the Power sensor dropdown menu.
•	If using a Blue Robotics Power Sense Module, select “Navigator w/ Blue Robotics Power Sense Module” from the dropdown menu. No further configuration is necessary.
<img width="940" height="590" alt="image" src="https://github.com/user-attachments/assets/50d7e9b1-7232-4f93-846e-bca9f07a2da7" />














