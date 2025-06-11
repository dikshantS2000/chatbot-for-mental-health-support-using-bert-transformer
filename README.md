# chatbot-for-mental-health-support-using-bert-transformer

This project implements a simple chatbot that uses BERT (from Hugging Face Transformers) for intent classification. The chatbot is trained on an `intents_updated.json` file and can respond to user inputs based on predicted intent tags.

---

## 📂 Project Structure

- `intents_updated.json`: JSON file with intents, patterns, and responses.
- Jupyter Notebook: Contains all code for data preprocessing, training, and running the chatbot.
- `requirements.txt`: Required packages for the project.

---

## 🧠 Features

- Fine-tunes `bert-base-uncased` for multi-class text classification.
- Uses `LabelEncoder` for label transformation.
- Includes a training loop with accuracy monitoring.
- Real-time prediction with confidence thresholding.
- Simple console-based chat loop.

---

## 📋 Requirements

Install all required dependencies using:

```
pip install -r requirements.txt
```

🚀 How to Run

1. Ensure intents_updated.json is present in the working directory.
2. Open and run the notebook in Jupyter or convert it to a Python script.
3. After training, interact with the chatbot via the terminal.
4. Type exit to quit the chat loop.

📁 Example Format of intents_updated.json

```
{
  "intents": [
    {
      "tag": "greeting",
      "patterns": ["Hi", "Hello", "Hey"],
      "responses": ["Hello!", "Hi there!", "Greetings!"]
    },
    {
      "tag": "goodbye",
      "patterns": ["Bye", "See you later", "Goodbye"],
      "responses": ["Goodbye!", "Take care!", "See you again!"]
    }
  ]
}
```

📌 Notes

The model is trained from scratch for classification — weights of classifier layers are randomly initialized.
Confidence threshold of 0.1 is used to handle uncertain predictions.
Requires a CUDA-enabled GPU for faster training (optional but recommended).

🧪 Output Sample
```
Chatbot is ready! Type 'exit' to stop.
You: Hello
Chatbot: Hi there!
```
