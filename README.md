
# 🎙️ Jarvis Voice Assistant <br><br>

## Introduction <br>
Jarvis is a simple voice-controlled assistant developed using Python. <br>
It listens for a wake word ("Jarvis") and performs tasks like opening websites and playing music using voice commands. <br><br>

## Libraries Used <br>
The following libraries are used in this project: <br><br>

• speech_recognition (sr) – Used for recognizing speech input. <br>
• webbrowser – Opens web pages in the default browser. <br>
• pyttsx3 – Text-to-speech library (not used in this version). <br>
• musicLibrary – Custom module that stores music names and their links. <br>
• openai – For OpenAI API integration (not used currently). <br>
• gtts (gTTS) – Converts text into speech. <br>
• pygame – Plays audio files. <br>
• os – Handles file operations like deleting temporary files. <br><br>

## Speak Function <br>
The speak function converts text to speech and plays it using gTTS and pygame. <br><br>

Text-to-Speech Conversion: <br>
`tts = gTTS(text)` <br>
`tts.save("temp.mp3")` <br><br>

Playing the Audio: <br>
`pygame.mixer.init()` <br>
`pygame.mixer.music.load("temp.mp3")` <br>
`pygame.mixer.music.play()` <br><br>

Cleanup: <br>
`os.remove("temp.mp3")` <br><br>

## processCommand Function <br>
This function takes voice input and performs actions based on the command. <br><br>

Open Websites: <br>
If the user says "open google", it opens Google in the browser. <br><br>

Play Music: <br>
If the command starts with "play", it extracts the song name and opens the song link from musicLibrary. <br><br>

## Main Program Loop <br>
The program continuously listens for the wake word "Jarvis". <br>
Once detected, it listens for a command and executes it. <br><br>

Steps: <br>
• Listen for wake word <br>
• Accept voice command <br>
• Process command <br>
• Handle errors if any <br><br>

## Error Handling <br>
All runtime and recognition errors are handled using exception handling and printed for debugging. <br><br>

## Conclusion <br>
This project demonstrates a basic Python voice assistant using speech recognition, text-to-speech, and audio playback. <br>
