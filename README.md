# Smart Home System with Design Patterns

This repository demonstrates a **Smart Home System** implemented using several **design patterns**: **Observer Pattern**, **Factory Method Pattern**, and **Proxy Pattern**. The system simulates devices such as lights, thermostats, and door locks, with features such as turning devices on/off, status updates, access control, and automated triggers based on conditions (e.g., temperature exceeding a threshold).

### **Features**
- **Observer Pattern**: Devices notify the central hub about status changes.
- **Factory Method Pattern**: Dynamically create different types of devices (lights, thermostats, door locks).
- **Proxy Pattern**: Control access to devices based on user authentication.
- **Automated Triggers**: Devices automatically take actions based on conditions (e.g., turning off a light if the temperature exceeds 75 degrees).
- **Scheduling**: Schedule tasks (e.g., turning devices on at specific times).

---

### **How It Works**
- **Devices**: The system supports devices like:
  - **Light**: Can be turned on/off.
  - **Thermostat**: Can be turned on/off and set a temperature.
  - **Door Lock**: Can be locked/unlocked.
- **Central Hub**: A **central hub** observes the devices and prints their status whenever a change occurs.
- **Authentication**: The **Proxy Pattern** ensures that only authorized users can control the devices.

---

### **Design Patterns Used**
1. **Two Behavioral Design Patterns**:
   - **Observer Pattern**: Devices (Light, Thermostat, Door Lock) notify the central hub whenever their status changes.
   - **Strategy Pattern**: Used for changing algorithms dynamically at runtime. For example, changing the thermostat's temperature setting dynamically or choosing different device control strategies.

2. **Two Creational Design Patterns**:
   - **Factory Method Pattern**: A factory is used to dynamically create instances of different devices (e.g., `SmartDeviceFactory` creates `Light`, `Thermostat`, and `DoorLock`).
   - **Singleton Pattern**: Ensures that the **CentralHub** only has one instance, providing a single point of control for the entire system.

3. **Two Structural Design Patterns**:
   - **Proxy Pattern**: **DeviceProxy** is used to control access to the devices, ensuring that actions like turning a device on/off are only performed if the user is authenticated.
   - **Adapter Pattern**: Adapts the interface of devices, enabling them to communicate with the central hub without changing the core device functionality.


