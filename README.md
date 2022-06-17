# Third Year Dissertation Project

This repository contains my third year dissertation. My dissertation focused in evaluating and creating a DNN for a Network Intrusion Detection System (NIDS).

The goal is the creation of a lightweight NIDS that have results comparable to those of published methods. The code can be found in [here](/DNN_NIDS_FYP_2021/Code/Dissertation_Code.ipynb).

The paper presented for my final year project can be found [here]().

# Abstract

Intrusion Detection Systems (IDS) are crucial in detecting possible attacks on a network and informing the administrator about the attack and the attack type. IDS are distinguished into Host-based IDS (HIDS), that check for attacks inside a computer, and Network-based IDS (NIDS), that check for attacks in a network. Additionally, IDS can be Anomaly-based IDS, which utilizes different Machine Learning and Deep Learning techniques to learn attack patterns and Rule-based IDS which utilizes rules that are derived from historical data to detect attacks. Anomaly-based IDS can detect zero-day attacks. As such, there is the need to create a Deep Neural Network (DNN) that can learn to detect and categorize the attacks in order to be used in Anomaly-based IDS. The aim of this paper is to create a DNN that can detect and categorize the attacks that are found in the CIC-IDS-2017 dataset while being as accurate and lightweight as possible. The DNN architectures created will be evaluated from different metrics to gain a better understanding of which architecture performs the best. Pre-processing of the dataset to extract the best performance will be researched to help create an IDS that can perform better with less computational overhead. The experimental data derived by the selected architecture shows a model that performs exceptionally well for the number of attack types it has to detect compared to other published works. Yet, published work tends to perform better as different attack categorization is used. Attacks are bundled to their categories and/or more complex architectures are employed, that is not as lightweight as the proposed one.

