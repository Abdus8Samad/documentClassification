## Document Classification and Data Extraction

<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#salient-features">Salient Features</a>
    </li>
    <li>
      <a href="#description">Description</a>
    </li>
    <li>
      <a href="#data-preprocessing">Data Preprocessing</a>
    </li>
    <li>
      <a href="#document-classification-model">Document Classification Model</a>
    </li>
    <li>
      <a href="#results">Results</a>
    </li>
    <li>
      <a href="#information-extraction-model">Information Extraction Model</a>
    </li>
    <li>
      <a href="#team">Team</a>
    </li>
  </ol>
</details>

## About The Project
This project presents a model capable of recognizing and classifying multiple documents contained in a PDF or image. The input PDF is divided into individual pages, and each page is classified into the appropriate document category using a CNN model. After classification, OCR (optical character recognition) is used to extract data from each document. The project focuses on five document types: voter identification, driver's license, PAN card, Aadhar card, and single-page gas bill. Each page in the input PDF must contain a single document, except for the front and back of the same document.

### Salient Features
- Hyperparameter tuning
- Regularization (early stopping)
- Document splitting

### Tech Stack Used
- Models: CNN and OCR
- Framework: Keras

### Methodology
![Methodology](https://user-images.githubusercontent.com/87893594/224972918-d1e9f755-02e0-40c0-8725-ac5c4824d49a.png)

## Description
When searching for an appropriate dataset, we found no publicly available dataset of identity documents due to their sensitive nature. However, we discovered a dataset on Kaggle containing six folders: Aadhar Card, PAN Card, Voter ID, single-page Gas Bill, Passport, and Driver's License. We added more images to each folder, including manually scanned documents and images from Google. Thus, we are classifying and extracting information from these four documents.

### Data Preprocessing
Before training the model, we applied horizontal and vertical data augmentation using random flips, increasing the size and diversity of the dataset. The categorical values of the labels column were converted to numerical values using one-hot encoding.

## Document Classification Model
![Classification Model](https://user-images.githubusercontent.com/87893594/224973161-2513f1f7-0291-41ed-9b79-c14ef2578882.png)

Various hyperparameters such as the number of layers, neurons in each layer, number of filters, kernel size, value of p in dropout layers, number of epochs, batch size, etc., were tuned until satisfactory training and validation accuracy were achieved.

![Model Accuracy](https://user-images.githubusercontent.com/87893594/224972235-be7435d0-1f11-4c38-8ab6-6958fcb3bb83.png)
![Model Loss](https://user-images.githubusercontent.com/87893594/224972374-4244b1b6-418d-4364-8fea-77a05450ca19.png)

### Final Model and Results
![Final Model](https://user-images.githubusercontent.com/87893594/224972133-8bf9642b-d16e-4880-b017-161c61d8f247.png)
![Final Model Results](https://user-images.githubusercontent.com/87893594/224972187-cd7f5c48-95d7-42fa-a187-bfd84344e903.png)

## Information Extraction Model
Following are the steps of OCR performed on images:

![OCR Steps](https://user-images.githubusercontent.com/87893594/224973268-06a235f9-6657-4970-befc-78cf665bfb65.png)
![OCR Workflow](https://user-images.githubusercontent.com/87893594/224973311-0b5c26d3-46d4-4df8-96a3-c4287072637a.png)

## Team
- Abdus Samad [GitHub](https://github.com/abdus8samad) | [LinkedIn](https://www.linkedin.com/in/abdus-8-samad/) 
- Samad Ahmed [GitHub](https://github.com/) | [LinkedIn](https://www.linkedin.com/in/samad-ahmed-6020871aa/)