 <H3>NAME: PRAJAN P</H3>
<H3>REGISTER NO:212223240121</H3>
<H3>EX. NO.8</H3>
<H3>DATE: 11.11.2024 </H3>
<H1 ALIGN =CENTER>Implementation of Speech Recognition</H1>
<H3>Aim:</H3> 
 To implement the conversion of live speech to text.<BR>
<h3>Algorithm:</h3>
Step 1: Import the speech_recognition library<Br>
Step 2: Initialize the Recognizer<Br>
Step 3: Create an instance of the Recognizer class, which will be used for recognizing speech.<Br>
Step 4: Set the duration for audio capture<Br>
Step 5: Define a variable to specify the duration (in seconds) for which the program will capture audio from the microphone.<Br>
Step 6: Display a message in the console to prompt the user to speak.<Br>
Step 7: Capture audio from the default microphone<Br>
Step 9: Use the default microphone as the audio source.<Br>
Step 10: Record audio for the specified duration using the Recognizer instance.<Br>
Step 11: Perform speech recognition with exceptional handling:<Br>
•	Attempt to recognize speech from the captured audio using the Google Speech Recognition service.<Br>
•	If successful, print the recognized text.<Br>
•	Handle specific exceptions: If the recognition result is unknown or if there is an issue with the request to the Google Speech Recognition service, print corresponding error messages.<Br>
•	A generic exception block captures any other unexpected errors.<Br>
<H3>Program:</H3>

```
import speech_recognition as sr
r = sr.Recognizer()
duration = 30
print("Say something")
with sr.Microphone() as source:
    audio_data = r.listen(source,timeout=duration)

try:
    text= r.recognize_google(audio_data)
except sr.UnknownValueError:
    print("Sorry, couldn't understand the audio")
except sr.RequestError as e:
    print(f'Error with request tp Google Speech Recognition service: {e}')
except Exception as e:
    print(f'Error : {e}')
```

<H3> Output:</H3>

![378376556-c96e7b80-8474-43f4-a9e0-8fad643be4f2](https://github.com/user-attachments/assets/784053df-0a60-4593-a316-28832d400ec4)

<H3> Result:</H3>
