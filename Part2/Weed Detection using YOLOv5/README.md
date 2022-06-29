
## Weed Detection using Yolov5
Our aim for this final year project is to focus on the health of tomato plants and for that , next step is to be able to detect and classify commonly found weeds around tomatoes. Thus to make this work we have used the help of pre-trained model YOLOv5 which gave us an accuracy of almost 98%

## Index

- Workflow
- Tips
- Tech Stack
- Deployement
- Acknowledgement
- Model Preview and Test Results
- My Trained Model

## WorkFlow

- Collect the data
- Split the dataset into training set ,test set and validation set.
- Label the data using makesense.ai
- Download the YOLOv5 Tutorial Google colab notebook from Github
- Clone the repository and import the necessary dependancies
- In the YOLOv5 folder edit the coco128.yaml file according to your dataset.
- Train the model
- Evaluate the model.
- Make Predictions.
## Tips

While working on this project I solved a few errors which might be helpful to others.

-  CUDA/GPU out of memory. Run this python code at the start ( Thanks to [@NicholasRenotte](https://www.youtube.com/c/NicholasRenotte)):

        gpus = tf.config.experimental.list_physical_devices('GPU')
        for gpu in gpus:
            tf.config.experimental.set_memory_growth(gpu, True)

- The code in the tutorial notebook for training the model needs a slight change; instead of just python it should be python3

        !python3 train.py --img 640 --batch 12 --epochs 50 --data coco128.yaml --weights yolov5s.pt --cache
        
- Increasing the quality of dataset: The dataset I gathered of some weeds were of really low quality and upscaling resolution of images online has limitations , thus with the help of ESRGAN (Enhanced SRGAN) I upscaled my images pretty quick thanks to [@Xintao](https://github.com/xinntao/ESRGAN)

**Before:**

![](https://github.com/TejasARathod/Final-Year-Project-AgriDoc-Agricultural-Robot-/blob/2c8d5e4abc9ea78e5de76fc5d089bcad1176305c/Part2/Weed%20Detection%20using%20YOLOv5/Before.png)
![](https://github.com/TejasARathod/Final-Year-Project-AgriDoc-Agricultural-Robot-/blob/2c8d5e4abc9ea78e5de76fc5d089bcad1176305c/Part2/Weed%20Detection%20using%20YOLOv5/BeforeSpec.png)

**After:**

![](https://github.com/TejasARathod/Final-Year-Project-AgriDoc-Agricultural-Robot-/blob/2c8d5e4abc9ea78e5de76fc5d089bcad1176305c/Part2/Weed%20Detection%20using%20YOLOv5/After.png)
![](https://github.com/TejasARathod/Final-Year-Project-AgriDoc-Agricultural-Robot-/blob/2c8d5e4abc9ea78e5de76fc5d089bcad1176305c/Part2/Weed%20Detection%20using%20YOLOv5/Afterspecs.png)
## Tech Stack

**Language Used:** Python

**IDE Used:** Jupyter Notebook 


## Deployement

To deploy this project simply follow the workflow and upload the jupyter notebook and run it.


 


## Special thanks to

 - [DeepLearning](https://www.youtube.com/c/DeepLearning004)
 - [makesense.ai](https://www.makesense.ai/)
 
 
 


## Model Preview and Test Results

**F1_curve:**

![](https://github.com/TejasARathod/Final-Year-Project-AgriDoc-Agricultural-Robot-/blob/907ac92004d505bde0f043d31fac4b7bd24679f9/Part2/Weed%20Detection%20using%20YOLOv5/F1_curve.png)

**PR_curve:**

![](https://github.com/TejasARathod/Final-Year-Project-AgriDoc-Agricultural-Robot-/blob/907ac92004d505bde0f043d31fac4b7bd24679f9/Part2/Weed%20Detection%20using%20YOLOv5/PR_curve.png)

**P_curve:**

![](https://github.com/TejasARathod/Final-Year-Project-AgriDoc-Agricultural-Robot-/blob/907ac92004d505bde0f043d31fac4b7bd24679f9/Part2/Weed%20Detection%20using%20YOLOv5/P_curve.png)

**Results:**

![](https://github.com/TejasARathod/Final-Year-Project-AgriDoc-Agricultural-Robot-/blob/907ac92004d505bde0f043d31fac4b7bd24679f9/Part2/Weed%20Detection%20using%20YOLOv5/results.png)

**Test Video**

[Click Here](https://drive.google.com/drive/folders/1iW7k3t1qQMEH-mBi6c9kgKB_pkKFhdwl?usp=sharing)




## My Trained Model

[You can access my trained model and other required materials over here](https://drive.google.com/drive/folders/1NtygCHO1TaXevhHUtaWwWscG-Hzif6rE?usp=sharing)
