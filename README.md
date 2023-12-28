# Passive-WiFi-Sensing-Based-Fine-Grained-Crowd-Analysis-Dataset
This repository includes three semi-synthetic and one real-world passive WiFi sensing-based datasets for fine-grained crowd analysis. 

The fine-grained crowd analysis aims to estimate the density of the whole crowd in a scene and the speeds of local high-density crowds through a certain measuring approache, and particularly, the passive WiFi sensing is utilized [1]. The basic idea is employing  WiFi sniffers to passively sense nearby pedestrians via capturing probe frames sent by their mobile devices, and then inferring the crowd states from the WiFi measurements in combination with deep learning model(s).

However, there is still a lack of annotated datasets for above tasks. Here we provide three semi-synthetic datasets (WiDIA, WiATC, and WiDATC) which are constucted by emulating passive WiFi sensing on precisely labelled pedestrian tracking datasets and a self-collecting real-world dataset (WiCAM) in a campus environment. In addition, the WiCAM can also support simple crowd counting task [2].

# Semi-Synthetic Datasets
To synthesize these datasets, two pedestrian tracking datasets (https://dil.atr.jp/sets/groups/), i.e. DIAMOR [3] and ATC [4], are taken as backbone datasets. Then, a divide-and-conquer approach is employed to emulate corresponding passive WiFi sensing data with the real data of each pedestrian. These datasets are in .mat (MATLAB data) format and can be utilized for generating crowd density map (CDM) or WiFi-sensed crowd density map (WDM). The details and links of each dataset are provided in the following.

-the files with suffixs of "corrected" are the pedestrian tracking data corrected by the linear interpolation (for one second per pedestrian), which are mainly utilized for generating CDMs and includ items of timestamp, pedestrian ID, position_x (m), position_y (m), position_z (m), velocity (m/s), motion_direction (rad), facing_direction (rad).
-the files with suffixs of "wifi" are the corresponding emulated WiFi sensing data and are mainly utilized for generating WDMs, which include cells per second composing of emulated locations of all randomly detected devices.

WiDIA: https://1drv.ms/f/c/edbf3ffa172dc60c/EvvsDqsfo3RNmzHrQTB4JqgBn9RSydex6rrxPBPsTw2XXg?e=buL7Tr
WiATC: https://1drv.ms/f/c/edbf3ffa172dc60c/Er6u7XKbfoJOuvWvOPCBJ00BqH2QpkbjFl1ECDJ7yNaeWg?e=31Gssw
WiDATC: https://1drv.ms/f/c/edbf3ffa172dc60c/Etv9qj2HzeBEnboUwQOegrEBCczxVYCN99aWEBR-kslyOA?e=id4eBs

# Real-World Dataset

second composing of emulated locations of all randomly detected devices estimated by WiFi fingerprint-based localizaiton.
https://1drv.ms/f/c/edbf3ffa172dc60c/EqeGb6NVgItDlKBX6SvtnqQBOU7uUfCHV9V7Go3KcBoc4Q?e=OhGgnZ

# References
[1] L. Hao, B. Huang, B. Jia and G. Mao, "On the Fine-Grained Crowd Analysis Via Passive WiFi Sensing," in IEEE Transactions on Mobile Computing, doi: 10.1109/TMC.2023.3324334.

[2] L. Hao, B. Huang, B. Jia, G. Xu and G. Mao, "Toward Accurate Crowd Counting in Large Surveillance Areas Based on Passive WiFi Sensing," in IEEE Transactions on Intelligent Transportation Systems, vol. 24, no. 12, pp. 14086-14096, Dec. 2023, doi: 10.1109/TITS.2023.3303700.

[3] F. Zanlungo, T. Ikeda, and T. Kanda, "Potential for the dynamics of pedestrians in a socially interacting group," Physical Review E, Vol. 89, No. 1, 012811, 2014.

[4] F. Zanlungo, D. Brscic, and T. Kanda, "Pedestrian group spatial size scaling under growing density conditions," Physical review E, Vol. 91, No. 6, 062810, 2015.
