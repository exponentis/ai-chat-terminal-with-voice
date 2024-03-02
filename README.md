# ai-chat-terminal-with-voice

Python terminal that enables a User/Assistant conversation driven by a content generation function, taking both text and voice as user input

## Usage

```python
from terminal_with_voice_input import start_terminal_with_voice_input

def process(input):
    return f"Done processing input: \"{input}\""

start_terminal_with_voice_input(process)
```

## Dependencies

The `speech_recognition` python library

For `whisper`, no other dependencies

For `vosk`:

* download a model from [https://alphacephei.com/vosk/models](https://alphacephei.com/vosk/models), unzip, rename folder to *model* and place in the root folder.
* install the python `json` library and import it as dependency
*  extract transcribed text from within json:
    ```
   text = recognizer.recognize_whisper(audio_data)
   text = json.loads(transcription)["text"]
   ```

