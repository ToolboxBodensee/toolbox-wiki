 toolbox-wiki
===================
[![Build Status](https://travis-ci.org/ToolboxBodensee/toolbox-wiki.svg?branch=master)](https://travis-ci.org/ToolboxBodensee/toolbox-wiki)
Das *neue* Wiki der Toolbox


Hier entsteht das Toolbox Wiki.
You have to install [Nikola](https://getnikola.com/getting-started.html) to get it working locally.


 Wo gehört was hin?
-------------------
### Wiki-Seiten
Wiki-Seiten gehören in den ``posts`` Ordner.

### Bilder
Bilder sind im ``galerie`` Ordner sehr gut aufgehoben.

### Das Menü
Das Menü wird in der Datei ``conf.py`` definiert.


 Cheat Sheet
-------------
**Clone**
```bash
git clone https://gitea.see-base.de/toolbox/toolbox-wiki.git
```

**Install Nikola**:
```bash
pip install --upgrade "Nikola[extras]"
````

**New site**
```bash
nikola new_post -e
```

**Build site**
```bash
nikola build
```

**Serve local site**
```bash
nikola serve --browser
```
