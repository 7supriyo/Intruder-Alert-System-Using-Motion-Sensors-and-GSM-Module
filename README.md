# Intruder-Alert-System-Using-Motion-Sensors-and-GSM-Module
This report has explored designing and implementing a cost-effective intruder alert system utilizing motion sensors and a GSM module. This system offers a practical solution for residential or commercial security applications, effectively detecting unauthorized entry attempts and triggering real-time notification via SMS alerts.

The report has detailed the system's components, and functionalities while acknowledging its potential for further development.
The core system presented serves as a robust foundation for future advancements. The functionalities can be significantly expanded by integrating additional sensors, a mobile application, and cloud connectivity. These enhancements, such as remote system control, real-time notifications with sensor location details, and historical data analysis, can contribute to a more comprehensive and user-friendly security solution.

Furthermore, exploring alternative power management solutions and potential camera integration would further strengthen the system's reliability and effectiveness. In conclusion, this intruder alert system offers a valuable tool for deterring potential intrusions and promoting a sense of security for property owners. It presents a strong foundation for further development, paving the way for a more comprehensive and user-centric approach to residential and commercial security.
![image](https://github.com/user-attachments/assets/b33d6e8a-bb96-4fc6-9031-75266dc0b983)
# Intruder Alert System Using Motion Sensors and GSM Module

## Overview

The **Intruder Alert System** is a security solution designed to detect unauthorized movement in a restricted area and send instant alerts to the user via SMS. This system utilizes motion sensors to detect movement and a GSM module to send notifications to a predefined phone number. It is an ideal solution for home security, office security, or any area where real-time intrusion detection is required.

## Features

- **Motion Detection**: Utilizes PIR (Passive Infrared) motion sensors to detect movement within a specified range.
- **Instant Alerts**: Sends real-time SMS alerts to the user's mobile phone when motion is detected.
- **GSM Integration**: Uses a GSM module (e.g., SIM800L) to communicate with the mobile network and send SMS notifications.
- **Customizable**: The system can be configured to send alerts to multiple phone numbers or customized messages.
- **Low Power Consumption**: Designed to operate efficiently with minimal power usage.
- **Easy to Install**: Simple setup and installation process with detailed instructions provided.

## Components Used

1. **PIR Motion Sensor**: Detects movement within its range.
2. **GSM Module (SIM800L)**: Sends SMS alerts to the user's phone.
3. **Microcontroller (Arduino)**: Processes sensor data and controls the GSM module.
4. **Power Supply**: Provides power to the system (e.g., 5V adapter or battery).
5. **Breadboard and Jumper Wires**: For connecting components.
6. **SIM Card**: Inserted into the GSM module for sending SMS.

## How It Works

1. The PIR motion sensor continuously monitors the area for any movement.
2. When motion is detected, the sensor sends a signal to the microcontroller.
3. The microcontroller processes the signal and triggers the GSM module.
4. The GSM module sends an SMS alert to the predefined phone number(s) with a custom message (e.g., "Intruder Detected!").
5. The system resets and continues monitoring for further movement.

## Installation and Setup

### Hardware Setup

1. **Connect the PIR Sensor**:
   - Connect the VCC pin of the PIR sensor to the 5V pin on the Arduino.
   - Connect the GND pin of the PIR sensor to the GND pin on the Arduino.
   - Connect the OUT pin of the PIR sensor to a digital input pin on the Arduino (e.g., D2).

2. **Connect the GSM Module**:
   - Connect the VCC pin of the GSM module to the 5V pin on the Arduino.
   - Connect the GND pin of the GSM module to the GND pin on the Arduino.
   - Connect the TX pin of the GSM module to the RX pin on the Arduino.
   - Connect the RX pin of the GSM module to the TX pin on the Arduino.

3. **Power the System**:
   - Connect the Arduino to a power source (e.g., USB or external power supply).

### Software Setup

1. **Install Arduino IDE**: Download and install the Arduino IDE from [arduino.cc](https://www.arduino.cc/).
2. **Install Required Libraries**: Install the necessary libraries for the GSM module (e.g., `SoftwareSerial`).
3. **Upload the Code**: Open the provided Arduino sketch (`Intruder_Alert_System.ino`) in the Arduino IDE, and upload it to the microcontroller.
4. **Insert SIM Card**: Insert a valid SIM card into the GSM module.
5. **Configure Phone Number**: Update the phone number(s) in the code where the alerts will be sent.

## Code Explanation

The Arduino code is responsible for reading the PIR sensor's output and sending SMS alerts via the GSM module. Here's a brief overview of the code:

- **PIR Sensor Reading**: The code continuously checks the output of the PIR sensor. If motion is detected, it sets a flag and proceeds to send an SMS.
- **GSM Communication**: The code initializes the GSM module and sends an AT command to send an SMS to the specified phone number.
- **Loop Function**: The loop function monitors the sensor and triggers the alert when motion is detected.

## Customization

- **Change Alert Message**: Modify the SMS message in the code to suit your needs.
- **Add Multiple Phone Numbers**: Update the code to send alerts to multiple phone numbers.
- **Adjust Sensitivity**: Adjust the sensitivity and delay settings of the PIR sensor as needed.

## Applications

- **Home Security**: Protect your home from intruders by receiving instant alerts.
- **Office Security**: Monitor restricted areas in your office or workplace.
- **Warehouse Security**: Keep an eye on your warehouse or storage facility.
- **Remote Monitoring**: Use the system to monitor remote locations where internet connectivity is not available.

## Troubleshooting

- **GSM Module Not Responding**: Ensure the SIM card is properly inserted and has sufficient balance. Check the antenna connection.
- **PIR Sensor Not Detecting Motion**: Adjust the sensitivity and positioning of the PIR sensor.
- **No SMS Received**: Verify the phone number in the code and ensure the GSM module has a strong network signal.

## Future Enhancements

- **Integration with IoT Platforms**: Connect the system to IoT platforms for remote monitoring and control.
- **Camera Integration**: Add a camera module to capture images or videos when motion is detected.
- **Battery Backup**: Implement a battery backup system for uninterrupted operation during power outages.

## License

This project is open-source and available under the MIT License. Feel free to modify and distribute it as per the license terms.

## Contributing

Contributions are welcome! If you have any suggestions, bug reports, or feature requests, please open an issue or submit a pull request.

## Acknowledgments

- Thanks to the Arduino community for providing extensive resources and support.
- Special thanks to the developers of the libraries used in this project.


