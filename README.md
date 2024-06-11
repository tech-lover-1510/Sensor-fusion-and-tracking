# Sensor-fusion-and-tracking

![AirportApronTrackingExample_01](https://github.com/tech-lover-1510/Sensor-fusion-and-tracking/assets/136898779/b488dbf0-f957-4e88-9b6b-058e7a0bab57)

Sensor fusion integrates data from multiple sensors to provide a more accurate and comprehensive understanding of an environment. Tracking monitors the state of an object over time, estimating its position and velocity. Combining these, sensor fusion enhances tracking accuracy and reliability by leveraging the strengths of different sensors. Common applications include autonomous vehicles, where data from GPS, cameras, LiDAR, and other sensors are fused to ensure precise navigation and situational awareness. This approach mitigates the limitations of individual sensors, resulting in robust, reliable tracking systems.

## Advantages of sensor fusion
#### Increases data quailty
When we combine 'n' identical sensors, it reduces the noise by a factor of $\sqrt{n}$. However, this is not the only way to do sensor fusion. We can combine different sensor data to get the data with less noise.

![image](https://github.com/tech-lover-1510/Sensor-fusion-and-tracking/assets/136898779/15652c4f-c0e6-4756-a1c7-d46245ea0c75)

A simple example of sensor fusion improving data quality is in a smartphone's navigation system. The GPS provides location data but can be inaccurate or unreliable in dense urban areas or indoors. By fusing GPS data with information from the accelerometer and gyroscope (which track the phone's movements and orientation), the navigation system can more accurately determine the phone's position and movement. This combined data helps maintain accurate tracking even when GPS signals are weak or unavailable, resulting in improved navigation accuracy and reliability.
