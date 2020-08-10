Low Cost Surveillance System Without Storage

We have designed a home surveillance system using a raspberry pi and an Arduino linked to a sensor and a thermal camera using a facial recognition algorithm that references the face detected by the raspberry pi camera to the faces of the members of the house. If there is no match, the home owners are sent a picture of the intruder via SMS and email. The intruder’s body temperature is also checked as it is vital in this COVID-era.<br>  

When someone approaches the door, the sensor is tripped and a signal is sent to the raspberry pi from the arduino upon which the pi camera takes a picture of the intruder. At the same time the thermal camera takes readings on the body temperature of the intruder. The thermal camera can also be used as a trigger to decide if an intruder is present.<br>  
 
The photo from the pi camera is then sent to the face recognition algorithm (face_recognition module) modified to increase efficiency. We calculate using MAE (Mean Absolute Error) instead of Euclidean distance which yields the same accuracy but is 50% faster than the latter.

The algorithm cross references the intruder’s encoding with the encodings of the house members and enters it into the data logs. If there is no match, the intruder’s picture is sent immediately to the house owner via SMS and email.<br>
The picture of the intruder IS NOT saved, only the encoding is, this assures that no storage is used.<br>

The front end consists of the SMS, email and a website that can be accessed by the house owners by logging in using credentials. The website consists of the most recent visitor, and the data logs of all the visitors.<br>

