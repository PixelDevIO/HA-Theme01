# Theme01

Ein schlichtes, modernes und dezentes Theme für Home Assistant, mit hellem und dunklem Modus in einer Datei.

- Neutrale Flächen, Karten nur mit feiner 1-px-Linie, keine Schatten
- Ein einziger Akzent (ruhiges Blau)
- Zustandsfarben nur, wenn etwas aktiv ist (Licht an, Heizen)
- 12 px Eckenradius, Schrift Inter (fällt auf Roboto/Systemschrift zurück)

## Installation über HACS

1. HACS öffnen, oben rechts das Menü und **Benutzerdefinierte Repositories** wählen.
2. `https://github.com/PixelDevIO/HA-Theme01` mit der Kategorie **Theme** hinzufügen.
3. **Theme01** herunterladen.
4. In der `configuration.yaml` müssen Themes aus dem Ordner `themes` geladen werden:

   ```yaml
   frontend:
     themes: !include_dir_merge_named themes
   ```

5. Home Assistant neu starten oder die Aktion `frontend.reload_themes` ausführen.
6. Im Benutzerprofil unter **Design** „Theme01“ wählen. Hell oder Dunkel folgt der Einstellung „Automatisch / Hell / Dunkel“ im Profil.

## Manuelle Installation

`themes/theme01.yaml` in den Ordner `config/themes/` kopieren und ab Schritt 4 weitermachen.

## Lizenz

MIT
