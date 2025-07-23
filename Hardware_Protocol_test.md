Industrial protocols: 
•	Modbus: Communication protocols between electronic devices, such as sensors, meters, and logic controllers.

TESTS: 
- Send specific request to device like: read Read Holding Registers data, write single coil. Check o/p.
- Also write known values to the device register and then read them back, to check corrupted data.
- Intentionally send invalid requests like: ask for an unavailable register. Check error code.
- Check response time under heavy load of continuous communication.

• BACnet: (Building Automation and Control Networks): Used for communication within building automation. It is an object-oriented. 
Uses: Used in smart buildings , It connects HVAC, lighting, access control, and fire detection systems. 
TESTS: 
-	Check if device ReadProperty' or 'WriteProperty' conforms to the official standard. Tool used : BACnet Testing Laboratories.
-	To ensure that a new device can work together by already available devices. 
-	Can query device to discover it’s objects and then read/write to their properties. Ex: change temperature, create conditions like a simulated high temperature to ensure the device generates and broadcasts alarms.

•	SNMP (Simple Network Management Protocol): managing and monitoring network devices.
There is a central "manager" that communicates with "agents". It used a DB to define the properties of the managed device.
Used in: routers, switches, and servers to printers and UPS.
	TESTS: 
-	You will ensure the device's MIB file is correctly written.
-	send GET requests to query data from a device (e.g., get CPU usage) and verify the value is correct. Can also test SET requests to change configurations where applicable.
-	unplugging a network cable from a switch port, to verify that the device correctly sends an alert message to the manager.

•	MQTT: (Message Queuing Telemetry Transport): 
very lightweight messaging protocol designed for unreliable or low-bandwidth networks. It uses a publish/subscribe model between Client-Broker. Devices ("clients") don't talk to each other directly; they publish messages to a central server ("broker"). Clients subscribe to those topics to receive messages.
Uses:  IOT, smart home sensors, connected cars, 
TESTS: 
-	Must use low bandwidth and battery power ,these are precious.
-	Reliable connect/Disconnect.
-	Quality of Service (QoS): MQTT has three QoS levels (0 - at most once, 
-	1 - at least once, 2 - exactly once). A major part of your job is to verify that messages are delivered according to the specified QoS level, especially in unreliable network conditions.
-	Check payload transferred, should be not corrupted in transfer. 

Tools to test: MQTTLens (chrome Extension), web apps(https://www.softblade.de/)
