
# Combined Phishing Detection Dataset

This dataset is a consolidated collection of phishing-related data from three different sources:

##  Dataset Details

| Source   | Description                                   | Rows  |
|----------|-----------------------------------------------|-------|
| `sms`    | SMS spam/phishing messages                    | 5,574 |
| `url`    | Phishing URLs (from URLhaus)                  | 89,851 |
| `webpage`| Webpage-based phishing (features + page text) | 11,430 |

**Total Rows**: 106,855  
**Label Distribution**:
- `1` = Phishing (96,313 entries)
- `0` = Legitimate (10,542 entries)

##  Columns

- `text`: The text content (SMS message, phishing URL, or webpage-related content)
- `label`: 
  - `1`: phishing
  - `0`: legitimate
- `source`: One of `sms`, `url`, or `webpage`

##  Usage

This dataset is suitable for fine-tuning phishing detection models using NLP architectures such as BERT. It can be loaded into `pandas`, or converted into HuggingFace datasets for transformer-based training.

##  Suggested Use

Fine-tune a binary classification model using the `text` as input and `label` as output. The `source` field can be used for analysis or ablation studies.

---

##  License

- SMS: Public corpus from UCI
- URL: [URLHaus](https://urlhaus.abuse.ch/)
- Webpage: [Shashwat Work's Dataset](https://www.kaggle.com/datasets/shashwatwork/web-page-phishing-detection-dataset) (CC BY 4.0)
