
# Exploring IoT Technologies in ambient intelligence
**Pau Climent-Pérez**
April, 2024

>_"The most profound technologies are those that disappear. They weave themselves into the fabric of everyday life until they are indistinguishable from it."_ -- Late Mark Weiser, who was the chief scientist at Xerox PARC

## A brief recap on Ambient Intelligence

As we said when defining Ambient Intelligence, it is:

> **Definition**
> 
> “Ambient intelligence is the concept of **capturing and processing** data through **sensors, processors, and actuators** **unobtrusively embedded** throughout the environment. **Leveraging artificial intelligence (AI)**, ambient systems provide **connected, seamless, uninterrupted** everyday experiences that require no human intervention.”
> 
> Optional read: [https://www.arm.com/glossary/ambient-intelligence](https://www.arm.com/glossary/ambient-intelligence)

If we take the definition and break it down, we see that the following concepts emerge:

1. We need **sensors, processors, and actuators** that are **unobtrusively embedded** in the environment
2. The data of the sensors will be **captured and processed**
4. It requires an automated **machine-based intelligence (AI)** to make decisions on the captured data (automated knowledge extraction)
5. It is **connected**, and works **seamlessly** and **continuously** requiring no human intervention

Therefore, one of the main characteristics of ambient intelligence (AmI for short) is the need for embedded sensors that are unobtrusive and can integrate naturally in the environment. The following figure[^1] shows the main characteristics of AmI (left), and how these can be achieved using certain technologies (right). The ***Internet of Things*** (IoT, for short) appears as a clear component.

[^1]: Image from: [source](https://medriva.com/health/revolutionizing-patient-care-how-ambient-ai-scribes-are-transforming-doctor-visits)

![](https://img-cdn.thepublive.com/fit-in/1280x960/filters:format(webp)/medriva/media/media_files/6d5bed77ef421fd0463de1638072d63d6a88d45193ce7e8900ee89ceee757c5f.jpg)

### AmI for Active and Healthy Ageing (AmI 4 AHA)

Ambient intelligence has many applications, such as in transportation, workplace improvement, smart homes, etc. It can be used to increase comfort, as well as to improve energy efficiency, or raise alarms when a hazard or a danger arises.

However, given the ageing population in most countries, **Active and Assisted Living** (previously **Ambient Assisted Living**) arises as a concept that integrates IT technologies for improved care of older adults. With older populations needing higher levels of care provision, it is necessary to **implement technologies** that aid in **independent living** for longer. Also, this brings the opportunity to use **human resources** more efficiently (fewer carers available per older adult).

When desigining AmI4AHA (AAL) systems, it is therefore of paramount importance to take a systematic approach[^2] :

![](https://www.mdpi.com/sensors/sensors-21-03549/article_deploy/html/images/sensors-21-03549-g006-550.jpg)

It is important to base the **sensor selection** (step 1) on the functional requirements of the system, and then use **acquire the data** that is necessary (step 2), processing it using ML/AI-based **recognition** algorithms (step 3) for data analysis and knowledge extraction, which can then be fed in long-term (temporal analysis) algorithms (step 4).

> **Important**
>
>**Mandatory reading:** Cicirelli _et al._ 2021 "Ambient Assisted Living: A Review of Technologies, Methodologies and Future Perspectives for Healthy Aging of Population" [http://dx.doi.org/10.3390/s21103549](http://dx.doi.org/10.3390/s21103549)

In the case of a home for older adults, many needs can emerge, regarding reminder tools, aids for activities of daily living (ADLs), as well as other medical and disease prevention interventions. One example is shown next[^2] :

![](https://www.mdpi.com/sensors/sensors-21-03549/article_deploy/html/images/sensors-21-03549-g005-550.jpg)

The example integrates everyday tools such as smart vacuum robots, but also wearable location sensors, health-related wearable devices (heart rate, blood pressure, temperature), microphones for interaction with voice assistant and communications, blinds equipped with actuators for opening and closing them remotely, environmental sensors to sense ambient humidity and temperature (or air quality, CO$_2$), presence sensors for the detection of inhabitants, surveillance cameras (for security[^3], but also for safety[^4])

[^2]: Images from [http://dx.doi.org/10.3390/s21103549](http://dx.doi.org/10.3390/s21103549)
[^3]: security, in English refers to the security against burglars and/or damage, etc. (i.e. security of property)
[^4]: safety in English refers to the well-being of humans (i.e. against injuries or death)

## Introduction to the _Internet of Things_ (IoT)

### But, what is IoT?

Apart from a main component of AmI, IoT can be described as the network of everyday "things" (appliances, small devices, electronics; but also parcels, unfinished products in a factory, product parts), that are embedded with sensors (i.e. made _smart_) and given the possibility to communicate with other devices, and the Internet. Put another way:

> **Definition**
>
>"[...] (IoT) describes the **network of physical objects**—“things”—that are **embedded with sensors**, software, and other technologies for the purpose of connecting and **exchanging data with other devices** and systems over the internet."


> **Important**
>
> **Mandatory reading**: [https://www.oracle.com/internet-of-things/what-is-iot/](https://www.oracle.com/internet-of-things/what-is-iot/)
>_focus on Industrial IoT, or ***IIoT***_

Similarly, there is also the idea that the devices of IoT are based on **"cheap" integrated circuits (ICs)**, with the capability of Internet connection (i.e. a minimal TCP/IP stack, Bluetooth or other protocols):

> **Definition**
>
>"The term **IoT** \[...] refers to the **collective network of connected devices** and the technology that facilitates **communication between devices and the cloud**, as well as **between the devices themselves**. Thanks to the advent of **inexpensive computer chips** and high bandwidth telecommunication, we now have billions of devices connected to the internet. This means **everyday devices** like toothbrushes, vacuums, cars, and machines can use sensors to collect data and respond intelligently to users."



> **Important**
>
>Read the full article (**mandatory**): [https://aws.amazon.com/what-is/iot/](https://aws.amazon.com/what-is/iot/)
>_focus on industrial and other applications_

In summary, instead of focusing on the deployment of sensors in the environment, and the processing of captured data and subsequent analysis (ambient intelligence), a particular focus is given to **the devices themselves, and how these interact with each other**.

### Components of an IoT ecosystem

#### 1. Edge computing

Edge computing refers to the paradigm of processing data **closer to its source**, typically at or **near the edge of the network**, rather than relying solely on centralized cloud servers. By **bringing computation** and data storage **closer to where it's needed**, edge computing **reduces latency**, **minimizes bandwidth usage**, and enhances efficiency in data processing. 

This distributed computing approach enables faster response times and real-time analysis, making it **ideal for applications that require immediate processing** and decision-making, **such as IoT devices**, autonomous vehicles, and **smart sensors**. Edge computing also offers greater **privacy** and **security** by **processing sensitive data locally**, without necessarily transmitting it to the cloud. That is, edge computing revolutionizes the way data is managed and processed in the era of interconnected devices and decentralized computing architectures.

#### 2. Cloud computing

This concept is perhaps the most well-known of the three, and refers to the **delivery of computing services**—including **storage**, **databases**, servers, networking, **software**, and **analytics**—**over the internet (i.e. "the cloud")** to offer faster innovation, flexible resources, and economies of scale. In the context of IoT, cloud computing plays a pivotal role in **handling the massive amounts of data generated by interconnected devices**. IoT devices collect and transmit data to cloud servers for storage, processing, and analysis.

Cloud platforms provide the necessary **infrastructure and services to manage and analyse IoT data** efficiently, enabling businesses and organizations to **derive valuable knowledge**, optimize operations, and deliver enhanced services. Moreover, **cloud computing facilitates scalability** and accessibility, allowing IoT applications to expand and reach a broader audience without significant infrastructure investments. The integration of cloud computing and IoT fosters innovation and drives the development of intelligent solutions across various industries, from smart homes and cities to healthcare and manufacturing.

#### 3. Machine learning (ML/AI)

**Machine learning** is a subset of **artificial intelligence (AI)** that focuses on the development of algorithms and **statistical models** to enable computer systems to learn from and make **predictions** or **decisions based on data**, without being explicitly programmed for each task. In the context of IoT, machine learning is the component **capable of extracting meaningful knowledge** from the **vast amounts of data** generated by interconnected devices. By **analysing patterns**, trends, and anomalies in IoT data, machine learning algorithms can identify correlations, predict future outcomes, and automate decision-making processes.

Machine learning **empowers IoT systems** to **detect and respond to events** in real-time, creating proactive systems, intelligent automations, and predictive analytics across various domains, from smart agriculture and industrial IoT to healthcare and smart cities. The integration of machine learning with IoT unleashes the full potential of connected devices, driving innovation, and transforming industries with intelligent, data-driven solutions.

#### What is 'fog' computing?

Edge vs. cloud vs. fog, explained:

<iframe width="560" height="315" src="https://www.youtube.com/embed/8KfBFVoA3JA?si=X0n6azPMbZ6VeZgJ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### IoT Protocols and Standards

There are several common IoT protocols and standards used for communication between devices, networks, and platforms in IoT ecosystems.

![](https://cdn.ttgtmedia.com/rms/onlineimages/iotagenda-top_12_iot_protocols_and_standards-f.png)

The figure above shows the 12 top ones, which we can classify into two main groups, depending on whether they are used for network connectivity (i.e. the network infrastructure itself), or they are used as part of a message passing or web API protocol that is more reduced in size, computational and bandwidth requirements than typical full-sized devices:

#### Network infrastructure

1. **Wi-Fi**
2. Bluetooth and **Bluetooth Low Energy** (BLE)
3. Cellular (GSM, 2G/3G, 4G/LTE, 5G)
4. Long range and **LoRaWAN**
5. **Zigbee**
6. Z-Wave
#### Message passing, web APIs, queuing and middleware
1. **MQTT** ("Mosquito"): Message Queuing Telemetry Transport
2. AMQP: Advanced Message Queuing Protocol
3. DDS: Data distribution service
4. CoAP: Constrained Application Protocol
5. EMPP: Extensible Messaging and Presence Protocol
6. LM2M: Lightweight Machine-to-Machine

> **Important**
>
>Read the article (**mandatory**) at: [https://www.techtarget.com/iotagenda/tip/Top-12-most-commonly-used-IoT-protocols-and-standards](https://www.techtarget.com/iotagenda/tip/Top-12-most-commonly-used-IoT-protocols-and-standards)

These protocols and standards provide the foundation for interoperability, scalability, and reliability in IoT deployments, enabling seamless communication and integration across diverse devices, networks, and platforms in IoT ecosystems. Choosing the right protocol depends on factors such as device capabilities, network constraints, scalability requirements, and application-specific needs. An example of this is the use of Zigbee devices in smart homes, which frees up space in the Wi-Fi channel for communication of larger devices (less IPs assigned). Furthermore, Zigbee devices can be battery powered, with batteries lasting in the range of years, rather than weeks or months.

#### IoT hubs and gateways: making different protocols work together

**IoT gateways and hubs** allow IoT devices connected in a local network to interact with cloud services, they perform **protocol translation** (e.g. Zigbee message to HTTP web service request) as part of their protocol interoperability functions, data can be **aggregated** before it is sent, which reduces bandwidth usage. When they do so, as said above they perform **edge** or **fog computing**. As part of their implementation, they need to provide **enhanced security** to the local network, avoiding unauthorized access to the local IoT devices.

> **Example**
>
>Commercially available products, such **Amazon echo** integrate gateway capabilities. This type of device can find local Zigbee and Wi-Fi home sensors and integrate them. When a voice command is issued by the user, the voice assistant connects to Amazon AWS, and performs the command recognition, which then sends back requests for actuator changes, etc.
>
>Open source projects, such as **Home Assistant** [https://www.home-assistant.io/](https://www.home-assistant.io/) go even further, acting as a gateway that enables commercial products to interact with each other even when manufacturers do not support competitors' devices

### Sensors and Actuators in IoT:

> **Definition**
>
>"**Sensors** are devices that **convert physical activity or changes into an electrical signal**, while **actuators are transducers** that **take one form of energy as input** and **produce some form of motion**, movement, or action"
>
>Read more (optional read): [https://www.sciencedirect.com/topics/computer-science/sensors-and-actuator#definition](https://www.sciencedirect.com/topics/computer-science/sensors-and-actuator#definition)

#### Sensor types in IoT

In Ambient Intelligence (AmI) environments, a variety of sensors are utilized to collect data about the physical world, human activities, and environmental conditions. These sensors play a crucial role in enabling intelligent systems to perceive, understand, and adapt to their surroundings. The following are some of the most common sensors utilized:

1. **Motion Sensors:** Motion sensors detect movement within their field of view using technologies such as passive infrared (PIR), ultrasonic, or microwave sensors. They are commonly used in smart home security systems, occupancy detection, and activity monitoring.
	* Some examples are:
		* Texas Instruments (mmWave): [https://www.ti.com/lit/spyy005](https://www.ti.com/lit/spyy005)
		* Most common PIR sensor: [https://learn.adafruit.com/pir-passive-infrared-proximity-motion-sensor/overview](https://learn.adafruit.com/pir-passive-infrared-proximity-motion-sensor/overview)

2. **Temperature and Humidity Sensors:** These sensors measure ambient temperature and humidity levels. They are vital for climate control systems, energy management, and environmental monitoring in smart buildings.
	- Examples:
		- The DHT11: [https://learn.adafruit.com/dht/overview](https://learn.adafruit.com/dht/overview)
		- Flood detection: [https://www.shelly.com/en-us/products/shop/shelly-flood-1](https://www.shelly.com/en-us/products/shop/shelly-flood-1)

3. **Light Sensors:** Light sensors, such as photodiodes or photoresistors, measure the intensity of ambient light. They are used for automatic lighting control, daylight harvesting, and optimizing energy usage in indoor and outdoor lighting systems.
	- Examples: components LDR 05, XD-80

4. **Proximity Sensors:** Proximity sensors detect the presence or absence of nearby objects without physical contact. They are employed in smart appliances, touchless interfaces, and object detection applications.
	- Example: Lidar-based smart vacuum cleaners, sonar, etc.

5. **Pressure Sensors:** Pressure sensors measure force or pressure applied to a surface. They are used in smart home devices like smart mattresses for sleep monitoring, etc.
	- Example: smart mattresses, etc. 

6. **Gas and Air Quality Sensors:** These sensors monitor the levels of various gases and pollutants in the air, including carbon dioxide, carbon monoxide, volatile organic compounds (VOCs), and particulate matter. They are essential for indoor air quality monitoring, pollution detection, and ventilation control.
	- Example: Aqara TVOC [https://www.aqara.com/us/product/tvoc-air-quality-monitor/](https://www.aqara.com/us/product/tvoc-air-quality-monitor/)

7. **Sound and Noise Sensors:** Sound sensors capture audio signals and detect noise levels in the environment. They are utilized in smart home security systems, noise monitoring, and acoustic event detection.
	- Example: any microphone or smart voice assistant (e.g. Amazon Echo Dot)

8. **Biometric Sensors:** Biometric sensors measure unique biological traits such as fingerprints, facial features, or heart rate. They are used for user authentication, health monitoring, and personalized services
	- Example: an smart medicine dispenser with user recognition

9. **Gesture Recognition Sensors:** Gesture recognition sensors detect and interpret human gestures and movements. They enable intuitive user interfaces and gesture-based control in smart devices, interactive displays, and wearable technology.	- Example: Leap Motion [https://www.ultraleap.com/](https://www.ultraleap.com/)

10. **Occupancy and Presence Sensors:** These sensors detect the presence of people within a space. They are used for occupancy sensing, crowd monitoring, and smart lighting control in buildings and public spaces.
	- Example: Smart surveillance cameras, specialized occupancy sensors, etc.

#### Actuators

Actuators are devices that convert electrical signals or energy into physical actions or movements. In the context of IoT and Ambient Intelligence (AmI) environments, actuators enable systems to interact with and affect the physical world based on data inputs and decisions taken by the ML-enabled components.

1. **Motorized Actuators:** Motorized actuators convert electrical energy into mechanical motion. They are used in various IoT devices for controlling the movement of physical objects, such as opening and closing doors, windows, curtains, blinds, or adjusting the position of robotic arms and mechanisms.
	- Common examples: garage door motors, automated blinds
    
2. **Solenoid Actuators:** Solenoid actuators use electromagnetic force to produce linear motion. They are employed in IoT systems for tasks such as locking and unlocking doors, valves, or latches, as well as in automotive applications for controlling fluid flow and pneumatic systems.
	- Common example: building's main door latch (e.g. activated from entryphone)
    
3. **Relays and Electromagnetic actuators:** Relays are electromagnetic switches that control the flow of electricity between circuits. They are utilized in IoT devices for switching power on or off to connected electrical devices, such as lights, appliances, or heating systems. Similarly, electromagnetic actuators use electromagnetic force to produce linear or rotary motion. They are utilized in IoT systems in home automation or industrial control applications.
	- Example: smart switches, smart plugs, fire door release mechanisms
    
4. **Servo Motors:** Servo motors are rotary actuators that provide precise control over angular position, velocity, and acceleration. They are commonly used in robotics, drones, camera gimbals, and IoT devices requiring precise motion control.
	- Examples: robotic arms, pan-tilt-zoom cameras, or automated surveillance systems.
    
5. **Pneumatic and Hydraulic Actuators:** Pneumatic and hydraulic actuators use compressed air or fluid pressure to generate mechanical motion. They are employed in industrial IoT applications for tasks such as controlling valves, pumps, and robotic manipulators in manufacturing, process automation, and heavy machinery.
	- Examples: Elevators, some mechanical beds
    
6. **Piezoelectric Actuators:** Piezoelectric actuators generate mechanical motion in response to an applied voltage. They are used in IoT devices for precise positioning, vibration control, and haptic feedback in touchscreens, medical devices, and consumer electronics.
	- Example: smart phones and tablets
    
7. **Shape Memory Alloys (SMAs):** SMAs are materials that change shape in response to temperature changes or applied stress. They are used in IoT devices for shape memory actuators, such as smart valves, adaptive structures, and biomedical implants.
	- Read more (optional): [https://en.wikipedia.org/wiki/Shape-memory_alloy](https://en.wikipedia.org/wiki/Shape-memory_alloy)
    
### Sensor Data Processing and Analysis

Sensor data processing and analysis are essential components of IoT systems, enabling the **extraction of knowledge from data**, as well as actionable information from raw sensor data. In sensor data processing, collected data undergoes various stages of transformation, including **filtering, aggregation, and normalization**, to ensure its accuracy, reliability, and usability. Once processed, the data is then subjected to analysis techniques such as **statistical analysis, machine learning, and data mining** to **uncover patterns, trends**, and correlations. This analysis enables IoT systems to derive meaningful understanding, predict future outcomes, and make informed decisions in real-time. Sensor data processing and analysis has multiple applications, such as: anomaly detection, environmental monitoring, and personalized services.

The following figure[^5] shows how the process of training an ML model based off of historical (temporally-aggregated) IoT data: 
![](https://media.licdn.com/dms/image/D5612AQHX6C9QXC32fg/article-inline_image-shrink_1500_2232/0/1695955563599?e=1717632000&v=beta&t=N6C-PYGPVkPN2fYGCQruvqgqQqikdCcOySQVnd2gcHE)

> **Important**
>
>**Mandatory read:** Understand the applications of DL in IoT (Sec. IV), as well as how IoT data can be aggregated and incorporated into different deep learning (DL) models (Sec. V).
>
>Mohammadi *et al.* 2018 "Deep Learning for IoT Big Data and Streaming Analytics: A Survey" [https://doi.org/10.1109/COMST.2018.2844341](https://doi.org/10.1109/COMST.2018.2844341)



> **Note**
>
>**Optional read:** Alghanmi *et al.* 2021 "Machine Learning Approaches for Anomaly Detection in IoT: An Overview and Future Research Directions" [https://doi.org/10.1007/s11277-021-08994-z](https://doi.org/10.1007/s11277-021-08994-z)

[^5]: Image from: [https://www.linkedin.com/pulse/beginners-guide-machine-learning-iot-controls-mlot-part-1-okechukwu/](https://www.linkedin.com/pulse/beginners-guide-machine-learning-iot-controls-mlot-part-1-okechukwu/)

### IoT Areas of application

#### IoXT: Internet of 'X' Things

Since the inception of the Internet of Things (original IoT), several other acronyms have appeared for specialized variants, to better explain certain fields of application of IoT technologies. Today we see a plethora of variants, such as:

- **Internet of Robotics Things** (IoRT)
- Consumer or **Commercial Internet of Things** (CIoT)
- **Internet of Industrial Things** (IIoT) or Industrial Internet of Things
- **Internet of Military Things** (IoMT)
- **Internet of Educational Things** (IoET) (e.g. [https://doi.org/10.1016/j.iot.2022.100558](https://doi.org/10.1016/j.iot.2022.100558) )
- etc.

> **Note**
>
> Optional read: "Internet of Things: The Five Types of IoT"
> [https://syntegra.net/internet-of-things-the-five-types-of-iot/](https://syntegra.net/internet-of-things-the-five-types-of-iot/)
>
> Optional read: "The Role of IoT in Education"
> [https://www.arduino.cc/education/the-role-of-the-iot-in-education](https://www.arduino.cc/education/the-role-of-the-iot-in-education)

However, due to the nature of our course we will focus next on the **Internet of Health(y) Things**.

#### IoHT: Internet of Health(y) Things

We have already delved into the application of IoT devices as part of ambient intelligence (AmI) in the **context of smart homes and their automation**. Furthermore we have explored that the aims of this might be several: energy efficiency, increased comfort of its inhabitants, etc. However, as we have also emphasized, AmI 4 AHA and AAL are the fields in which ambient intelligence, and particularly IoT devices, can provide more societal benefits.

As part of this AmI 4 AHA effort, the **Internet of Health(y) Things** (IoHT), or the **Healthcare Internet of Things** (H-IoT) emerges as a field in which the devices that are connected and interact with each other and cloud services are related to the provision of care and/or health condition management, or prevention.

Of particular interest, in the field of AmI4AHA, or AAL, is the part of IoHT that considers the wearable technologies and IoT-based applications to support independent living of older adults, so that they can remain in their preferred environment longer.

> **Important**
>
>**Mandatory reads:**
> 
> - Baig *et al.* 2019 "A Systematic Review of Wearable Sensors and IoT-Based Monitoring Applications for Older Adults" [https://doi.org/10.1007/s10916-019-1365-7](https://doi.org/10.1007/s10916-019-1365-7)

Other IoHT solutions focus further in the applications within hospitals, or care facilities, as well as in-home e-health and tele-health provision.

> **Note**
> 
> **Optional reads:**
>
> - Selvaraj *et al.* 2020 "Challenges and opportunities in IoT healthcare systems: a systematic review" [https://doi.org/10.1007/s42452-019-1925-y](https://doi.org/10.1007/s42452-019-1925-y)
>
> - Mishra *et al.* 2019 "IoT Health care Monitoring and Tracking: A Survey" [https://doi.org/10.1109/ICOEI.2019.8862763](https://doi.org/10.1109/ICOEI.2019.8862763)
>
> - **Example application:** Bassoli et al. 2017 "An IoT approach for an AAL Wi-Fi-based Monitoring System" [https://doi.org/10.1109/TIM.2017.2753458](https://doi.org/10.1109/TIM.2017.2753458)

#### Intelligent Environments: beyond the house

**Intelligent Workspaces** leverage IoT technologies and advanced automation to enhance productivity, efficiency, and **user experience within office environments**. These environments i**ntegrate sensors, smart devices, and data analytics** to optimize workspace **layout, lighting, temperature**, and **resource allocation** based on real-time usage patterns and employee preferences. For instance, think of a co-working space in which seats can be booked if not currently in use: sensors are needed to detect currently vacant seats, and a dynamic booking system to allow for seat booking in real time. Additionally, intelligent workspaces often incorporate smart meeting rooms, digital collaboration tools, and personalized workplace assistants to streamline communication, collaboration, and task management, fostering a more dynamic and adaptable work environment.

**Smart Building Management Systems.** Smart buildings utilize IoT technologies to enhance operational efficiency, **occupant comfort, and sustainability**. They integrate interconnected **sensors, actuators, and control systems** to optimize energy usage, indoor air quality, and facility management. Smart buildings also enable **predictive maintenance** (for instance, smart lights informing the maintenance team of their end of life approaching), real-time **monitoring**, and adaptive control strategies to **minimize costs**, reduce **environmental impact**, and create more responsive and sustainable built environments.

**Energy Efficiency in Intelligent Environments.** Energy efficiency in intelligent environments involves leveraging IoT technologies and data-driven approaches to optimize energy usage and reduce wastage. By integrating **sensors, smart meters, and energy management** systems, intelligent environments can **monitor and analyse energy consumption patterns** in real-time. This enables automated **adjustments to lighting, heating, cooling**, and other systems based on **occupancy**, environmental conditions, and energy demand.

### Data Security and Privacy:

By definition, the IoT encompasses a vast network of interconnected physical objects globally, linked via the Internet. Envisioned to interconnect trillions of intelligent objects daily, **these entities possess the capacity to gather, process, and communicate data regarding themselves and their surroundings**. Prominent examples of IoT applications span various domains, including **very sensitive information** such as in **healthcare**, smart city **infrastructure**, **surveillance** systems, and data acquisition in public and **defence** sectors.

Recent technological advancements have yielded smart sensor nodes and RFIDs, leading to **a large number of wireless networks** filled with intelligent **devices continuously transmitting data** to the Internet. **Securing and preserving the privacy** of this data within the IoT framework **poses an enormous challenge**, that needs to be given priority for present and future applications.

Devices such as smart phone, WSNs and RFIDs etc., are the major components of IoT network which are basically **resource constrained devices**. Consequently, the design and implementation of security and privacy management schemes demand consideration of factors like **performance optimization, minimal power consumption, resilience against attacks, data tampering prevention, and end-to-end security assurance**. Security measures within IoT frameworks safeguard against unauthorized access, data alterations, or destruction, while privacy protocols aim to uphold individuals' rights to control the usage and purpose of collected information.

> **Note**
>
>**Optional (but *highly* recommended) reads:**
> - Chanal *et al.* 2020 "Security and Privacy in IoT: A Survey" [https://doi.org/10.1109/JIOT.2019.2898113](https://doi.org/10.1109/JIOT.2019.2898113)
> - "Cryptography Key Management, Authentication and Authorization for IoT"
> - [https://medium.com/@preetirajesh400/cryptography-key-management-authentication-and-authorization-for-iot-4198dfa0481b](https://medium.com/@preetirajesh400/cryptography-key-management-authentication-and-authorization-for-iot-4198dfa0481b)


> **Note**
>
>**News on Bluetooth vulnerabilities (optional read):**
>[https://www.kaspersky.com/blog/bluetooth-vulnerability-android-ios-macos-linux/50038/](https://www.kaspersky.com/blog/bluetooth-vulnerability-android-ios-macos-linux/50038/)
>**Examples of vulnerabilities:**
>[https://www.keyfactor.com/education-center/iot-device-security/](https://www.keyfactor.com/education-center/iot-device-security/)

### Ethical and Social Implications:

The proliferation of IoT technology brings forth a series ethical and social implications that require careful consideration. **Privacy concerns** arise as IoT **devices continuously collect**, **transmit, and analyze** personal data, raising **questions about consent**, **data ownership**, and surveillance.

**Security vulnerabilities** in IoT systems pose risks of **unauthorized access**, **data breaches**, and manipulation, threatening individuals' safety and privacy. Moreover, the deployment of IoT technologies in critical infrastructure, **such as healthcare and transportation**, raises concerns about **reliability**, **accountability**, and potential consequences of system failures.

Additionally, the digital divide **exacerbates societal inequalities**, as access to and benefits from **IoT technologies may not be equally distributed across populations**. Ethical dilemmas emerge regarding the ethical use of AI algorithms in decision-making processes, potential biases, and unintended consequences.

**Example -- Barriers for adoption in IoHT:** On of the main challenges faced by technologies such as the ones presented today (IoT, but particularly IoHT), is that of **user acceptability**. The following figure[^6] shows the four biggest barriers:

1. Having to wear a device that can be **stigmatizing** (i.e. shows weakness or lack of independence) is often a barrier for adoption.
2. **Data collection and processing** itself might be perceived oftentimes as a threat that hinders acceptability.
3. **Constant alerts** and warnings can be seen as an **annoyance** by end users, or perceived as **patronizing**, and have to be well-timed for assistance **when required only**.
4. Finally, **acceptability** is dicreased by poor **usability** of the system (i.e. design that is not well-thought or that didn't involve the end users' needs).

<img src="https://media.springernature.com/lw685/springer-static/image/art%3A10.1007%2Fs10916-019-1365-7/MediaObjects/10916_2019_1365_Fig2_HTML.png?as=webp" width="450px"/>
[^6]: Figure from: [https://doi.org/10.1007/s10916-019-1365-7](https://doi.org/10.1007/s10916-019-1365-7)

### Conclusion and Recap:

In this lesson, we have presented the possibilities that the Internet of Things (IoT) concept opens for us. We have seen how, contrary to the concept of ambient intelligence, that focuses on the deployment of sensors into the environment and the prediction of user needs, the **concept of IoT is _closer_ to the hardware**, as it is the network of connected _things_ that can be any everyday object that is network-capable thanks to the emergence of cost-reduced integrated circuits that implement a full network stack. Alternatively a hub or gateway that can connect to the Internet provides access for a network of devices that transmit via a restricted bandwidth network infrastructure (such as Zigbee, Z-Wave, etc).

We have also explored the IoT ecosystem and its components: **edge** and cloud **computing**,  and **machine learning** (ML/AI). We have also briefly introduced the **protocols and standards** that exist in the IoT field.

Additionally, we have introduced the most common **types of sensors and actuators**, with some examples. Moreover, we have delved into the processing of data by machine learning techniques, particularly **deep learning methodologies**.

To finalize, we have covered the **data security, privacy**, as well as **social and ethical questions** raised by IoT usage and spread.

### References:

> **Warning**
>
> References have been ***included along the text***, please review the material and find tip boxes marked as **Important**, which contain mandatory reading material.
> 
> As explained in the previous chapter, **a test will be conducted** including topics covered in this material.
