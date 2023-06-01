# OCR_for_Bank_Statement
This project aims to create an Optical Character Recognition for Bank Statements and explored the approach to upscale the low resolution images. Besides, this project also trained an SVM model for Bank Statement Classification with 100% accuracy.  

<details>
  <summary><B>Table of Content</B></summary>
  
  1. Overview
  2. [Pre-requisite](#Pre-requisite)
  3. [Tesseract](#Install Tesseract)
  4. [OCR for Bank Statements](#OCR for Bank Statements)
     * Import Libraries
     * EDA
     * Model Architecture
     * Model Performance
  5. Bank Statement Classfication Model
     * Import Libraries
     * Model Architecture
     * Model Performance
  6. References

</details>

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

# Install Terresact  
#### 1. Run below the command
<code> brew install tesseract </code>  
It may take several minutes to complete the installation.   
![image](https://user-images.githubusercontent.com/93269907/232904805-e74328b7-c444-43d5-bf8d-a7a5d719bdae.png)

### 2. Check the path of Tesseract
<code> which tesseract </code>  
<code> brew list tesseract </code>

# OCR for Bank Statements
In this part, I mainly tried 2 different model achitrecures and compared their performance. 

![image](https://github.com/ScarlettQiu/OCR_for_Bank_Statement/assets/93269907/f1103296-3797-48b5-85eb-b6a29df3bec6)
