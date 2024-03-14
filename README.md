# Dynamic Detection and Segmentation with YOLOv9+SAM

This repository is dedicated to the advanced object detection and segmentation task using YOLOv9 combined with the Spatial Attention Module (SAM). Leveraging the cutting-edge capabilities of YOLOv9 for detection and SAM for segmentation, this project aims to achieve precise delineation of objects within various images. The integration of YOLOv9 and SAM sets a new standard for accuracy and detail in object detection and segmentation tasks, making it an ideal solution for applications requiring high-level visual understanding.

## Dataset

The images used in these notebooks are obtained from RF100 construction-safety-2 dataset from Roboflow, a platform that simplifies dataset management, preprocessing, and augmentation. You can access the dataset used in this project from [Roboflow](https://roboflow.com/).

![](/images/image12.jpeg)


## Getting Started

- To get started with this project, clone the repository to your local machine or directly to your preferred development environment: git clone https://github.com/suniash/DynamicDetect_YOLOv9_SAM.git

- Run the Jupyter Notebook to train the model

## Implementation

This project is implemented in Python, utilizing the PyTorch framework for model training and inference. The YOLOv9 and SAM models are intricately configured to work in tandem, providing seamless object detection followed by precise segmentation.

### Workflow

The project workflow involves several key steps:

- Detection with YOLOv9: Initially, objects within images are detected using YOLOv9, providing accurate bounding box coordinates for each object.

- Segmentation with SAM: For every detected object, SAM performs instance segmentation within the specified bounding boxes, enhancing the output with detailed masks.

- Visualization: The final output merges the initial detections with the segmented masks, producing images that offer a visual understanding of both the location and the shape of each object.

While bounding boxes provide positional information about objects, they lack the fine details required for more advanced computer vision tasks like instance segmentation or background removal.

Converting bounding boxes to segmentation masks allows us to extract accurate object boundaries and separate them from the background, opening up new opportunities for analysis and manipulation.

### Model Architecture

YOLOv9: Serves as the backbone for object detection, efficiently identifying and localizing objects within the image. YOLOv9 is a powerful computer vision model for object detection, developed by Chien-Yao Wang, I-Hau Yeh, and Hong-Yuan Mark Liao. It introduces the YOLOv9 and GELAN architectures.

Segment Anything Model (SAM): Enhances segmentation accuracy by focusing on spatially relevant features, improving the delineation of detected objects. Segment Anything (SAM) is an image segmentation model developed by Meta AI. This model can identify the precise location of either specific objects in an image or every object in an image.

## Results

The combination of YOLOv9's detection capabilities with SAM's segmentation prowess results in highly detailed images where each object is not only detected but also meticulously segmented. This approach enhances the utility of computer vision in applications requiring nuanced understanding of scene composition, from autonomous driving to medical imaging analysis.

![YOLOv9_detections](/yolov9_results/download.jpeg)

![YOLOv9+SAM_detections](/yolov9+sam_results/results_1.png)

## Contribution

Contributions to this project are welcome. Please feel free to fork the repository, make your changes, and submit a pull request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

The YOLOv9 (Ultralytics) and SAM (META) teams for their exceptional work in advancing the field of object detection and segmentation.
Contributors to the datasets used, enabling the demonstration of this project's capabilities.
