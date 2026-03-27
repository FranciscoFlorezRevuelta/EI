# Computer vision for AAL

## Introduction

Ambient Assisted Living (AAL) uses information and communication technologies to support **independent, healthy living** for **older people** and **people with disabilities**. AAL services often operate in homes, workplaces, and public spaces. They rely on sensors embedded in the environment (for example, motion sensors or door contacts) and sensors worn by the user (for example, smartwatches). These sensors capture signals about the person and their surroundings. Systems then interpret the data to provide support, such as reminders, safety alerts, or links to caregivers.

Recent progress in **wearables** and **mobile health** has made continuous support more realistic. Devices such as smartwatches, wristbands, smart glasses, and smartphones can collect data over long periods. This can include physiological signals (for example, heart rate), movement, location, and daily routines. “Lifelogging” approaches extend this idea by recording parts of everyday life to support wellbeing and independence. In AAL, these data streams can enable services such as wellbeing monitoring, activity support, memory support, improved social participation, caregiver support, and risk detection (for example, increased fall risk).

Computer vision adds another sensing option. Cameras can capture richer information than many traditional AAL sensors, especially for **activity understanding**, **safety monitoring**, and **context recognition**. Two main approaches are common:

- **Third-person vision**: cameras placed in the environment to observe activity in a room or home.
- **Egocentric vision**: a camera worn on the head or torso to capture the user’s point of view.

Both approaches can strengthen AAL services, but they also raise practical and ethical issues (privacy, consent, bystanders, security, and trust). These constraints strongly shape how vision-based AAL systems should be designed and deployed.

## Video-based AAL applications

Video-based AAL uses cameras plus computer vision to support safety, independence, and care. These applications often work best when they are **focused on specific risks or tasks**, and when the system design limits data capture and protects privacy.

- **Fall detection and alerting**
  Cameras can detect falls by analysing posture, movement, and transitions (for example, standing → lying). The system can then trigger an alert to a caregiver or service.  
  *Key challenge:* false alarms can overwhelm users and carers, while missed detections can be high-risk.

- **Activity monitoring (ADLs and routines)**
  Vision can support monitoring of activities of daily living (for example, eating, walking, getting up at night). Over time, the system can detect meaningful changes in routine that may indicate declining mobility, illness, fatigue, or emerging care needs.  
  *Key challenge:* homes vary widely, and routine changes can have benign causes (visitors, holidays, new habits).

- **Safety monitoring in high-risk areas**
  In kitchens, bathrooms, and stairs, video can help detect safety-relevant situations (for example, a person on the floor, a long period of inactivity, or risky use of appliances). Systems can also support “check-in” workflows rather than fully automatic escalation.  
  *Key challenge:* these are also the most privacy-sensitive spaces, so design choices matter.

- **Non-contact health and wellbeing signals (limited use cases)**
  Some methods aim to estimate physiological signals from video (for example, heart-rate related signals under controlled conditions). In AAL, these approaches are best treated as **research or niche options**, because performance can degrade with lighting changes, motion, camera quality, and skin-tone differences.  
  *Key challenge:* reliability and fairness in real homes.

- **Social and emotional wellbeing support (use with caution)**
  Video can support wellbeing indirectly (for example, detecting social isolation risk through activity patterns). Direct “emotion recognition” from facial expressions is a high-risk use case: it is context-dependent and can be inaccurate or culturally biased.  
  *Safer framing:* support carers with behavioural indicators and user-reported input, rather than inferring emotions as facts.

- **Prompting and memory support**
  Vision can detect relevant context (for example, a person approaching the door, preparing food, or searching for an object) and trigger reminders such as medication prompts or step-by-step task support.  
  *Key challenge:* prompts must be timely and helpful, not distracting or controlling.

These applications can improve safety and reduce caregiver workload, but only when systems are **reliable**, **transparent**, and **designed for real homes**. In practice, successful video-based AAL systems combine technical performance with strong privacy-by-design choices, clear user control, and well-defined escalation pathways.

