VHDL Car-parking-system

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# College Parking System with VHDL

This repository contains a VHDL-based implementation of a college parking system that integrates vehicle management, a ticketing system, fire detection, and a vending machine for drinks. The system supports 50 parking spaces and offers both student/staff ID validation and guest ticketing, ensuring smooth management of the parking facility.

## Features

### 1. **Parking Management:**
- **ID System** for staff and students.
- **Ticket System** for guests with automatic entry time recording.
- **Ultra-Sonic Sensors** for each parking space to detect car presence.
- **Occupancy Monitoring**: Displays available parking spots via 7-segment displays.
- **Gate Control**: Automatically opens the entrance gate for vehicles with valid IDs or after a ticket is assigned.

### 2. **Vending Machine:**
- Offers **Coffee**, **Water**, and **Hot Chocolate**.
- Users select a drink, make a payment, and the machine dispenses the drink.
- Displays the price of selected drinks and provides change if necessary.

### 3. **Fire Detection:**
- Integrated **Fire Sensor** to detect emergencies by monitoring temperature.
- Triggers alarms if the temperature exceeds a defined threshold.

### 4. **Parking Sensors:**
- **Ultra-Sonic Range Sensors** monitor the status of parking spots.
- Occupied spots turn off corresponding **LED indicators**.
- Available parking spots are updated on the **7-segment displays**.

## Inputs and Outputs

### Input Ports:
- `id_valid`: Signal to indicate whether a vehicle has a valid ID.
- `ticket_in`: Input for ticket assignment for guest vehicles.
- `enter_time_in`/`exit_time_in`: Inputs to record the time a vehicle enters/exits the garage.
- `sensor_array`: Array of Ultra-Sonic sensors to detect car presence in each parking space.
- `temperature`: Input from the fire sensor to monitor temperature levels.
- **Vending Machine Buttons**:
  - `coffee_button`
  - `water_button`
  - `hot_chocolate_button`: Inputs for drink selection.
- `money_in`: Input to track the money received for drinks.

### Output Ports:
- `free_count`: Displays the number of available parking spaces.
- `payment_due`: Displays the calculated payment for guest vehicles.
- `gate_open`: Signal to control the entrance gate.
- `fire_alarm`: Signal to trigger fire alarms in case of high temperature.
- **7-Segment Display Outputs**:
  - `seg`: Displays the available parking spots.
- **LED Indicators**:
  - `led`: LEDs representing parking spot status (on for free, off for occupied).
- **Vending Machine Status**:
  - `coffee_ready`, `water_ready`, `hot_chocolate_ready`: Signals to indicate when a selected drink is ready.

## System Overview

1. **Parking System**: 
   - Vehicles with a valid ID are granted access automatically, while guests receive a ticket with their entry time recorded.
   - Ultra-Sonic sensors detect whether parking spaces are occupied, updating the system in real-time.
   - The system displays the number of free spots and controls the gate accordingly.

2. **Vending Machine**: 
   - Users can purchase drinks from the vending machine by selecting their desired option and paying the displayed price. Once payment is received, the system dispenses the selected drink and calculates any change.

3. **Fire Detection**: 
   - The system includes a fire sensor that monitors the garage’s temperature. If the temperature rises above a certain level, the system triggers an emergency alarm.

## Project Structure

- **`parking_system.vhd`**: Contains the VHDL code for the entire parking system.
- **Testbench Files**: (Optional) Add testbench files to simulate and verify the behavior of the system.

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/ZeyadArafa/college-parking-system-vhdl.git
   ```

2. Set up your VHDL simulation environment (e.g., ModelSim, Xilinx Vivado).

3. Load the provided VHDL files into your simulator and run the testbench to verify the system's functionality.

4. If deploying to hardware, adjust the system clock frequency and input/output configurations as per your requirements.

## Contributions

Contributions are welcome! Feel free to fork the repository, open issues, or submit pull requests for bug fixes, improvements, or new features.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Cars passing through the entrance are allowed immediate access; otherwise, a ticket is assigned with the entry time recorded. Within the parking garage with 50 spaces, Ultra-Sonic range sensors determine if a car is parked by measuring the distance. When parked, the corresponding LED turns off, and the 7-Segment display decreases the count of available spots. The Fire Sensor alerts if temperatures reach dangerous levels. Additionally, a vending machine offers various options like Coffee, Water, and Hot Chocolate. Press the desired button, pay the displayed price, and collect your drink.



![image](https://github.com/ZeyadArafa/Car-Parking-System-/assets/121558294/6fa53b7a-8b33-4b9f-ad74-c009fd724d68)


![image](https://github.com/ZeyadArafa/Car-Parking-System-/assets/121558294/b8f344a1-7e73-48cf-b95f-160fc83726dd)


![image](https://github.com/ZeyadArafa/Car-Parking-System-/assets/121558294/9f291560-0d53-404b-9537-ca21561c61c9)


![image](https://github.com/ZeyadArafa/Car-Parking-System-/assets/121558294/58957fcb-4b69-449c-a65f-4b4bd45c195e)

