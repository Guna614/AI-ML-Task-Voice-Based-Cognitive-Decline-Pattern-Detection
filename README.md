# AI-ML-Task-Voice-Based-Cognitive-Decline-Pattern-Detection

📝 Final GitHub README (Colab-Compatible Project
# 🎧 Cognitive Risk Analysis using Audio and Speech Features

This project focuses on **analyzing voice samples** to extract cognitive features and detect anomalies using **machine learning**. It was implemented using Python and designed to run efficiently on **Google Colab** for accessibility and reproducibility.

---

## 📌 Objective

To analyze audio recordings and detect signs of cognitive risk based on:
- Speech rate
- Pitch variation
- Hesitation frequency
- Pauses
- Word count

A simple ML model is trained to detect anomalies that may signal **"At Risk"** cases.

---

## 🚀 How It Works

The notebook extracts features from `.wav` files and applies a **scikit-learn Isolation Forest** model to classify whether the speaker is **"Normal"** or **"At Risk"** based on their speech patterns.

---

## 🛠️ Libraries Used

| Library | Purpose |
|--------|---------|
| `librosa` | Audio analysis (duration, pitch, features) |
| `speech_recognition` | Transcribe speech to text |
| `pydub` | Audio format handling |
| `webrtcvad` | Voice activity detection (optional for fine-tuning pauses) |
| `nltk`, `spacy` | NLP processing and tokenization |
| `pandas`, `numpy` | Data processing |
| `scikit-learn` | Machine learning model (Isolation Forest) |
| `matplotlib`, `seaborn` | Data visualization |

---

## 📂 Project Structure

. ├── voice_clips/ # Uploaded .wav audio files (10+ samples) ├── Cognitive_Risk_Analysis.ipynb # Google Colab-ready notebook ├── README.md # Project documentation (this file)

---

## 📥 Setup in Google Colab

1. Upload `.wav` files when prompted.
2. All packages are installed at the top of the notebook.
3. Transcription, feature extraction, modeling, and visualization all occur in one place.

---

## 🔎 Features Extracted from Audio

| Feature        | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| `speech_rate`  | Number of words spoken per second                                           |
| `pitch_var`    | Variation in voice tone (pitch)                                             |
| `hesitations`  | Count of filler words like "um", "uh", "erm"                                |
| `pauses`       | Approximate count of pauses via spacing and punctuation in transcription    |
| `word_count`   | Total words spoken                                                          |

---

## 🧠 Machine Learning: Isolation Forest

- Used **Isolation Forest** to detect outliers in speaking patterns.
- Trained on scaled feature data.
- Tags speakers as:
  - `Normal`: Speech within expected range
  - `At Risk`: Potential cognitive or expressive difficulty

---

## 📊 Visualization

Used `seaborn.pairplot()` to visualize relationships between features and highlight the "risk" label across distributions.

![image](https://github.com/user-attachments/assets/6bd436ea-6d19-4299-bfcd-8dd7ae7b02f0)


---

## 🧪 Cognitive Risk Function

This project includes a callable function:
python
get_cognitive_score(audio_path)
✅ Transcribes the file
✅ Extracts features
✅ Returns "Normal" or "At Risk"

🧩 Example Output
File	Speech Rate	Pitch Var	Hesitations	Pauses	Word Count	Risk
user1.wav	1.95	26.2	3	5	85	Normal
user2.wav	1.20	14.1	6	7	60	At Risk
📌 Notes
You can scale up this solution by:

Using Whisper or Wav2Vec2 for better transcription

Applying Deep Learning models for fluency scoring

Adding pause duration analysis using webrtcvad for more accurate detection

🙌 Acknowledgements
Inspired by real-world use-cases in:

Mental health screening

Public speaking tools

Interview coaching and speech therapy

Built by K Guna Surya Kumar using open-source tools.

📎 License
This project is under the MIT License.


Would you like me to:
- you can always fork for any reference 👍
- Create a `requirements.txt` from the Colab cell?
- Help with publishing this to your actual GitHub repo?

Just say the word! Always free to help 😄
