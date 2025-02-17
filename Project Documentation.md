# Fitness Tracker Application - Project Documentation
## 1. Project Overview

I developed the Fitness Tracker Application to help users monitor their daily fitness activities, particularly step counting. The app integrates various components, such as a pedometer, GPS tracking, and Bluetooth connectivity, to enhance the user experience. While the step counter is fully functional, I am still debugging the GPS and Bluetooth features to improve overall performance.

----

## 2. Features & Functionalities

### Implemented Features:

- Step Counter: Utilizes the device’s motion sensors to track the number of steps taken by the user.

- User Interface: Simple and intuitive design with icons representing various fitness activities.

- Fitness Charts: Displays fitness data using graphical charts to help users visualize their progress.

- Image Assets: Various icons and images enhance the UI, making navigation intuitive.

### Features Under Development:

- GPS Tracking: Planned to track user movement and log fitness activities based on location.

- Bluetooth Connectivity: Will allow connection with external fitness devices for better tracking.

- Data Logging: Future updates will include historical step count data storage and retrieval.

----

## 3. Technology Stack

- Platform: MIT App Inventor

- Programming Logic: Block-based programming (App Inventor Blocks)

- Sensors Used:

   - Accelerometer (for step tracking)

   - GPS (for location tracking - currently under debugging)

   - Bluetooth module (for external device connectivity - currently under debugging)

- UI Components:

  - Buttons for navigation

  - Image assets for a visually appealing interface

  - Graphical charts for data visualization

----

## 4. Code Explanation

### Step Counter Code Block

````
when Clock1.Timer do
    if Pedometer1.Enabled then
        set LabelStepCount.Text to Pedometer1.StepCount
    end if
````
Explanation:

- The Clock1.Timer event triggers periodically to check if the step counter is enabled.

- If enabled, it updates the label displaying the step count using Pedometer1.StepCount.

### GPS Tracking (Under Debugging)

````
when LocationSensor1.LocationChanged do
    set LabelLatitude.Text to LocationSensor1.Latitude
    set LabelLongitude.Text to LocationSensor1.Longitude
````
Explanation:

- This block updates the latitude and longitude labels when the GPS detects a location change.

- It relies on LocationSensor1.LocationChanged to fetch real-time coordinates.

### Bluetooth Connectivity (Under Debugging)

````
when BluetoothClient1.ConnectionStatusChanged do
    if BluetoothClient1.IsConnected then
        set LabelStatus.Text to "Connected"
    else
        set LabelStatus.Text to "Disconnected"
````
Explanation:

- This checks the status of the Bluetooth connection and updates the label accordingly.

- The BluetoothClient1.IsConnected property determines the connection state.

----
## 5. Current Limitations & Debugging Plan

- GPS Not Functioning Properly: The GPS feature is present but not yet operational. My debugging efforts are focused on ensuring location permissions are correctly requested and processed.

- Bluetooth Issues: Bluetooth component is included but not connecting as expected. I plan to check the device’s compatibility and implement proper pairing protocols.

- No Data Persistence: Currently, there is no way to store past fitness data. In future updates, I will integrate a database or file storage mechanism.

----
## 6. Future Enhancements
- Full GPS Integration: Enable route tracking and location-based fitness recommendations.

- Bluetooth Pairing with Fitness Devices: Support for external sensors like heart rate monitors.

- Data Storage & Syncing: Implement cloud-based or local storage to track fitness progress over time.

- User Profiles: Allow multiple users to track their fitness journeys individually.

----
## 7. Development Process

The development of the Fitness Tracker Application followed an iterative approach:

- Initial Concept & Design: I created wireframes and planned core functionalities.

- Implementation: Using MIT App Inventor, I developed the step counter and UI.

- Testing & Debugging: I focused on ensuring the step counter worked correctly before expanding features.

- Future Development: Debugging GPS and Bluetooth features and integrating data storage are my next priorities.

----
## 8. Code Review Summary

- Step Counter: Verified for accuracy and efficiency in detecting steps.

- GPS & Bluetooth: Identified as requiring debugging for stability.

- UI & User Experience: Improved navigation and design for better usability.

- Performance Considerations: Checked for potential battery usage optimization.

----
## 9. Resources Used

- https://appinventor.mit.edu/explore/ai2
- https://developer.android.com/guide/topics/sensors
- https://developer.android.com/guide/topics/connectivity/bluetooth
- https://developer.android.com/training/location

----
## 10. Conclusion

I have developed the Fitness Tracker Application as a work in progress, with a functional step counter and a structured plan for additional features. The upcoming debugging phases will focus on GPS and Bluetooth integration to enhance tracking capabilities. I am excited to continue refining this app into a comprehensive fitness tracking solution.
