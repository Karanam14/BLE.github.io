BLE.github.io
What is Bluetooth Low Energy?
Bluetooth Low Energy, BLE for short, is a power-conserving variant of Bluetooth. BLE’s primary application is short distance transmission of small amounts of data (low bandwidth). Unlike Bluetooth that is always on, BLE remains in sleep mode constantly except for when a connection is initiated.
This makes it consume very low power. BLE consumes approximately 100x less power than Bluetooth (depending on the use case).
![image](https://user-images.githubusercontent.com/97583689/218306679-6bed89cf-3e93-45df-b8ce-34496dcb93c1.png)
Additionally, BLE supports not only point-to-point communication, but also broadcast mode, and mesh network.
Take a look at the table below that compares BLE and Bluetooth Classic in more detail.
![image](https://user-images.githubusercontent.com/97583689/218306707-e6436099-da91-4bcb-b1a3-42935d566a12.png)
Due to its properties, BLE is suitable for applications that need to exchange small amounts of data periodically running on a coin cell. For example, BLE is of great use in healthcare, fitness, tracking, beacons, security, and home automation industries.
*BLE Server and Client*
With Bluetooth Low Energy, there are two types of devices: the server and the client. The ESP32 can act either as a client or as a server.
The server advertises its existence, so it can be found by other devices, and contains the data that the client can read. The client scans the nearby devices, and when it finds the server it is looking for, it establishes a connection and listens for incoming data. This is called point-to-point communication.
![image](https://user-images.githubusercontent.com/97583689/218306763-cb07244c-f1e2-44d9-9d68-6d194b2f6a58.png)
As mentioned previously, BLE also supports broadcast mode and mesh network:

Broadcast mode: the server transmits data to many clients that are connected;
Mesh network: all the devices are connected, this is a many to many connection.
Even though the broadcast and mesh network setups are possible to implement, they were developed very recently, so there aren’t many examples implemented for the ESP32 at this moment.
