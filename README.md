# CropDamageClf

**CropDamageClf** is a machine learning model designed to classify crop damage using images. This project is part of the "Eyes on the Ground" initiative, a collaboration between ACRE Africa, the Kenya Agricultural & Livestock Research Organization (KALRO), the International Food Policy Research Institute (IFPRI), and the Lacuna Fund, aimed at developing a Picture Based Insurance framework for smallholder farmers.

## Table of Contents

1. [Overview](#overview)
2. [Features](#features)
3. [Dataset](#dataset)
4. [Methodology](#methodology)
5. [Installation](#installation)
6. [Usage](#usage)
7. [Evaluation](#evaluation)
8. [Compute Restrictions](#compute-restrictions)
9. [Technologies Used](#technologies-used)
10. [Contributing](#contributing)
11. [License](#license)
12. [Contact](#contact)
13. [Acknowledgments](#acknowledgments)

## Overview

The **CropDamageClf** project aims to help farmers across Africa manage agricultural risk by using image data to settle insurance claims and carry out loss assessment. ACRE Africa reviews smartphone pictures of insured crops sent by farmers to verify crop damage and provide agricultural advisories. These advisories depend on whether a crop is damaged and the cause of that damage, such as weather, pests, diseases, or man-made factors.

## Features

- **Damage Classification**: Classifies crops into categories: Good growth (G), Drought (DR), Nutrient Deficient (ND), Weed (WD), and Other (including pest, disease, or wind damage).
- **Insurance Claim Verification**: Automates the verification of insurance claims based on crop damage classification.
- **Personalized Advisories**: Provides personalized agricultural advisories to farmers based on the classification results.

## Dataset

The project uses a collection of smartphone images of crops categorized into the following damage types:

- **DR**: Drought
- **G**: Good (growth)
- **ND**: Nutrient Deficient
- **WD**: Weed
- **Other**: Disease, Pest, Wind

The dataset is divided into training (train directory) and test (test directory) sets. The training set includes labeled images, while the test set contains images without labels for evaluation.

## Methodology

The project follows a structured approach to classify crop damage accurately:

1. **Data Ingestion**: Collect and organize the images.
2. **Data Transformation**: Preprocess the images, including resizing, normalization, and augmentation.
3. **Data Validation**: Ensure the quality and consistency of the data.
4. **Model Training**: Train the model using the preprocessed dataset.
5. **Model Evaluation**: Evaluate the model using metrics like accuracy and Log Loss.

## Installation

Follow these steps to set up the project on your local machine:

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/yash-raj202134/CropDamageClf.git
    ```

2. **Install Dependencies**:
    - Create and activate a virtual environment:
        ```bash
        python -m venv cropdamageclf
        source cropdamageclf/bin/activate  # On Windows, use `cropdamageclf\Scripts\activate`
        ```
    - Install the required packages:
        ```bash
        pip install -r requirements.txt
        ```

3. **Prepare Data**:
    - Ensure the dataset is available in the specified directory.
    - Follow the instructions in the project documentation to format and preprocess the dataset.

## Usage

To use the CropDamageClf project, follow these steps:

1. **Run the Preprocessing Script**:
    ```bash
    python preprocess_data.py
    ```

2. **Train the Model**:
    ```bash
    python train_model.py
    ```

3. **Evaluate the Model**:
    ```bash
    python evaluate_model.py
    ```

4. **Classify New Images**:
    ```bash
    python classify_image.py --image_path path/to/image/file
    ```

## Evaluation

The evaluation metric for this project is Log Loss. Your submission should look like:

| ID        | DR  | G   | ND  | WD  | Other |
|-----------|-----|-----|-----|-----|-------|
| ID_YMXCDK | 0.73| 0.19| 0.01| 0.67| 0.92  |
| ID_B3HJ3N | 0.03| 0.45| 0.99| 0.46| 0.20  |

The values should be between 0 and 1. Do not set thresholds or round your probabilities to improve your place on the leaderboard. This ensures the client receives the best solution and can set thresholds according to their needs.

## Compute Restrictions

The model should be lightweight and able to train and run inference within reasonable time constraints:

- **Training Time**: Less than 8 hours on a single-GPU machine (e.g., Nvidia P100).
- **Inference Time**: Less than 1 hour.
- **Implementation Environment**: 4-core Virtual Machine with up to 16GB of RAM.

## Technologies Used

- **Python**: The primary programming language for the project.
- **TensorFlow/Keras**: Used for building and training the deep learning models.
- **OpenCV**: Utilized for image processing and augmentation.
- **Pandas/Numpy**: Employed for data manipulation and analysis.
- **Scikit-learn**: Used for model evaluation and performance metrics.
- **Jupyter Notebooks**: For exploratory data analysis and experimentation.

## Contributing

We welcome contributions from the community! If you would like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch with your changes.
3. Make a pull request to the main branch.

For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contact

Feel free to reach out with any questions or feedback:

- **Author**: Yash Raj
- **Email**: yashraj3376@gmail.com
- **LinkedIn**: [Yash Raj](https://www.linkedin.com/in/yash-raj-8b924a296/)

## Acknowledgments

- Thanks to the contributors and the open-source community for their invaluable support.
- Special thanks to my mentors and peers who provided guidance and feedback throughout the project.
- We thank CGIAR Research Initiative on Digital Innovation for technical and financial support that made this challenge possible.

---

Happy Coding!
