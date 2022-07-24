# text-in-audio-python
Transformando texto em audio em Python com a biblioteca pyttsx3.

```
import pyttsx3

leitura = open('/home/ander/Documentos/IA/ia', encoding="utf8")
nome = pyttsx3.init()
voices = nome.getProperty('voices')

nome.setProperty('voice', voices[1].id)
rate = nome.getProperty('rate')
nome.setProperty('rate', rate-35)
nome.setProperty('volume', 3)
nome.setProperty('voice', b'brazil')

text = leitura.read()

print(text)
nome.say(text)
nome.runAndWait()
leitura.close()

```
