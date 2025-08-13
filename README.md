# Jarvis AI Assistant

Jarvis is a personal AI assistant built with Python, designed to understand voice commands, interact with the internet, and leverage the power of artificial intelligence.

## Description

This project provides a voice-controlled assistant that can:
* Recognize spoken commands.
* Open various websites (YouTube, Wikipedia, Google) and system applications (FaceTime, Passky).
* Play music files.
* Tell the current time.
* Engage in AI-powered conversations using OpenAI's GPT-3.5/4 models.
* Execute specific AI prompts and save the responses to files.
* Allow users to quit the application or reset the chat history.

## Features

* **Voice Command Recognition:** Utilizes `speech_recognition` to process user input.
* **Web Navigation:** Opens specified websites directly.
* **Application Launcher:** Launches system applications.
* **Music Player:** Plays local music files.
* **AI Chatbot:** Maintains a conversational context with OpenAI.
* **AI Prompting:** Generates responses to specific prompts and stores them.
* **Time Display:** Announces the current time.
* **Customizable Configuration:** Requires an OpenAI API key for AI functionalities.

## Installation

1.  **Clone the repository:**
    ```bash
    git clone <repository_url>
    cd jarvis-ai
    ```
    *(Replace `<repository_url>` with the actual URL of your project if it's hosted)*

2.  **Install dependencies:**
    You'll need Python 3.x installed on your system.
    ```bash
    pip install -r requirements.txt
    ```
    *(You'll need to create a `requirements.txt` file with the following dependencies: `speechRecognition`, `openai`, `numpy`)*

3.  **Configure OpenAI API Key:**
    Create a `config.py` file in the root directory of the project with the following content:
    ```python
    # todo: Add your api key here
    apikey = "YOUR_OPENAI_API_KEY"
    ```
    Replace `"YOUR_OPENAI_API_KEY"` with your actual OpenAI API key.

## Usage

1.  **Run the main script:**
    ```bash
    python Main.py
    ```

2.  **Interact with Jarvis:**
    Once the script is running, Jarvis will greet you. You can then speak commands.

    **Examples:**
    * "Open YouTube"
    * "What's the time?"
    * "Open music" (will play the specified music file)
    * "Using artificial intelligence, write an email to my boss for resignation."
    * "Jarvis Quit" (to exit the program)
    * "Reset chat" (to clear the conversation history)

## Configuration

* **`config.py`**: This file is crucial for setting up your OpenAI API key. Ensure it's correctly placed and contains your key.
* **Music Path**: In `Main.py`, the `musicPath` variable is hardcoded. You may want to update this to point to your desired music file.
    ```python
    # todo: Add a feature to play a specific song
    if "open music" in query:
        musicPath = "/Users/harry/Downloads/downfall-21371.mp3" # Update this path
        os.system(f"open {musicPath}")
    ```

## Dependencies

* `speech_recognition`
* `openai`
* `numpy`
* `webbrowser` (built-in)
* `os` (built-in)
* `datetime` (built-in)
* `random` (built-in)

## To-Do / Future Improvements

* Add more websites and system applications to open.
* Implement more sophisticated music playback controls.
* Enhance error handling for voice recognition and API calls.
* Allow users to specify the music file to play.
* Integrate with other services or APIs.
* Implement a more robust way to manage chat history and context.
* Add support for different AI models.
