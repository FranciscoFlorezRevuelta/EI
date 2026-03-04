# Intelligent environments

## Objectives

- Build a strong understanding of **Ambient Intelligence (AmI)** and how it provides the conceptual and technological basis for **intelligent environments** and **enhanced living and working spaces**.
- Explain the key technologies behind AmI: **sensing**, **communication networks**, **user interfaces**, **data processing**, **AI**, and **actuation**. Show how they combine in **IoT**, **AI-enabled services**, and **natural interaction** to create intelligent environments.
- Analyse how AmI principles and technologies are applied in **Ambient Assisted Living**, **smart buildings**, **smart cities**, and **smart industry**, focusing on practical impact and what these applications can change.
- Develop a critical view of AmI: benefits (quality of life, efficiency, safety, comfort) and challenges (privacy, security, interoperability, bias, and wider ethical issues).
- Introduce the main **legal, regulatory, and ethical** frameworks that shape the design, deployment, and governance of AmI systems.

## Introduction

Ambient Intelligence (AmI) builds on ideas from Mark Weiser’s vision of **ubiquitous computing** in the early 1990s. Weiser argued that the most useful technologies are those that “disappear” into everyday life: present and helpful, but not demanding constant attention. AmI takes this further by focusing on environments that can **sense what is happening**, **understand context**, and **respond** in ways that support people. The aim is not to fill spaces with gadgets. The aim is to create systems that fit around human routines, reduce effort, and improve safety, comfort, and wellbeing, while staying as unobtrusive as possible.

In practice, AmI sits alongside two related terms: **Intelligent Environments (IE)** and **Enhanced Living Environments (ELE)**. These terms overlap, but they come from slightly different communities and emphasise different goals.

- **Ambient Intelligence (AmI)**  
  AmI refers to digital systems embedded in the environment that are **context-aware**, **adaptive**, and often **proactive**. They use sensing, connectivity, and AI to personalise support and to respond to people and situations. A key feature is that the interaction should feel natural and low-effort, with much of the computation happening in the background.

- **Intelligent Environments (IE)**  
  IE is a broader umbrella term for spaces (rooms, buildings, campuses, cities) that use integrated technology to **monitor**, **reason**, and **act**. An IE may focus on energy, safety, access control, logistics, or user experience. It often highlights the environment as a system: sensing infrastructure, data processing, and actuation working together.

- **Enhanced Living Environments (ELE)**  
  ELE usually refers to applying AmI/IE ideas to **homes and everyday living spaces**, with an explicit focus on **quality of life**. This often includes support for older people, people with disabilities, and people living with chronic conditions. Typical examples include assistive home automation, health and activity monitoring, and safety support.

In short: **AmI** is a guiding paradigm for human-centred, context-aware support; **IE** describes the broader class of smart, responsive spaces; and **ELE** focuses on living spaces where the main goal is improving daily life, health, and wellbeing. Together, they define a shift from “people adapting to technology” towards “technology adapting to people”.

