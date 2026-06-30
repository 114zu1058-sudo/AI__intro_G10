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

[Describe the file structure of your project, including how the files are organized and what each file contains. Be sure to explain the purpose of each file and how they are related to one another.]

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
