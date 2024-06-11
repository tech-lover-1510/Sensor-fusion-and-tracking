# Sensor-fusion-and-tracking

![AirportApronTrackingExample_01](https://github.com/tech-lover-1510/Sensor-fusion-and-tracking/assets/136898779/b488dbf0-f957-4e88-9b6b-058e7a0bab57)

Sensor fusion integrates data from multiple sensors to provide a more accurate and comprehensive understanding of an environment. Tracking monitors the state of an object over time, estimating its position and velocity. Combining these, sensor fusion enhances tracking accuracy and reliability by leveraging the strengths of different sensors. Common applications include autonomous vehicles, where data from GPS, cameras, LiDAR, and other sensors are fused to ensure precise navigation and situational awareness. This approach mitigates the limitations of individual sensors, resulting in robust, reliable tracking systems.

## Advantages of sensor fusion
#### Increases data quailty
When we combine 'n' identical sensors, it reduces the noise by a factor of $\sqrt{n}$. However, this is not the only way to do sensor fusion. We can combine different sensor data to get the data with less noise.

![image](https://github.com/tech-lover-1510/Sensor-fusion-and-tracking/assets/136898779/15652c4f-c0e6-4756-a1c7-d46245ea0c75)

A simple example of sensor fusion improving data quality is in a smartphone's navigation system. The GPS provides location data but can be inaccurate or unreliable in dense urban areas or indoors. By fusing GPS data with information from the accelerometer and gyroscope (which track the phone's movements and orientation), the navigation system can more accurately determine the phone's position and movement. This combined data helps maintain accurate tracking even when GPS signals are weak or unavailable, resulting in improved navigation accuracy and reliability.

#### Increasing reliability
When fusing two identical sensors, like averaged accelerometers, we gain reliability by having a backup in case one fails. If one sensor fails, quality might drop, but we still maintain the measurement. Adding a third sensor allows the fusion algorithm to discard any single sensor's data that deviates significantly from the others. An example is using three pitot tubes to measure an aircraft's airspeed: if one fails or gives an incorrect reading, the other two can still provide an accurate measure. This redundancy increases reliability, but we must be cautious of common failure modes that could affect all sensors simultaneously. For instance, an aircraft flying through freezing rain might find all three pitot tubes freezing up, rendering them useless despite sensor fusion.

In such cases, fusing sensors measuring different quantities can mitigate the problem. For example, supplementing pitot tube airspeed measurements with estimates from GPS and atmospheric wind models ensures that airspeed can still be determined even if the primary sensors fail. Although the quality might be reduced, maintaining airspeed measurement is crucial for the aircraft's safety. Thus, while losing a sensor impacts quality, having a diverse and redundant sensor fusion system ensures continued operation and reliability.

#### Estimates unmeasured states
The third benefit of sensor fusion is its ability to estimate unmeasured states. It's important to understand that "unmeasured" doesn't mean "unmeasurable"; it simply indicates that the system lacks a sensor to directly measure the desired state. For instance, a visible camera can't directly measure the distance to an object in its view. A large object far away might appear the same size in pixels as a small object up close. However, by adding a second optical sensor and applying sensor fusion, we can extract three-dimensional information. The fusion algorithm compares scenes from two different angles to measure relative distances between objects in the images. Thus, while the individual sensors can't measure distance on their own, they can when combined.

![image](https://github.com/tech-lover-1510/Sensor-fusion-and-tracking/assets/136898779/8bdbbe36-487a-4896-844d-7bd9e9aedd2d)

#### Increases coverage
Sensor fusion can also increase coverage area. Consider the short-range ultrasonic sensors on a car used for parking assist. These sensors measure distances to nearby objects, like parked cars and curbs, alerting the driver when they are close to impact. Each sensor typically has a limited range and a narrow field of view. To achieve full coverage around the car, additional sensors are added, and their measurements are fused to create a larger, comprehensive field of view. While these measurements might not be averaged or combined mathematically—since it's important to know the specific location of each detected object relative to the car—the system that integrates these sensors into a coherent whole is still utilizing sensor fusion.

![image](https://github.com/tech-lover-1510/Sensor-fusion-and-tracking/assets/136898779/166b1c5d-67bf-4661-a453-da6128ff18ff)
