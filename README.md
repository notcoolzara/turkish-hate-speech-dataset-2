# Türkçe Nefret Söylemi Veri Seti 2
10,224 adet Türkçe tweetten oluşan etiketlenmiş nefret söylemi veri setidir.

Veri setindeki sınıf dağılımı şöyledir:

| Etiket  | Tweet Sayısı |
| ------------- | ------------- |
| nefret   | 2.336  |
| saldırgan   | 166  |
| hiçbiri  | 7.722   |
| **TOPLAM**  | **10.224**  |

# İletişim ve Atıf Bilgileri

**Veri kümesi ile ilgili sorularınız için:** islam.mayda@stu.khas.edu.tr 

**Veri kümesine referans vermek için:**

*İ. Mayda, Y. E. Demir, T. Dalyan and B. Diri, "Hate Speech Dataset from Turkish Tweets," Innovations in Intelligent Systems and Applications Conference (ASYU), Elazig, Turkey, 2021, pp. 1-6, doi: 10.1109/ASYU52992.2021.9599042.*

**Veri kümesi üzerinde yapılan çalışmaya dair yayın:**

IEEE Xplore: [https://ieeexplore.ieee.org/document/9599042](https://ieeexplore.ieee.org/document/9599042)

ResearchGate: [https://www.researchgate.net/publication/356365659_Hate_Speech_Dataset_from_Turkish_Tweets](https://www.researchgate.net/publication/356365659_Hate_Speech_Dataset_from_Turkish_Tweets)


------------------------------------------------------------------------

## Project Details

This project tackles the class imbalance and builds models to classify tweets into **Hiçbiri**, **Nefret**, and **Saldırgan** categories.

### Preprocessing Steps
1. **Tokenization**: Splitting tweets into individual tokens (words).
2. **Stop-word Removal**: Removing common Turkish words (e.g., "bir", "ve").
3. **Lowercasing**: Converting all text to lowercase for uniformity.

### Text Representation
- **CountVectorizer**: Counts the occurrence of words in tweets.
- **TfIdfVectorizer**: Highlights important words by adjusting frequency based on all tweets.

### Handling Class Imbalance
The dataset is imbalanced, with most tweets labeled as neutral. To address this:
- **Oversampling**: Using SMOTE to generate synthetic samples for minority classes.
- **Undersampling**: Reducing the number of neutral tweets.
- **Combined Methods**: Applying both oversampling and undersampling.

### Machine Learning Models
The following models were evaluated:
- **Random Forest**
- **LightGBM**
- **XGBoost**
- **Artificial Neural Network (ANN)**

#### Performance Metrics
- **Precision**, **Recall**, and **F1-Score** were used to evaluate model performance.

| Model         | Class         | Precision | Recall | F1-Score |
|---------------|---------------|-----------|--------|----------|
| Random Forest | Hiçbiri       | 0.85      | 0.97   | 0.91     |
|               | Nefret        | 0.85      | 0.70   | 0.77     |
|               | Saldırgan     | 0.20      | 0.10   | 0.13     |
| LightGBM      | Hiçbiri       | 0.89      | 0.96   | 0.92     |
|               | Nefret        | 0.87      | 0.76   | 0.81     |
|               | Saldırgan     | 0.23      | 0.10   | 0.14     |
| XGBoost       | Hiçbiri       | 0.88      | 0.96   | 0.92     |
|               | Nefret        | 0.84      | 0.75   | 0.79     |
|               | Saldırgan     | 0.24      | 0.10   | 0.14     |

### Key Findings
- LightGBM and XGBoost performed best for **Hiçbiri** and **Nefret** detection.
- All models struggled with the **Saldırgan** class due to its small size.
- Resampling techniques improved recall but leave room for further enhancement.

---

## Future Work
- Further explore deep learning models (e.g., BERT-based architectures).
- Experiment with advanced preprocessing methods and feature engineering.
- Enhance resampling techniques to address the imbalance more effectively.

---

When referencing this work, please cite:  
*I. Mayda, Y. E. Demir, T. Dalyan and B. Diri, "Hate Speech Dataset from Turkish Tweets," ASYU 2021.*  

