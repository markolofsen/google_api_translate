<p align="center"><b>🛠️ Questo repository è stato creato usando <a href="https://gitupload.com">GitUpload</a>.</b></p>
<p align="center"><a href="https://kupi.net"><img src="https://github.com/markolofsen/google_api_translate//blob/master/.banners/banner_it.png?raw=1" /></a></p>
<p align="center"><b>Languages:</b><br /><a href="https://github.com/markolofsen/google_api_translate/blob/master/README_de.md">🇩🇪 Deutsch</a> | <a href="https://github.com/markolofsen/google_api_translate/blob/master/README.md">🇬🇧 English</a> | <a href="https://github.com/markolofsen/google_api_translate/blob/master/README_es.md">🇪🇸 Spanish</a> | <a href="https://github.com/markolofsen/google_api_translate/blob/master/README_fr.md">🇫🇷 French</a> | <b>🇮🇹 Italian</b> | <a href="https://github.com/markolofsen/google_api_translate/blob/master/README_ru.md">🇷🇺 Russian</a></p>

---

# Libreria arricchita per la traduzione di testo dall&#39;API di Google Traduttore (per Python 3)!

Library version = 2.1.2 <br />
Nome libreria = google_api_translate <br />
Titolo = Google Translate API (Python 3) <br />
Parole chiave = Google Cloude API <br />

### Caldo da installare

```sh
pip3 install google_api_translate==2.1.2
```


## Come usare

1. Abilitare il [Cloud Translation API] (https://cloud.google.com/translate/docs/quickstart?csw=1)
2. Scarica una chiave privata come file JSON.
3. Specificare il percorso del file nella variabile &quot;creds_path&quot;

### Esempio 1
```python
import os
from google_api_translate import Translator, TextUtils
creds_path = os.path.join(os.path.dirname(__file__), 'creds.json')

s = Translate(creds_path=creds_path).translate(text="Hello new world!", target_language='cn')
print(s.text)
```

### Esempio 2
```python
import os
from google_api_translate import Translator, TextUtils
creds_path = os.path.join(os.path.dirname(__file__), 'creds.json')

html_str = '<p>Russian word</p>'
s = Translator(creds_path=creds_path).html(text=html_str, target_language='ru')
print(s.text)
```

### Esempio 2
```python
from google_api_translate import TextUtils
s = TextUtils().detect('Detect my language please...')
print(s)
```



### Utilizzare qualsiasi variabile senza traduzione? - Facile!
```python
import os
from google_api_translate import Translator, TextUtils
creds_path = os.path.join(os.path.dirname(__file__), 'creds.json')

text = "Hi, this is [[name]], waiting for $ [[number]] from you!"
s = Translator(creds_path=creds_path).translate(text="Hello new world!", target_language='ru')
print(s.text)
```

Risultato: «Привет, это [[name]], жду от тебя $ [[number]]!»

---

<p align="center"><b>🛠️ Questo repository è stato creato usando <a href="https://gitupload.com">GitUpload</a>.</b></p>