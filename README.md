<p align="center">
  <img src="https://raw.githubusercontent.com/toptuk/whisper-assistant-vscode/main/images/logo.jpg" alt="Speak 2 Script">
</p>

# Speak2Script: Trunscribe your voice to code

Speak2Script is an extension for Visual Studio Code or [Cursor](https://www.cursor.com/) that transcribes your spoken words into text. This hands-free approach to coding allows you to focus on your ideas instead of your typing.

# Powered by OpenAI Whisper
**Note: This extension requires an API key.**

By default, Speak2Script use OpeanAI WHisper model and requires API key.
There is also the option to use Groq API to transcribe your audio for remote transcription.

For more details about Whisper, visit the [Whisper OpenAI GitHub page](https://github.com/openai/whisper).

## Getting Started: Installation Instructions

To install and setup Speak2Script, follow these steps:

1.  Install SoX utility to enable easy microphone recording through the command line.

    - MacOS: Using the Homebrew package manager, run the following command in your terminal:
      ```
      brew install sox
      ```
    - Windows: Using the Chocolatey package manager, run the following command in your terminal:
      ```
      choco install sox.portable
      ```
      **Note for Windows Users:** Some users have reported issues with newer SoX versions not recognizing the default audio device. If you encounter this, installing version 14.4.1 specifically might resolve the problem. You can install it using Chocolatey with the following command:
      ```
      choco install sox.portable --version=14.4.1
      ```
    - Ubuntu: Run the following command in your terminal:
      ```
      sudo apt install sox
      ```
2.  Install the Speak2Script extension into Visual Studio Code or Cursor.

# How to Use Speak2Script

1. **Initialization**: Upon loading Visual Studio Code, the extension verifies the correct installation of SoX. If any issues are detected, an error message will be displayed.

Once initialization is complete, a quote icon will appear in the bottom right status bar.

  <img src="https://raw.githubusercontent.com/toptuk/speak-2-script/main/images/microphone.png" alt="Whisper Assistant icon" style="width: 144px; height: auto; ">

2. **Starting the Recording**: Activate the extension by clicking on the quote icon or using the shortcut `Command+M` (for Mac) or `Control+M` (for Windows). You can record for as long as you like, but remember, the longer the recording, the longer the transcription process. The recording time will be displayed in the status bar.

  <img src="https://raw.githubusercontent.com/toptuk/speak-2-script/main/images/recording.png" alt="Recording icon" style="width: 100px; height: auto;">

3. **Stopping the Recording**: Stop the recording using the same shortcut (`Command+M` or `Control+M`). The extension icon in the status bar will change to a loading icon, and a progress message will be displayed, indicating that the transcription is underway.

  <img src="https://raw.githubusercontent.com/toptuk/speak-2-script/main/images/transcribing.png" alt="Transcribing" style="width: 360px; height: auto; ">

4. **Transcription**: Once the transcription is complete, the text will be saved to the clipboard. This allows you to use the transcription in any program, not just within Visual Studio Code. If an editor is active, the transcription will be pasted there automatically.

  <img src="https://raw.githubusercontent.com/toptuk/speak-2-script/main/images/transcribed.png" alt="Transcribed" style="width: 400px; height: auto; ">

**Tip**: A good microphone will improve transcription accuracy, although it is not a requirement.

## Using Speak2Script with Cursor

To enhance your development experience with Cursor.so and Speak2Script, follow these simple steps:

1.  Start the recording: Press `Command+M` (Mac) or `Control+M` (Windows).
2.  Speak your instructions clearly.
3.  Stop the recording: Press `Command+M` (Mac) or `Control+M` (Windows).
    _Note: This initiates the transcription process._
4.  Open the Cursor dialog: Press `Command+K` or `Command+L`.
    _Important: Do this **before** the transcription completes._
5.  The transcribed text will automatically populate the Cursor dialog. Here, you can edit the text or add files/docs, then press `Enter` to execute the GPT query.

By integrating Cursor with Speak2Script, you can provide extensive instructions without the need for typing, significantly enhancing your development workflow.

# Configure API Options

Speak2Script offers two ways to transcribe your audio:

1. **OpenAI Cloud API**: A powerful cloud option using OpenAI's Whisper-1 model for fast, accurate transcription (requires API key)
2. **Groq Cloud API**: A powerful cloud option using Groq's Whisper Large v3 Turbo model for fast, accurate transcription (requires API key)

## Configuring the API Provider

1. Open VSCode settings (File > Preferences > Settings)
2. Search for "Speak2Script"
3. Set "Api Provider" to one of:
   - `openai`
   - `groq`
4. Enter your API key:
   - For OpenAI: Get your key from [OpenAI's console](https://platform.openai.com/api-keys)
   - For Groq: Get your key from [GROQ's console](https://console.groq.com)
