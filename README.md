# Gemini CLI 🚀

A powerful, lightweight Python script that brings Google's Gemini models (1.5 Flash & Pro) to your Linux terminal. Interact with Gemini using both text and images directly from your command line.

🛠️ Installation
1. Get Dependencies
Clone the repository (if you haven't already)
```
git clone https://github.com/prateek-puranik/gemini_from_terminal.git
cd gemini_from_terminal
```

Install required Python packages
```
pip install --break-system-packages google-generativeai Pillow
```

2. Configure API Key
This is a one-time setup. Get your key from [Google AI Studio](https://aistudio.google.com/).

```
echo 'export GEMINI_API_KEY="YOUR_API_KEY_HERE"' >> ~/.bashrc
source ~/.bashrc
```

3. Install the Script
Make the script executable and move it to a location in your PATH.

make sure the file is titled 'askg'
```
chmod +x askg
mkdir -p ~/.local/bin
mv askg ~/.local/bin/
```

Open a new terminal for the askg command to be available.

# 🚀 Usage
The script handles multimodal (text + image) queries. The prompt should always come before optional flags like -i or -m.

Basic Text Query:
```
askg "What are the main differences between Python lists and tuples?"
```

Using the Pro Model:
```
askg -m pro "Write a short story about a robot who discovers music."
```

Analyze an Image:
```
askg "Describe the architecture of this building." -i /path/to/building.jpg
```

Compare Multiple Images:
```
askg "Which of these two logos is more effective and why?" -i logo1.png -i logo2.png
```
