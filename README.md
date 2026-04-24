# PhishShield

Machine learning-based URL phishing detection system with real-time analysis.

## Features

- Real-time URL scanning
- ML-based detection (TF-IDF + structural features)
- Confidence scoring
- REST API support
- Lightweight and fast
- Privacy-focused (no data storage)

## Tech Stack

- Python
- Flask
- NumPy
- Pandas
- scikit-learn (Logistic Regression)
- Custom Ensemble (Pure Python)

## Project Structure

phishshield/
├── app.py
├── train_model.py
├── requirements.txt
├── phishing_site_urls.csv
│
├── Ensemble model/
│   ├── app.py
│   ├── train_ensemble_pure.py
│   └── requirements.txt
│
└── templates/
└── index.html


## Installation

bash
git clone https://github.com/yourusername/phishshield.git
cd phishshield


Create virtual environment:

bash
python -m venv venv
venv\Scripts\activate   # Windows
# or
source venv/bin/activate

Install dependencies:

bash
pip install -r requirements.txt

## Usage

### Train Model

bash
python train_model.py

For ensemble version:

bash
cd "Ensemble model"
python train_ensemble_pure.py

### Run Application

bash
python app.py

Open in browser:

http://localhost:5000

## API

### Predict

bash
POST /predict

Request:

json
{
  "text": "https://example.com"
}

Response:

json
{
  "label": "not_spam",
  "confidence": 0.98,
  "is_spam": false
}

## Models

### Logistic Regression

* ~95% accuracy
* Uses scikit-learn

### Pure Python Ensemble

* ~94% accuracy
* Includes:

  * Logistic Regression
  * Decision Tree
  * Random Forest
  * Naive Bayes

## Dataset Format

csv
URL,Label
https://google.com,good
http://phishing-site.xyz,bad


## Troubleshooting

**Model not found**

bash
python train_model.py

**Missing dependencies**

bash
pip install -r requirements.txt

**Port already in use**

* Change port in `app.py`

## Contributing

Pull requests are welcome.

## License

MIT License

## Disclaimer

This project is for educational purposes only. Do not rely on it as your only security tool.

## Author

Francis Norbert Ouma
