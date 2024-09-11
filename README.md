# NLP Analysis of The Lord of the Rings Dialogues

This project applies Natural Language Processing (NLP) techniques to analyze dialogue from *The Lord of the Rings* movie scripts and books. The goal is to explore how different characters speak, the distribution of dialogue, and use machine learning models to predict which character is speaking based on the text.

## Project Structure

The project consists of several key sections:

### 1. Introduction
- **Context**: Analyzes dialogue from *The Lord of the Rings* movies and books.
- **Objectives**: 
  - Dialogue structure analysis.
  - Character classification using machine learning models.
  - Feature importance identification.

### 2. Data Preparation
- **Dataset**: The project uses *The Lord of the Rings* movie scripts and focuses on the dialogues attributed to specific characters.
- **Preprocessing**: Text is cleaned by removing punctuation, special characters, stopwords, and tokenized using the `spaCy` library.

### 3. Exploratory Data Analysis (EDA)
- **Character Analysis**: Distribution of dialogues by characters, dialogue lengths, and word frequency analysis.
- **Visualizations**: Histograms and bar charts showing dialogue length distribution and character-specific dialogue statistics.
- **Movie Comparison**: Dialogue distribution and word frequency across the three movies of the trilogy.

### 4. Machine Learning Analysis
#### 4.1 Unsupervised Learning
- **Clustering**: KMeans and Agglomerative Clustering are used to group similar dialogues and characters. Clustering is evaluated using the Silhouette Score.
- **Dimensionality Reduction**: TF-IDF and Truncated SVD are used to reduce the dimensionality of the data for clustering and visualization.

#### 4.2 Supervised Learning
- **Character Classification**: A Random Forest classifier is used to predict which character speaks based on dialogue text. The model is trained on TF-IDF features and evaluated with accuracy and classification reports.
- **Improvement Strategies**: 
  - Filtering for top characters to improve model accuracy.
  - Hyperparameter tuning to optimize the Random Forest classifier.
  
### 5. Conclusions and Summary
- **Findings**: 
  - Characters like Frodo, Sam, and Gandalf dominate the dialogue.
  - Frequent words reflect key narrative themes.
  - Classification performance improves after focusing on top characters and tuning the model.
  
## Requirements
To replicate the analysis, the following Python libraries are required:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `spacy`
- `tqdm`
- `wordcloud`
- `textblob`
- `unidecode`

## How to Run

1. Clone this repository.
2. Install the required libraries using `pip install -r requirements.txt`.
3. Run the notebook in Google Colab or locally.
4. Load the dataset located in `DB/LOTR/lotr_scripts.csv` for the analysis.

## Future Work
- **Additional Analysis**: Extend the analysis to *The Lord of the Rings* books for comparison with movie dialogues.
- **Improved Models**: Experiment with advanced NLP techniques such as LSTM or Transformer-based models to enhance character classification.
