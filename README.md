# 🧐 Fact-Checking System

## Setup Guide

### 1️⃣ Extract the ZIP File
- Unzip the project folder to your preferred location.
---
### 2️⃣ Set Up a Virtual Environment

- Open a terminal or command prompt in the project folder.
- Run the following command to create a virtual environment:

#### **For Windows:**
```sh
python -m venv venv
```
#### **For Mac/Linux:**
```sh
python3 -m venv venv
```
- Activate the virtual environment:
#### **For Windows:**
```sh
venv\Scripts\activate
```
#### **For Mac/Linux:**
```sh
source venv/bin/activate
```
---
### 3️⃣ Install Dependencies
```sh
pip install -r requirements.txt
```
---
### 4️⃣ Run the Streamlit App
- Start the Streamlit app with:
```sh
streamlit run Home.py
```
- The application should open in your browser.
- Use the sidebar to enter and save your Hugging Face API token.
---
### 5️⃣ Add Your Hugging Face API Token
#### Option 1: Setting API Key via Environment Variable (Temporary)
- Works only for the current session.
- If you restart the terminal, you'll need to set the key again.
##### **For Windows:**
```sh
set HUGGINGFACEHUB_API_TOKEN=your_api_token_here
```
##### **For Mac/Linux:**
```sh
export HUGGINGFACEHUB_API_TOKEN=your_api_token_here
```

#### Option 2: Using a .env File (Permanent)
- Create a file named .env in the root directory.
- Add the following line:
```sh
HUGGINGFACEHUB_API_TOKEN=your_api_token_here
```
- The project will automatically load this key.

#### Option 3: Setting API Key Using Streamlit Sidebar
- Open the Streamlit app.
- Navigate to the LLM Implementation screen.
- Enter your Hugging Face API token in the sidebar.
- The token will be saved automatically for your session.

---

### 6️⃣ Run the Project
#### Streamlit App
```sh
streamlit run app.py
```
- Open the app in your browser and enter your API key in the sidebar.

#### CLI-Based Usage (main.py)
```sh
python main.py --query "Your fact-checking statement here"
```
- Make sure you have set up the API key using either environment variables or a .env file.

---

### Troubleshooting
- ModuleNotFoundError? Ensure the virtual environment is activated before running the app.
- Streamlit not found? Run pip install streamlit inside the virtual environment.
- API errors? Ensure you have entered the correct Hugging Face API token.


### How It Works
- Enter a claim to fact-check in the input box.
- If a similar claim exists in ChromaDB, the system will return a result, augmented by the LLM’s reasoning.
- If no similar claim is found, an LLM-based fact-checking API will be used.
- Review the response and analyze the credibility of the claim.

### Possible Future Enhancements
- 🚀 Add support for more LLMs (e.g., GPT-4, Claude).
- 🎯 Improve fact-checking accuracy with fine-tuned models and robust datasets.
- 📢 Implement a feedback mechanism to refine results.


Developed by Jhon Raza



