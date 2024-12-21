# Music Genre Classification Using Convolutional Neutral Networks
## Abstract
This project aims to classify songs based on their genres with the help of Convolutional Neural Networks, leveraging the GTZAN dataset. The model uses Mel-frequency cepstral coefficients (MFCCs) extracted from 3-second audio segments as input features. This model outperforms traditional 1D CNN models, achieving a test accuracy of 90% approximately. It demonstrates the potential for real-world applications like music recommendation systems and automated playlist categorization.

## Dataset
This project utilizes the GTZAN dataset, a benchmark dataset widely employed for music genre classification tasks. The dataset comprises 1,000 music tracks, each 30 seconds long, evenly distributed across 10 genres: Blues, Classical, Country, Disco, Hip Hop, Jazz, Metal, Pop, Reggae, and Rock. 
While the dataset includes a variety of audio sources ensuring diversity, it has some known issues such as:
- Duplicate tracks and mislabeled genres.
- Lack of metadata on recording conditions or sources.

To address these challenges and facilitate segment-wise learning, we used a 3-second segmented version of the dataset (features_3_seconds). This resulted in a total of 9,990 audio segments, ensuring adequate data points for training, validation, and testing.

You can download it from [Kaggle](https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification).  

## Preprocessing
Preprocessing is a crucial step to ensure that the raw audio data was converted into a suitable format for the convolutional neural network (CNN). The preprocessing of the GTZAN dataset involved several steps to prepare the audio data for training the CNN model. Each 30-second track was segmented into 3-second non-overlapping clips, resulting in a total of 9,990 audio segments. For each segment, Mel-Frequency Cepstral Coefficients (MFCCs) were extracted to capture the spectral and temporal characteristics of the audio, with 13 coefficients computed per segment. These features were normalized to have a mean of 0 and a standard deviation of 1, ensuring consistency and aiding model convergence. The dataset was then split into training (80%), validation (10%), and test (10%) subsets using a stratified sampling approach to maintain a balanced genre distribution.

## Results: 
![image](https://github.com/user-attachments/assets/579438aa-ef43-41a2-bbb4-1e2df1594f59)

Feel free to explore the code, dataset preparation steps, and model training process in the repository. Contributions and suggestions are welcome!
