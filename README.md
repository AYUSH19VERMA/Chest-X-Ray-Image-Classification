# Chest-X-Ray-Image-Classification
## Approach
This analysis uses a detailed state-of-the-art dataset collected from Wang et al. (2019). A total of 112,120 frontal-view chest X-rays (CXRs) images collected from 30,805 unique patients are included in the dataset. All the images were labeled with one of the 14 pathological diseases and classified as “No Findings” for those with no disease. The Hernia class eventually withdrew from the label, leaving 13 main classes because the images were smaller than the others. Some examples and their corresponding annotations in Chest X-ray14 (Wang et al., 2019).

Overall, our approach produces labels using the reports in two passes. In the first iteration, we detected all the dis- ease concept in the corpus. The main body of each chest X-ray report is generally structured as “Comparison”, “Indication”, “Findings”, and “Impression” sections. Here, we focus on detecting disease concepts in the Findings and Impression sections. If a report contains neither of these two sections, the full-length report will then be considered. In the second pass, we code the reports as “Normal” if they do not contain any diseases (not limited to 8 predefined pathologies).

One of the significant problems faced with this research is that the classes’ images are not enough for proper training of our models; hence, to get effective results with high accuracy, we generalized the data by considering data augmentation. Image augmentation provides training images by alternate processing or assembly methods of many systems, such as random rotation, turns, shear, flips, zooming, etc.



## Results
In the analysis of this data, the number of labels for each disease was analysed. It was found that Infiltration had the highest number of labels (nearly 20,000) with the rest of the disease having very few labels in the entire image dataset of 112,120 images. About 60,361 images had labels of “No Finding” indicating a large irregularity in the dataset with respect to the disease labelling. Also there is no data regarding the presence of healthy patients in the data and whether these “No Findings” correspond to them or not. Thus, the overall authenticity of the dataset with respect to labelling for different types of diseases can’t be verified.
![image](https://github.com/AYUSH19VERMA/Chest-X-Ray-Image-Classification/assets/75496202/3576d549-da9e-4ca1-b5ab-2033593e93ee)

Further looking at the image dimensions in Fig. 6, the mean of image width was observed to be 2646 mm and image height was observed to be 2486 mm. The distribution of the image width and image height was observed to be in a distribution of less than 20% around the mean, thus indicating a reasonable dataset which can be used without much pre-processing. 
![image](https://github.com/AYUSH19VERMA/Chest-X-Ray-Image-Classification/assets/75496202/2668bcbd-da90-4a18-a42b-83df4633e27c)

The dataset segmentation by gender shows nearly 63340 male data and 48780 female data in the images as shown in Fig.7 a, implying a proportionate collection of data from both the genders. Also, the dataset segmentation by view shows 67310 images in the Posterior-anterior view and 44810 images in the anterior-posterior views as shown.

![image](https://github.com/AYUSH19VERMA/Chest-X-Ray-Image-Classification/assets/75496202/02d92e12-95d2-46ce-980f-4ea1dc13ec64)
![image](https://github.com/AYUSH19VERMA/Chest-X-Ray-Image-Classification/assets/75496202/ccb851cb-7890-45e9-a1c7-496e90c7e26f)



