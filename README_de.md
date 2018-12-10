<p align="center"><b>🛠️ Dieses Repository wurde mit <a href="https://gitupload.com">GitUpload</a> erstellt.</b></p>
<p align="center"><a href="https://gitupload.com"><img src="https://github.com/markolofsen/google_api_translate//blob/master/.banners/banner_de.png?raw=1" /></a></p>
<p align="center"><b>Languages:</b><br /><b>🇩🇪 Deutsch</b> | <a href="https://github.com/markolofsen/google_api_translate/blob/master/README.md">🇬🇧 English</a> | <a href="https://github.com/markolofsen/google_api_translate/blob/master/README_es.md">🇪🇸 Spanish</a> | <a href="https://github.com/markolofsen/google_api_translate/blob/master/README_fr.md">🇫🇷 French</a> | <a href="https://github.com/markolofsen/google_api_translate/blob/master/README_it.md">🇮🇹 Italian</a> | <a href="https://github.com/markolofsen/google_api_translate/blob/master/README_ru.md">🇷🇺 Russian</a></p>

---

# Erweiterte Bibliothek zum Übersetzen von Text aus der Google Translate API (für Python 3)!

Bibliotheksversion = 2.1.4 <br />
Bibliotheksname = google_api_translate <br />
Titel = Google Translate API (Python 3) <br />
Schlüsselwörter = Google Cloude API, google api translate free <br />

### Heiß zu installieren

```sh
pip3 install google_api_translate==2.1.4
```


## Wie benutzt man

1. Aktivieren Sie die [Cloud Translation API] (https://cloud.google.com/translate/docs/quickstart?csw=1).
2. Laden Sie einen privaten Schlüssel als JSON-Datei herunter.
3. Geben Sie den Pfad zur Datei in der Variable &quot;creds_path&quot; an.

### Probe 1
```python
import os
from google_api_translate import Translator, TextUtils
creds_path = os.path.join(os.path.dirname(__file__), 'creds.json')

s = Translate(creds_path=creds_path).translate(text="Hello new world!", target_language='cn')
print(s.text)
```

### Probe 2
```python
import os
from google_api_translate import Translator, TextUtils
creds_path = os.path.join(os.path.dirname(__file__), 'creds.json')

html_str = '<p>Russian word</p>'
s = Translator(creds_path=creds_path).html(text=html_str, target_language='ru')
print(s.text)
```

### Probe 2
```python
from google_api_translate import TextUtils
s = TextUtils().detect('Detect my language please...')
print(s)
```



Verwendung beliebiger Variablen ohne Übersetzung? - Einfach!
```python
import os
from google_api_translate import Translator, TextUtils
creds_path = os.path.join(os.path.dirname(__file__), 'creds.json')

text = "Hi, this is , waiting for $ [[number]] from you!"
s = Translator(creds_path=creds_path).translate(text="Hello new world!", target_language='ru')
print(s.text)
```

Ergebnis: «Привет, это , жду от тебя $ [[number]]!»

---

<p align="center"><b>🛠️ Dieses Repository wurde mit <a href="https://gitupload.com">GitUpload</a> erstellt.</b></p>