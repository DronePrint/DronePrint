# AcousticPrint


## Team
* [Harini Kolamunna](https://dblp.org/pers/k/Kolamunna:Harini.html) 
* Thilini Dahanayake, 
* Junye Li, 
* [Suranga Seneviratne](https://www.sydney.edu.au/engineering/about/our-people/academic-staff/suranga-seneviratne.html)
* [Kanchana Thilakaratne](https://www.sydney.edu.au/engineering/about/our-people/academic-staff/kanchana-thilakarathna.html)
* [Albert Y. Zomaya](https://www.sydney.edu.au/engineering/about/our-people/academic-staff/albert-zomaya.html) 
* [Aruna Seneviratne](https://www.engineering.unsw.edu.au/electrical-engineering/professor-aruna-seneviratne) 


## Media
https://www.youtube.com/watch?v=s9kNu…


## Introduction
*DronePrint* generates signature acoustic profiles for different classes of drones by using machine learning technologies that is capable of identify an incomming acoustic signal is from a drone or not, and identify the drone make and model. The overview of the system architecture is shown below.
![DronePrint System](/Images/System.png)


## Dataset
The dataset we used in this project is available with the following headings. The experimental data collection setup is as shown below.
![Experimental Data collection](/Images/Experiments.png)


1. DS1:
   1. Experimentally-Captured:
      * Drone acoustic profiles collected experimentally with a RODE NTG4 shotgun directional microphone for five different classes of drones, rangingfrom amateur to professional drones, **Parrot: Bebop 2**, **DJI: MavicPro**, **DJI: Phantom 4 Pro**, **DJI: Spark**, **DJI: Matrice 100**; 
      * Drones are flying around at 20m above ground and within a 50m radius;
      * Signals are sampled at 44.1kHz;
      * *Test* - 50s; captured on 3 different sessions over 2 days.
   1. YouTube-Sourced: 
      * Drone acoustic profiles scraped from YouTube videos.
      * Traces for **Parrot: Bebop 2**, **DJI: MavicPro**, **DJI: Phantom 4 Pro**, **DJI: Spark**, **DJI: Matrice 100**, **Autel: EVO**, **DJI: Inspire2**, **DJI: MavicAir**, **Feima Robotics: J.ME**, and **Parrot: Anafi**. 
      * *Training* - 150s; *Validation* - 50s; *Test* - 50s; scraped from multiple YouTube videos.
   1. Other-Online-Databases-Sourced: 
      * Drone acoustic profiles scraped from different online databases.
      * Traces for **Parrot: Bebop**, **Parrot: Membo**, and **MikroKopter: MK-Quadro**
      * *Training* - 150s; *Validation* - 50s; *Test* - 50s; 
1. DS2: 
    * Non-Drone acoustic profiles collected experimentally and scraped from YouTube videos.
    * Scraped from YouTube videos - **Busy Road Noise**, **Airplane Sounds**, **Hair Dryer**, **Rain**, **Bird Sounds**, and **Human Speech**.
    * Experimentally collected - **Calm Environment** 
    * *Training* - 270s; *Validation* - 90s; *Test* - 90s; scraped from 5 different YouTube videos/ captured on 5 different sessions.
1. DS3: 
    * Online downloaded acoustic signals (from https://www.soundsnap.com/) that consist of various mechanical sound; 7 unknown drone sounds (**AIrHogs: DR1FPV Race**, **Blade: NanoQX**, **ZeroZero: Falcon**, **DJI: Inspire1**, **DJI: MavicMini**, **DJI: Phantom3**, **Syma: X5SW**); 
    * Scraped from YouTube videos - 5 non-drone mechanical sounds (**Helicopter**, **Motorcycle**, **Lawn Mover**, **Air Blower**, and **Car**); and 2 natural background noise (**Slight Breeze** and **Bees Humming**) that were not used in training.
    * *Test* - 30s; 
    


* *Training* and *Validation* samples are augmented with frequency warping techniques. Each sample is scaled 21 times along in the time axis and in amplitude by  values ranging from 0.8 to 1.2 with 0.02 steps.
* The usage of the datasets in DronePrint is shown below.
![Usage of the Datasets](/Images/Dataset.png)
