# OCR_for_Bank_Statement
This project aims to create an Optical Character Recognition for Bank Statements and explored the approach to upscale the low resolution images. Besides, this project also trained an SVM model for Bank Statement Classification with 100% accuracy.  

<details>
  <summary><B>Table of Content</B></summary>
  
  1. Overview
  2. [Pre-requisite](#Pre-requisite)
  3. [Install Tesseract](#InstallTesseract)
  4. [OCR for Bank Statements](#OCRforBankStatements)
     * Import Libraries
     * EDA
     * Model Architecture
     * Model Performance
  5. Bank Statement Classfication Model
     * Import Libraries
     * EDA
     * Model Architecture
     * Model Performance
  6. References

</details>

# Overview  
OCR is short for Optical Character Recognition, which is a technique that detects text in images and scanned documents (Ariga, 2017). Python OCR allows us to extract text from PDFs or images using Python (Ariga, 2017).   

<b>The goals of this project are: </B>

1. to build up an OCR for bank statements which could extract the text and numbers from different format of bank statements even those images which have low resolution. 

2. Also, another part of this project is to train a model to classify the type of the bank statement based on the text extracted from the bank statement using OCR.

From research, I found different approaches of OCR to handle different input files: 
![image](https://github.com/ScarlettQiu/OCR_for_Bank_Statement/assets/93269907/78374404-cb93-428a-a4e3-97648462e0e7)

Since PDF files usually have a high resoluion, so it is easy to directly use tabula-py or PyTesseract (need to convert PDF to images using PyPDF2 first) to extract content from PDF files. <b> Therefore, this project mainly explored the OCR approach when the input files are images.  </B>

<b> Dataset </b>
There are 2 dataset folders in this repository. The folder <b> Dataset </b> contains 15 images for training the bank statement classfication model. The folder <b> Dataset2 </b> contains 3 images for testing the performance of OCR. 2 of the images have relatively low resolution. 

# Pre-requisite  
## Homebrew for Mac  

### What is Homebrew?   
Here is link to understand homebrew: https://brew.sh/ 

### Why do we need Homebrew?  
To install the popular package Tesseract, we need Homebrew on Mac.  

About Tesseract: https://github.com/tesseract-ocr/tesseract

### Install Homebrew
#### 1. Paste below command in macOS Terminal  
<code> /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)" </code>

![image](https://user-images.githubusercontent.com/93269907/232903664-eb341c8c-68fb-4289-a5df-6e540d939d39.png)

#### 2. Run below command in the Terminal  
<code> eval "$(/opt/homebrew/bin/brew shellenv)" </code>

![image](https://user-images.githubusercontent.com/93269907/232903939-ca466b60-a4d2-459b-b327-0b42845364f5.png)

Once we have the homebrew installed, we could start to install Terresact.  

# Install Tesseract  
#### 1. Run below the command
<code> brew install tesseract </code>  
It may take several minutes to complete the installation.   
![image](https://user-images.githubusercontent.com/93269907/232904805-e74328b7-c444-43d5-bf8d-a7a5d719bdae.png)

### 2. Check the path of Tesseract
<code> which tesseract </code>  
<code> brew list tesseract </code>

# OCR for Bank Statements
In this part, I mainly tried 2 different model achitrecures and compared their performance. 

![image](https://github.com/ScarlettQiu/OCR_for_Bank_Statement/assets/93269907/186440fc-49fc-4934-9a08-98959ec36f97)

![image](https://github.com/ScarlettQiu/OCR_for_Bank_Statement/assets/93269907/d032df54-8318-49e9-a3e1-a1b391b878f3)



