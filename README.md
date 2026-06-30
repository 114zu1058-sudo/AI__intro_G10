# ici_template [This section can be removed in the submission version]
This GitHub repository offers a template specifically designed to teach students how to write effective README.md files and create a well-organized file structure. The template provides clear instructions and examples, helping students to learn the basics of GitHub and how to create professional-looking repositories.


# Project Title

[Enter the title of your project]

## Project Description
### Background
In the era of social media, people frequently share captivating photos of their daily lives,
study spaces, or travels. However, social media users often encounter several pain
points when trying to identify the locations in these photos:
+ ### Hidden Locations:
  
Influencers often gatekeep locations, requiring followers to direct message them just to get a place's name.
+ ### Unfamiliar Recommendations:

When seeing a recommendation from a follower they are not personally close with, users may feel awkward asking for the location directly.
+ ### Locating Friends:

Students often wonder where their peers are studying on campus to join them, but tracking down the exact campus building or library can be inefficient

Our survey of 41 samples revealed that 65.9% of people have experienced the desire to know a specific location after seeing a photo shared by others. Among various categories, libraries showed a significantly high frequency of interest, with 63.4% of respondents stating that a search scope limited to National Chengchi University(NCCU)libraries would be highly helpful.
Therefore, to address this practical need, our team decided to kickstart this project by focusing on the campus libraries and learning centers of National Chengchi University as our primary scope and pilot study.

### Importance and Value
Our project, "SEE-SEE-U", addresses these gaps by offering an intuitive, image-based localization assistant. The system provides several key advantages:

+ ### Direct Recognition:

It recognizes specific locations directly from an image without requiring prior textual tags or location metadata.
+ ### Seamless Navigation:

It bridges the gap between image recognition and real-world utility by immediately offering navigation support, making it highly user-
friendly.
+ ### Efficiency:

By automating the workflow, it eliminates the need to manually message others or guess locations, allowing users to discover places and connect with the world effortlessly.

### Dataset Description
Since there was no comprehensively pre-existing, public image dataset specifically for National Chengchi University landmarks, our team built the dataset from scratch through self-collection.
The dataset was gathered through two primary methods to ensure diversity in lighting, angles, and composition:

+ ### Web Scraping:

Collecting publicly available images of NCCU libraries from various social media platforms, search engines, and the official university website.
+ ### Field Photography:

Team members personally visited the campus to take high-quality, real-world photos of the target buildings under different weather conditions and perspectives.

### Dataset Scale and Structure
+ Classes: The dataset targets 8 distinct categories of campus libraries and major learning centers at NCCU.

+ Volume: To ensure an un-biased and balanced dataset, we collected exactly 100
image samples per library category.

+ Total Size: The final dataset comprises a total of 800 labeled images, which
were split into training, validation, and testing sets for our CNN

### Analytical Methods Applied
The system employs a Convolutional Neural Network (CNN) model for core feature extraction and image classification. The workflow consists of image pre-processing, feature extraction via the CNN model, and location mapping. Finally, the highest-probability prediction is converted into a Google Maps search keyword to dynamically generate a one-click navigation link.


## Getting Started

### Prerequisites and Environment
The project is explicitly implemented and optimized to run on the Google Colab
environment, leveraging Google Drive for dataset cloud storage and model serialization.

+ ### Operating Platform:

Google Colab (Linux-based cloud instance).
+ ### Hardware Acceleration:

GPU acceleration is strongly required due to the size of the ResNet50V2 architecture and the two-phase training process.
+ ### Programming Language:

Python 3.9+
+ ### Deep Learning Framework:

TensorFlow 2.x (Keras API)

### Dependencies and Package Installation
The system relies on several computer vision and data processing libraries.
Key Python Libraries Used:

+ 











## File Structure
Below is the directory blueprint of our "SEE-SEE-U" project repository, outlining
the exact organization of our final dataset, model weights, and execution scripts:

 + AI 導論 final pics/ (Dataset Directory)

Contains our self-collected campus image data. It includes exactly 800 image
samples balanced evenly across 8 NCCU library and center categories:

  o NCCU Main Library
  
  o NCCU Dah Hsian Library
  
  o NCCU Social Sciences Library
  
  o NCCU Commerce Library
  
  o NCCU Law Library
  
  o NCCU Research Center and Innovation Incubation Center
  
  o NCCU College of Communication Library
  
  o NCCU Art Culture Center
+ models/ (Model Weights Directory)

Stores our deployment-ready deep learning model weights file named
model.v2.h5. This file contains the optimized mathematical parameters of our
fine-tuned ResNet50V2 network, which utilizes Transfer Learning to leverage
deep feature knowledge from pre-trained image databases.
+ src/ (Core Source Code Directory)

Contains the modular Python pipeline scripts that run our application:

  o data_preprocessing.py: Manages data ingestion pipelines via Keras
ImageDataGenerator with a 0.2 validation split, automatically
reshaping image tensors to 224* 224* 3 and executing target normalization.

  o train_model.py: Constructs the sequential top layers over the frozen
ResNet50V2 base, compiles the architecture using the Adam optimizer
alongside categorical_crossentropy loss, and executes the 10-epoch
training performance loop.

  o app.py: Houses the interactive deployment and predictive inference
engine. It feeds uploaded images into our saved model network,
computes the highest target index score, filters predictions using a strict
classification threshold, and automatically triggers embedded Google
Maps navigation links.

+ requirements.txt (Environment Configuration)

A standard reference file specifying mandatory module dependencies and
library framework versions (TensorFlow, Keras, NumPy, IPython Display, etc.)
required to safely reproduce the project environment.
+ README.md (Repository Documentation)
The main markdown-formatted user manual that displays our comprehensive
project overview, data distributions, training diagnostics, and deployment setup
guidelines.

### File Relationship Summary
Image samples organized within AI 導論 final pics/ are structurally prepared and
preprocessed by src/data_preprocessing.py. These formatted arrays are passed into
src/train_model.py to train the top classification layers attached to the ResNet50V2
Transfer Learning core. Once the training cycle successfully concludes, the resulting
optimal neural weights are saved into models/model.v2.h5.
Finally, our live deployment framework loads this file. When a user submits a
campus photo, the system evaluates the top classification probability. If this score
meets or exceeds our 0.75 confidence threshold, it displays the confirmed location
and provides a clickable Google Maps navigation hyperlink. If the prediction score
falls below 0.75, it flags the sample as unidentifiable and prompts the user to upload
another photo.

## Analysis

[Describe your analysis methods and include any visualizations or graphics that you used to present your findings. Explain the insights that you gained from your analysis and how they relate to your research question or problem statement.]

## Results

[Provide a summary of your findings and conclusions, including any recommendations or implications for future research. Be sure to explain how your results address your research question or problem statement.]

## Contributors
114zu1001 王紫君

114zu1009 黎芯妤

114zu1015 汪宜家

114zu1025 趙芯悅

114zu1058 楊恆慈
## Acknowledgments

[Thank any individuals or organizations who provided support or assistance during your project, including funding sources or data providers.]

## References

[List any references or resources that you used during your project, including data sources, analytical methods, and tools.]
