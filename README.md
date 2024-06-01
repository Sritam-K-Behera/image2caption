# Image Captioning Web Application

This project is an image captioning web application built using Streamlit, TensorFlow, and Keras. It generates captions for images either uploaded by the user or provided via a URL. The application leverages a pre-trained image captioning model to generate multiple captions for a given image, offering a variety of descriptive options.

## Table of Contents
- [Demo](#demo)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Model](#model)
- [Project Structure](#project-structure)
- [Acknowledgements](#acknowledgements)

## Demo
You can interact with the application through the following interface:
1. Enter an image URL or upload an image file.
2. View the image and the generated captions.

## Features
- **URL Input**: Users can provide a URL to an image to generate captions.
- **File Upload**: Users can upload an image file (jpg, png, jpeg) to generate captions.
- **Multiple Captions**: The application generates multiple captions for a single image, providing diverse descriptions.
- **On-the-Fly Processing**: The captions are generated dynamically as images are uploaded or URLs are provided.

## Installation
To run this application locally, follow these steps:

1. **Clone the repository**:
    ```sh
    git clone https://github.com/your-username/image-captioning-webapp.git
    cd image-captioning-webapp
    ```

2. **Set up a virtual environment**:
    ```sh
    python -m venv venv
    source venv/bin/activate   # On Windows: venv\Scripts\activate
    ```

3. **Install the required dependencies**:
    ```sh
    pip install -r requirements.txt
    ```

4. **Download the model weights and vocabulary files**:
    - Download the saved models from [here](https://huggingface.co/spaces/Sritam-K-Behera/image2caption/tree/main/saved_models) and place them in the `saved_models` folder.
    - Download the vocabulary files from [here](https://huggingface.co/spaces/Sritam-K-Behera/image2caption/tree/main/saved_vocabulary) and place them in the `saved_vocabulary` folder.

5. **Run the Streamlit application**:
    ```sh
    streamlit run app.py
    ```

## Usage
1. Open the application in your web browser. By default, it runs at `http://localhost:8501`.
2. Enter an image URL in the provided text input box or upload an image file using the file uploader.
3. Wait for the image to be processed and captions to be generated.
4. View the generated captions below the image.

## Model
The image captioning model is based on a combination of CNN and Transformer architectures:
- **CNN Encoder**: Uses InceptionV3 pre-trained on ImageNet to extract features from images.
- **Transformer Encoder and Decoder**: Custom layers implemented to process the image features and generate captions.

### Components:
- **CNN Encoder**: Extracts features from the image.
- **Transformer Encoder**: Processes the image features.
- **Transformer Decoder**: Generates the caption from the processed features.

### Model Loading
The model weights are loaded from a pre-saved file. Ensure the weights file is placed in the correct directory as specified in the installation section.

## Project Structure
- `app.py`: Main application file containing the Streamlit code.
- `model.py`: Contains the model architecture and helper functions.
- `requirements.txt`: List of required Python packages.
- `saved_models/`: Directory to store model weights.
- `saved_vocabulary/`: Directory to store the vocabulary file.

## Acknowledgements
- **Streamlit**: For providing an easy-to-use interface for deploying machine learning applications.
- **TensorFlow and Keras**: For providing the deep learning frameworks.
- **COCO Dataset**: Used for training the image captioning model.

This project is inspired by various open-source image captioning implementations and aims to provide an easy-to-use web interface for generating image captions.