Mandatory readings: 
> * GoodBrother COST Action (2022). [State of the Art of Audio- and Video-Based Solutions for AAL](https://doi.org/10.5281/zenodo.6390709). Section 3.1. Video-based sensing technologies, Section 3.3.1 Main challenges for data processing, Section 3.4. Multimodal data fusion for AAL, Section 4. AAL applications: recent advances in successful assistive and supportive functions (NOTE: do not read sections on the use of audio-based devices).


Optional reading:
> * Climent-Pérez, P., Spinsante, S., Mihailidis, A., & Florez-Revuelta, F. (2020). [A review on video-based active and assisted living technologies for automated lifelogging](https://doi.org/10.1016/j.eswa.2019.112847). Expert Systems with Applications, 139, 112847.

## Concerns on the use of cameras for AAL

Cameras can make AAL systems more capable, but they can also reduce acceptance. Many people see cameras as more intrusive than other sensors because they can capture identity, behaviour, and the presence of other people in the home. Concerns are not only technical. They are also psychological, social, and legal. If you ignore them, systems may fail in real deployments even if the models perform well in the lab.

### Privacy, dignity, and psychological comfort
- **Perceived surveillance** can change behaviour and reduce comfort at home.
- **Bystanders** (family, visitors, care workers) may be recorded without meaningful consent.
- **Sensitive spaces and moments** (bedrooms, bathrooms, intimate care) raise dignity concerns.
- Even when systems do not store raw video, people may still worry about *who can see what* and *when*.

### Data governance and security
Video data can be highly identifying. This raises issues around:
- what data are collected (and whether the system can meet its goal with less data)
- how long data are stored and where (edge device vs cloud)
- who has access, and how access is audited
- cybersecurity risks, including unauthorised access and device compromise

### Ethical concerns
Camera-based AAL raises common healthcare ethics questions:
- **beneficence**: does it provide clear benefit?
- **non-maleficence**: could it cause harm (false alarms, stigma, loss of autonomy)?
- **respect for autonomy**: can the user understand, choose, and control the system?
- **confidentiality**: can the system protect sensitive information throughout its lifecycle?

Ethical design must also consider fairness and inclusion. Some groups may face higher risks of exclusion due to cost, digital literacy, housing conditions, or cultural preferences.

### Legal and regulatory constraints
AAL systems must comply with multiple frameworks, often at the same time:
- **data protection and privacy** (for example, GDPR)
- **cybersecurity and product safety**
- **medical regulation** when a system claims medical purpose or influences clinical decisions (for example, the Medical Device Regulation)
- **AI governance** for high-risk uses (for example, requirements introduced by the AI Act)

These frameworks are demanding in camera-based systems because video can be sensitive, continuous, and hard to fully anonymise.

### Social impact and acceptance
Finally, camera-based AAL can affect relationships and power dynamics:
- it may shift control towards carers, providers, or organisations
- it can increase feelings of being monitored or managed
- it may worsen inequalities if only some households can access safe, well-supported systems

For camera-based AAL to work in practice, design must treat privacy, autonomy, and trust as core requirements, not as add-ons.

Mandatory reading: 
> * Ravi, S., Climent-Pérez, P., & Florez-Revuelta, F. (2024). [A review on visual privacy preservation techniques for active and assisted living](https://link.springer.com/article/10.1007/s11042-023-15775-2). Multimedia Tools and Applications, 83(5), 14715-14755. (except Section 6. Performance evaluation)

## Additional resources
You can, optionally, access [this presentation](https://unialicante-my.sharepoint.com/:b:/g/personal/francisco_florez_mscloud_ua_es/EV6lRC852G9MjgbBQhShivoBn33XyH_xREwvXbj2u2s65g?e=nztneB) on computer vision for active assisted living. It includes videos on different applications of computer vision for active assisted living.

## Moodle test

* The moodle test will be developed during practice sessions on **Friday 27 March at 4.05pm CET**.
* The test has a maximum duration of 30 minutes from the start.
* The test consists of 20 triple choice questions.
* Each wrong answer subtracts 1/3 of the value of a correct answer.
* The mark for the test will be considered as one of the marks for the theoretical part of the course. See the overall evaluation of the course in the general conditions.
* The questions will be based on this webpage and all the mandatory readings proposed. The test will also include questions about the module on the Internet of Things.


