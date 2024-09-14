
# Negotiation Chatbot

## Overview

The Negotiation Chatbot is a Streamlit application that simulates a price negotiation scenario between a customer and a sales assistant. It utilizes the Groq API to integrate AI capabilities, such as generating responses and performing sentiment analysis with the Llama 3 model.

## Features

- **Interactive Chat Interface**: Engage in a conversation with the chatbot through a user-friendly UI built with Streamlit.
- **Price Negotiation Logic**: The chatbot can accept offers, make counteroffers, and adjust pricing based on the sentiment of your messages.
- **Sentiment Analysis**: Analyzes the sentiment of the user's input and adjusts the negotiation strategy accordingly.
- **AI-Powered Responses**: Generates responses using the Llama 3 model via the Groq API when the user's input isn't a price offer.
- **Ngrok Integration**: Uses ngrok to expose the local server to the internet for external access during development or presentations.

## Installation

### Prerequisites

- **Python 3.7 or higher**
- **Groq API key**
  

### Steps

1. **Clone the Repository**

   ```bash
   git clone https://github.com/Rahul-R-7/Chatbot.git
   cd Chatbot
   ```

2. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up Environment Variables**

   #### Groq API Key

   Export your Groq API key as an environment variable:

   ```bash
   export GROQ_API_KEY='your_groq_api_key'
   ```

   #### Ngrok Auth Token

   Export your ngrok auth token as an environment variable:

   ```bash
   export NGROK_AUTH_TOKEN='your_ngrok_auth_token'
   ```

## Usage

### Start Ngrok Tunnel

In a terminal window, start ngrok to forward to port 8501:

```bash
ngrok authtoken $NGROK_AUTH_TOKEN
ngrok http 8501
```

Note the forwarding URL provided by ngrok (e.g., https://abcd1234.ngrok.io).

### Run the Streamlit App

In a new terminal window, navigate to the project directory and run:

```bash
streamlit run app.py --server.port 8501
```

### Access the Application

Open the ngrok forwarding URL in your web browser to interact with the chatbot.

## Code Explanation

The application consists of the following key components:

- **Product Class**: Defines the product being negotiated, including its base price, minimum acceptable price, and methods to update offers.
- **Sentiment Analysis Function**: Analyzes the user's message to determine if it's positive, negative, or neutral, influencing the negotiation strategy.
- **Bot Response Function**: Generates responses using the Llama 3 model via the Groq API, ensuring dynamic and context-aware interactions.
- **Main Function**: Manages the Streamlit app, handles user input, updates the conversation history, and controls the negotiation logic.

## Dependencies

- Python 3.7+
- Streamlit
- Groq API Client
- Pyngrok


## Contact

For any questions or feedback, please contact [rahulr21302@gmail.com].
