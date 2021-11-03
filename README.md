# Evaluation of biases in remote photoplethysmography methods

This work investigates the estimation biases of remote photoplethysmography (rPPG) methods for pulse rate measurement across diverse demographics. Advances in photoplethysmography (PPG) and rPPG methods have enabled the development of contact and noncontact approaches for continuous monitoring and collection of patient health data. The contagious nature of viruses such as COVID-19 warrants noncontact methods for physiological signal estimation. However, these approaches are subject to estimation biases due to variations in environmental conditions and subject demographics. The performance of contact-based wearable sensors has been evaluated, using off-the-shelf devices across demographics. However, the measurement uncertainty of rPPG methods that estimate pulse rate has not been sufficiently tested across diverse demographic populations or environments. Quantifying the efficacy of rPPG methods in real-world conditions is critical in determining their potential viability as health monitoring solutions. Currently, publicly available face datasets accompanied by physiological measurements are typically captured in controlled laboratory settings, lacking diversity in subject skin tones, age, and cultural artifacts (e.g, bindi worn by Indian women). In this study, we collect pulse rate and facial video data from human subjects in India and Sierra Leone, in order to quantify the uncertainty in noncontact pulse rate estimation methods. The video data are used to estimate pulse rate using state-of-the-art rPPG camera-based methods, and compared against ground truth measurements captured using an FDA-approved contact-based pulse rate measurement device. Our study reveals that rPPG methods exhibit similar biases when compared with a contact-based device across demographic groups and environmental conditions. The mean difference between pulse rates measured by rPPG methods and the ground truth is found to be ~2% (1 beats per minute (b.p.m.)), signifying agreement of rPPG methods with the ground truth. We also find that rPPG methods show pulse rate variability of ~15% (11 b.p.m.), as compared to the ground truth. We investigate factors impacting rPPG methods and discuss solutions aimed at mitigating variance.

# Contribution

In this paper, an evaluation of the biases existing in the measurement of heart rate using rPPG approaches has been performed. In summary, the contributions of the work are:

1) Performs data collection of facial videos of subjects containing demographics typically not represented in existing datasets used to evaluate rPPG methods for pulse rate estimation.

2) Compares and tests the estimation accuracy of state-of-the-art rPPG methods against an FDA-approved ground truth PPG sensor on the collected demographically diverse dataset.

3) Investigates the sources of bias in rPPG approaches for pulse rate estimation, such as country of origin, gender, and skin tone, and quantifies the error due to each identified source.

# Dataset

The 'Data' folder contains the video data of subjects from India and Sierra Leone. As the participants have given permission for their de-indentified video data to be shared publicly, we generated 3 videos from the facial video of each subject. The 3 videos generated for each subject are described below and the corresponding regions (R1: Forehead, R2: Left Cheek, R3: Right Cheek) on the face are shown in the accompanying figure.

1) Rectangular region of 60 x 30 pixels of the forehead 
2) Rectangular region of 25 x 25 pixels of the left cheek (the left of the viewer)
3) Rectangular region of 25 x 25 pixels of the right cheek (the right of the viewer)

The ground truth mean heart rate for each video is provided in the respective '.csv' files contained in the 'Ground_Truth' folder. 

![alt text](https://github.com/AiPEX-Lab/rppg_biases/blob/main/Fig.jpg?raw=true)

# Running the scripts

The results of the heart rate obtained using 5 rPPG approaches - CHROM [[1]](https://iopscience.iop.org/article/10.1088/0967-3334/35/9/1913), BKF [[2]](https://www.osapublishing.org/boe/fulltext.cfm?uri=boe-9-2-873&id=381227), Spherical Mean [[3]](https://ieeexplore.ieee.org/document/9022571), DeepPhys [[4]](https://arxiv.org/abs/1805.07888) and POS [[5]](https://ieeexplore.ieee.org/document/7565547), have been tabulated in the file 'Results_Final_Main.csv'. 
The python script 'HypoTest_Results_p.py' provides hypothesis test results (p-values) obtained for the hypothesis tests detailed in the paper. 
The python script 'blandaltman.py' provides the Bland Altman plots for the results obtained using rPPG approaches, as compared to the results obtained using the ground truth Masimo device 

# Citation
If you use any of the data or resources provided on this page in any of your publications we ask you to cite the following work.

Dasari, A., Prakash, S.K.A., Jeni, L.A. et al. Evaluation of biases in remote photoplethysmography methods. npj Digit. Med. 4, 91 (2021). https://doi.org/10.1038/s41746-021-00462-z
