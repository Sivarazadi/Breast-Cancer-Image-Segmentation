# Breast-Cancer-Image-Segmentation
 
In this project, I aimed to use image segmentation techniques to detect the location of cancer in ultrasound images using the [Ultrasound Breast Images for Breast Cancer](https://www.kaggle.com/datasets/vuppalaadithyasairam/ultrasound-breast-images-for-breast-cancer) dataset from Kaggle. Image segmentation involves dividing an image into distinct regions or segments, which can be used to identify and classify different objects or backgrounds within the image. In the context of cancer ultrasounds, image segmentation can differentiate between different types of tissue, such as normal tissue and tumors. This information can be valuable in the diagnosis and treatment of cancer.

To begin, I preprocessed the ultrasound images and corresponding masks. This included loading the images and masks, resizing them to a consistent size, converting them to the RGB color space (if necessary), and normalizing the pixel values. Preprocessing the data ensured that it was in a suitable format and scale for training a machine learning model.

After preprocessing the data, I combined the images and masks and shuffled them. I then split the data into training, validation, and test sets. I used the training set to fit a machine learning model using TensorFlow and Keras. The model was trained using a supervised learning approach, with the ultrasound images as the input and the masks as the corresponding output.

Once the model was trained and evaluated on the validation set, I tested it on the test set to assess its generalization ability. The input is an ultrasound image of cancer tissue, and the true mask is the ground truth annotation of where the cancer is located in the image. The model mask is the output of the image segmentation algorithm, which shows the predicted location of cancer in the image.

![true mask](https://github.com/Sivarazadi/Breast-Cancer-Image-Segmentation/blob/main/images/true_mask_0.png)
![model mask](https://github.com/Sivarazadi/Breast-Cancer-Image-Segmentation/blob/main/images/model_mask_0.png)

In this example, the model mask is able to accurately detect the location of cancer in the image, as indicated by the overlap between the true mask and the model mask. Overall, the project received a validation accuracy of ~95%, a Mean IoU on the test set of 0.735, and an F1 score on the test set of 0.793. These results indicate that the image segmentation algorithm was able to accurately detect the location of cancer in the ultrasound images and that it has the potential to be a useful tool in cancer diagnosis and treatment.

The goal of this project was to develop an image segmentation algorithm that could accurately detect where cancer is located in ultrasound images. By doing so, I hoped to improve the accuracy of cancer diagnosis and treatment. Image segmentation is a valuable tool for analyzing medical images, and this project aimed to demonstrate its potential for improving patient outcomes.
