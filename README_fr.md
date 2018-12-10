<p align="center"><b>🛠️ Ce référentiel a été créé en utilisant le <a href="https://gitupload.com">GitUpload</a>.</b></p>
<p align="center"><a href="https://gitupload.com"><img src="https://github.com/markolofsen/google_api_translate//blob/master/.banners/banner_fr.png?raw=1" /></a></p>
<p align="center"><b>Languages:</b><br /><a href="https://github.com/markolofsen/google_api_translate/blob/master/README_de.md">🇩🇪 Deutsch</a> | <a href="https://github.com/markolofsen/google_api_translate/blob/master/README.md">🇬🇧 English</a> | <a href="https://github.com/markolofsen/google_api_translate/blob/master/README_es.md">🇪🇸 Spanish</a> | <b>🇫🇷 French</b> | <a href="https://github.com/markolofsen/google_api_translate/blob/master/README_it.md">🇮🇹 Italian</a> | <a href="https://github.com/markolofsen/google_api_translate/blob/master/README_ru.md">🇷🇺 Russian</a></p>

---

# Bibliothèque enrichie pour la traduction de texte à partir de l&#39;API Google Translate (pour Python 3)!

Version de la bibliothèque = 2.1.4 <br />
Nom de la bibliothèque = google_api_translate <br />
Titre = Google Translate API (Python 3) <br />
Mots-clés = Google Cloude API, google api translate free <br />

### Chaud à installer

```sh
pip3 install google_api_translate==2.1.4
```


## Comment utiliser

1. Activez le [Cloud Translation API] (https://cloud.google.com/translate/docs/quickstart?csw=1).
2. Téléchargez une clé privée sous forme de fichier JSON.
3. Spécifiez le chemin du fichier dans la variable &quot;chemin_cred&quot;

### Sample 1
(dix)]

### Sample 2
```python
import os
from google_api_translate import Translator, TextUtils
creds_path = os.path.join(os.path.dirname(__file__), 'creds.json')

html_str = '<p>Russian word</p>'
s = Translator(creds_path=creds_path).html(text=html_str, target_language='ru')
print(s.text)
```

### Sample 2
```python
from google_api_translate import TextUtils
s = TextUtils().detect('Detect my language please...')
print(s)
```



### Utilisation de variables sans traduction? - Facile!
```python
import os
from google_api_translate import Translator, TextUtils
creds_path = os.path.join(os.path.dirname(__file__), 'creds.json')

text = "Hi, this is , waiting for $ [[number]] from you!"
s = Translator(creds_path=creds_path).translate(text="Hello new world!", target_language='ru')
print(s.text)
```

Résultat: «Привет, то , жду от тебя $ [[number]]!»

---

<p align="center"><b>🛠️ Ce référentiel a été créé en utilisant le <a href="https://gitupload.com">GitUpload</a>.</b></p>