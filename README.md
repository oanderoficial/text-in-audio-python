# text-in-audio-python
Transformando texto em audio em Python com a biblioteca pyttsx3.

```python

import pyttsx3

def speak_text_from_file(file_path):
    with open(file_path, encoding="utf8") as file:
        text = file.read()
    engine = pyttsx3.init()
    voices = engine.getProperty('voices')
    engine.setProperty('voice', voices[1].id)
    engine.setProperty('rate', engine.getProperty('rate') - 35)
    engine.setProperty('volume', 3)
    engine.setProperty('voice', b'brazil')

    print(text)
    engine.say(text)
    engine.runAndWait()

speak_text_from_file('/home/ander/Documentos/IA/ia')

```