Mandatory readings: 
> * Weiser, M. (1991). [The Computer for the 21st Century](https://www.jstor.org/stable/pdf/24938718.pdf). Scientific american, 265(3), 94-105. 
> * Augusto, J. C., Callaghan, V., Cook, D., et al. (2013). [Intelligent Environments: a manifesto](https://hcis-journal.springeropen.com/counter/pdf/10.1186/2192-1962-3-12.pdf). Human-Centric Computing and Information Sciences, 3(12).
> * Dunne, R., Morris, T., & Harper, S. (2021). [A survey of ambient intelligence](https://dl.acm.org/doi/pdf/10.1145/3447242). ACM Computing Surveys (CSUR), 54(4), 1-27.

Optional readings:
> * Friedewald, M., & Da Costa, O. (2003). [Science and technology roadmapping: Ambient intelligence in everyday life (AmI@ Life)](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=2445733d5686cacdee6fce7ccd1398b1b2517462) (pp. 1-197). Working Paper. Seville: Institute for Prospective Technology Studies IPTS. 
> * Ducatel, K., M. Bogdanowicz, F. Scapolo, J. Leijten & J-C. Burgelman (2001) [Scenarios for ambient intelligence in 2010](http://www.ist.hu/doctar/fp5/istagscenarios2010.pdf). Seville: Institute for Prospective Technology Studies IPTS. (This is a very interesting document about what was foreseen to be the applications of AmI in 2010)

## Basic principles

Ambient Intelligence (AmI) aims to make environments supportive, adaptive, and easy to use. The system should fit around people, not the other way round. The principles below describe what “good” AmI looks like.

- **Context awareness**  
  The system senses its surroundings and interprets what is happening. Context can include location, time, activity, social setting, and relevant environmental conditions. The goal is not to collect everything, but to collect what is needed to make a good decision.

- **Ubiquity and unobtrusiveness**  
  Computing is embedded across the environment (objects, rooms, infrastructure), but it should not demand attention all the time. The best AmI support often feels “in the background”.

- **Responsiveness**  
  The environment reacts to changes in the user or the setting. This can be immediate (turning on lights when someone enters) or delayed (adjusting heating based on daily routines). Responsiveness must be reliable and predictable.

- **Personalisation and adaptation**  
  AmI should adjust to individual needs and preferences, and it should improve over time. This can include learned routines, accessibility needs, or preferred interaction styles. Personalisation must remain transparent and controllable.

- **Anticipation (proactivity)**  
  The system can suggest or trigger actions before the user asks, based on context and learned patterns. Proactivity must be careful: it should reduce effort, not remove autonomy or cause surprise.

- **Natural and seamless interaction**  
  Interaction should be low-friction. Instead of relying only on explicit commands, AmI can use speech, gestures, mobile devices, wearables, or implicit signals (for example, behaviour and routine). When the system acts, it should make the action and the reason easy to understand.

- **Intelligence and autonomy**  
  AmI uses AI to infer context, make decisions, and coordinate devices. Autonomy should be bounded: the system must know when to act alone, when to ask, and when to hand control back to the user.

- **Privacy, security, and trust by design**  
  AmI often involves sensitive data and continuous sensing. Systems must minimise data collection, protect data in transit and storage, and resist misuse. Trust also depends on good defaults, clear consent, and meaningful user control.

## Key technologies

Ambient Intelligence (AmI) relies on a set of technologies that work together to sense what is happening, interpret it, decide what to do, and then act. A useful way to think about AmI is as a loop:

**sense → communicate → understand → decide → act → learn**

### Sensor technology (sensing the environment)
Sensors provide the raw signals that make context awareness possible. They can measure:
- **environmental conditions** (temperature, light, air quality, noise)
- **presence and movement** (PIR, radar, depth cameras, pressure mats)
- **identity and access** (badges, biometrics, device proximity)
- **health and activity** (wearables, heart rate, sleep, activity patterns)

Good sensing is not “more sensors”. It is the right sensors, placed well, with known limitations.

### Communication networks (moving data and control)
AmI needs reliable connectivity so devices and services can share data and coordinate actions. This includes:
- **local networks** (Wi-Fi, Ethernet)
- **low-power and short-range** (Bluetooth LE, Zigbee, Thread)
- **wide-area connectivity** (4G/5G, LPWAN options such as LoRaWAN)
- **protocols and messaging** (MQTT, HTTP/REST, event streams)

Network choices affect latency, reliability, power use, and security.

### User interface technology (interaction and control)
AmI must allow people to understand what the system is doing and to stay in control. Interfaces include:
- **mobile and wearable interfaces**
- **touch and displays** (panels, TVs, smart displays)
- **voice interaction**
- **gesture-based and multimodal interaction**
- **notifications and explainable feedback** (what happened, why, and what you can change)

Accessibility and clarity matter as much as “smartness”.

### Data processing and AI (making sense of signals)
This is where AmI becomes intelligent. Typical building blocks include:
- **signal processing and data cleaning**
- **sensor fusion** (combining sources to reduce uncertainty)
- **context modelling** (rules, probabilistic models, knowledge graphs, ontologies)
- **machine learning** (classification, prediction, anomaly detection)
- **activity recognition and behaviour modelling**
- **personalisation** (user models, preference learning)

AI must be robust to noise, missing data, and domain shift (real homes and buildings are messy).

### Actuators (changing the environment)
Actuators turn decisions into effects. Examples include:
- **lighting, heating, ventilation, blinds**
- **locks and access systems**
- **alarms and safety features**
- **robots or assistive devices**
- **industrial control actions**

Actuation must be safe, reversible where possible, and designed with clear fallback modes.

### Three useful “bundles” to remember
You can group AmI technologies into three interlinked bundles:

- **IoT**: connected sensors and actuators that make the environment observable and controllable.
- **AI**: models that infer context, predict needs, and support decisions under uncertainty.
- **Natural interaction**: interaction methods that fit human behaviour (voice, gesture, routines), plus feedback that keeps people informed and in control.

Together, these bundles enable environments that can perceive, reason, and respond in ways that support everyday life.

## Applications

Ambient Intelligence (AmI) is not a single product. It is a way of designing systems where sensing, connectivity, AI, and actuation work together to support people in real settings. Applications vary by domain, but they share the same core pattern: **understand context → decide → support action**.

Below are four common application domains.

### Ambient Assisted Living (AAL)

**Ambient Assisted Living (AAL)** integrates technology into living environments to support people who may need assistance, including **older people**, **frail people**, and **people with disabilities**. The main goal is to help people live safely and independently for longer, while also supporting families and care services.

Typical AAL functions include:
- activity and wellbeing monitoring (with clear consent and limits)
- safety support (falls, hazards, wandering, emergency response)
- medication and routine support
- social connection and participation
- caregiver support and care coordination

Main objectives of AAL often include:
- help people live longer in their preferred environment, with more autonomy and confidence
- support health, function, and daily routines
- encourage healthier lifestyles for people at risk
- improve safety and reduce social isolation
- support caregivers and care providers
- use resources more efficiently in ageing societies

Mandatory reading:
> * Colantonio, S., Aleksic, S., Calleja Agius, J., Camilleri, K. P., Čartolovni, A., Climent-Pérez, P., ... & Zgank, A. (2025). [A historical view of active assisted living](https://link.springer.com/chapter/10.1007/978-3-031-84158-3_1). In Privacy-Aware Monitoring for Assisted Living: Ethical, Legal, and Technological Aspects of Audio-and Video-Based AAL Solutions (pp. 3-44). Cham: Springer Nature Switzerland.

### Smart homes and smart buildings

**Smart homes** use connected devices, sensors, and automation to support daily living in domestic spaces. The focus is often on comfort, convenience, safety, energy use, and accessibility. Modern systems may learn routines, but they must remain understandable and controllable.

Common smart home functions include:
- lighting and climate automation
- security and access control
- appliance monitoring and energy optimisation
- assistive features (for example, voice control or reminders)

**Smart buildings** apply similar ideas at a larger scale (offices, campuses, hospitals). They aim to improve performance across:
- energy and carbon reduction (HVAC, lighting, occupancy-aware control)
- space utilisation (how rooms are used, capacity management)
- maintenance (fault detection, predictive maintenance)
- safety and security

Mandatory readings:
> * Sovacool, B. K., & Del Rio, D. D. F. (2020). [Smart home technologies in Europe: A critical review of concepts, benefits, risks and policies](https://www.sciencedirect.com/science/article/pii/S1364032119308688). *Renewable and Sustainable Energy Reviews*, 120, 109663.  

Optional reading:
> * Al Dakheel, J., Del Pero, C., Aste, N., & Leonforte, F. (2020). [Smart buildings features and key performance indicators: A review](https://www.sciencedirect.com/science/article/pii/S2210670720305497). *Sustainable Cities and Society*, 61, 102328.

### Smart cities

**Smart cities** use sensing, connectivity, and data-driven decision-making to improve urban services and quality of life. The aim is not only efficiency, but also sustainability, resilience, and inclusion.

Common smart city areas include:
- mobility (traffic management, public transport optimisation, micromobility)
- energy (smart grids, demand response, street lighting)
- environment (air quality, noise, heat, flooding)
- waste and water management
- public safety and emergency response
- citizen services and participation

Mandatory reading:
> * Law, K. H., & Lynch, J. P. (2019). [Smart city: Technologies and challenges](https://iopscience.iop.org/article/10.1088/1757-899X/365/2/022039/pdf). *IT Professional*, 21(6), 46–51.

### Smart industry

**Smart industry** (often linked to **Industry 4.0**) integrates digital technologies into industrial processes so systems can monitor themselves, adapt, and optimise performance. Key ideas include **cyber-physical systems**, industrial IoT, robotics, and data-driven optimisation.

Typical applications include:
- real-time monitoring and quality control
- predictive maintenance and fault detection
- flexible production and mass customisation
- worker safety systems (risk detection, ergonomics, access control)
- supply chain visibility and optimisation
- digital twins for simulation and planning

Mandatory reading:
> * Lasi, H., Fettke, P., Kemper, H. G., Feld, T., & Hoffmann, M. (2014). [Industry 4.0](https://link.springer.com/article/10.1007/s12599-014-0334-4). *Business & information systems engineering*, 6(4), 239-242.


## Benefits and challenges

Ambient Intelligence (AmI) can improve daily life and system performance, but it also introduces risks that you must manage. A useful way to think about this section is: **what AmI can improve** and **what can go wrong if design and governance are weak**.

### Benefits

- **Better quality of life**: AmI can reduce friction in everyday tasks, support independence, and improve comfort by adapting the environment to people’s needs.

- **Personalisation**: Systems can adapt to routines, preferences, and accessibility needs. This can be useful in homes, workplaces, education, and care settings.

- **More natural interaction**: Voice, gesture, mobile interaction, and context-aware interfaces can reduce the effort needed to control technology and can improve accessibility.

- **Real-time awareness and decision support**: AmI can process signals as situations change (for example, safety monitoring, building control, traffic management, or industrial supervision).

- **Efficiency and sustainability**: Context-aware control can reduce energy and resource use (lighting, HVAC, water, logistics), lowering costs and environmental impact.

- **Safety and security support**: Systems can detect hazards (falls, smoke, gas leaks, unsafe temperatures, unauthorised access) and trigger alerts or mitigation actions.

- **Support for older people and people with disabilities**: AmI can enable safer independent living through reminders, monitoring, assistive control, and links to caregivers and services.

- **Improved service delivery (including healthcare and maintenance)**: Continuous monitoring and early detection can support timely intervention, reduce avoidable incidents, and improve operational planning.

- **Better work environments**:  Occupancy-aware comfort control, safety monitoring, and resource management can improve wellbeing and productivity.

### Challenges

- **Privacy**:  Many AmI systems rely on continuous sensing and inference about behaviour. This can expose sensitive information, even when systems do not store “obvious” identifiers.

- **Security**: Connected devices expand the attack surface. Compromised sensors, hubs, or cloud services can lead to data breaches and unsafe actuation.

- **Interoperability and vendor lock-in** Devices and platforms often use different standards and ecosystems. Poor interoperability increases cost, complexity, and long-term dependence on vendors.

- **Reliability in real settings**: Homes, cities, and factories are noisy and unpredictable. Sensors fail, data goes missing, and models can behave poorly outside the conditions they were trained on.

- **Data management**: AmI produces large, continuous data streams. You must manage storage, latency, data quality, and data governance across the system lifecycle.

- **Cost and maintenance**: Deployment costs can be high, but so can ongoing costs: calibration, replacements, updates, cybersecurity patching, and support.

- **User acceptance and trust**: People may reject systems that feel intrusive, confusing, or controlling. Trust depends on transparency, meaningful consent, and the ability to override or opt out.

- **Ethical and societal issues**: Risks include loss of autonomy, over-reliance on automation, bias and unequal performance across groups, and unclear accountability when systems fail.

- **Legal and regulatory uncertainty**: Liability, data protection, safety obligations, and AI governance can be complex, especially in multi-stakeholder environments (home + care provider + insurer + platform).

A successful AmI system balances usefulness with safeguards: **minimise data**, **secure the stack**, **design for failure**, and **keep humans in control**.

Mandatory viewings:
> * [What is the GDPR? | A summary of the EU GDPR](https://www.youtube.com/watch?v=Assdm6fIHlE)

Mandatory readings: 
> * [High-level summary of the AI Act](https://artificialintelligenceact.eu/high-level-summary/)
> * Čartolovni, A., Dantas, C., Malešević, A., & Ilgaz, A. (2025). [Ethical issues in AAL](https://doi.org/10.5281/zenodo.6793617). In Privacy-Aware Monitoring for Assisted Living: Ethical, Legal, and Technological Aspects of Audio-and Video-Based AAL Solutions (pp. 277-289). Cham: Springer Nature Switzerland - Section 5. Ethical Principles in AAL.
> * GoodBrother COST Action (2022). [State of the art in privacy preservation in video data](https://doi.org/10.5281/zenodo.6806207) - Section 2. Privacy by design.

Optional readings:
> * [AI Act](https://data.consilium.europa.eu/doc/document/ST-5662-2024-INIT/en/pdf)
> * [General Data Protection Regulation](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A32016R0679)

## Moodle test

* The moodle test will be developed during practice sessions on **Friday 20 March at 4.15pm CET**.
* The test has a maximum duration of 30 minutes from the start.
* The test consists of 20 triple choice questions.
* Each wrong answer subtracts 1/3 of the value of a correct answer.
* The mark for the test will be considered as one of the marks for the theoretical part of the course. See the overall evaluation of the course in the general conditions.
* The questions will be based on this webpage and all the mandatory readings proposed. The test will also include questions about the module on the Internet of Things.


