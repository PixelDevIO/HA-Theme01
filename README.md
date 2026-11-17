# Theme01

Ein schlichtes, modernes und dezentes Theme für Home Assistant. Hell und Dunkel stecken in einer Datei; Home Assistant wählt den Modus nach der Einstellung im Benutzerprofil.

- Neutrale Flächen, Karten nur mit feiner 1-px-Linie, keine Schatten
- Ein einziger Akzent, in drei Varianten: **Theme01** (Blau), **Theme01 Salbei**, **Theme01 Graphit**
- Zustandsfarben nur, wenn etwas aktiv ist (Licht an, Heizen)
- 12 px Eckenradius, Schrift Inter (fällt auf Roboto bzw. die Systemschrift zurück, wenn Inter nicht installiert ist)
- Optional: dezente Animationen mit [card-mod](https://github.com/thomasloven/lovelace-card-mod)

## Installation über HACS

1. HACS öffnen, oben rechts das Menü und **Benutzerdefinierte Repositories** wählen.
2. `https://github.com/PixelDevIO/HA-Theme01` mit der Kategorie **Theme** hinzufügen.
3. **Theme01** herunterladen.
4. In der `configuration.yaml` müssen Themes aus dem Ordner `themes` geladen werden (bei den meisten Installationen schon vorhanden):

   ```yaml
   frontend:
     themes: !include_dir_merge_named themes
   ```

5. Die Aktion `frontend.reload_themes` ausführen (oder Home Assistant neu starten).
6. Im Benutzerprofil unter **Design** eine der drei Varianten wählen.

## Animationen (optional)

Das Theme bringt dezente Animationen mit. Damit Home Assistant sie anwendet, wird **card-mod** gebraucht:

1. In HACS nach **card-mod** suchen (`thomasloven/lovelace-card-mod`) und installieren.
2. Den Browser bzw. die App neu laden.

Ohne card-mod sieht das Theme genauso aus, nur ohne Bewegung.

Was animiert wird:

- Karten und Badges blenden beim Laden weich ein
- Wechsel zwischen Ansichten blendet weich über
- Farbwechsel bei Ein/Aus (Icons, Kacheln) laufen sanft statt hart
- Rahmen von Karten heben sich beim Überfahren mit der Maus leicht ab
- Kacheln und Buttons geben beim Antippen eine kurze Rückmeldung
- Seitenleiste, Tabs und Zeilen in Entitätenkarten haben sanfte Übergänge

Bewusst nicht animiert wird `transform` (Verschieben, Skalieren), damit Pop-ups mit fester Position, z. B. von bubble-card, nicht verrutschen. Wer im Betriebssystem **Bewegung reduzieren** eingestellt hat, bekommt keine Animationen.

Tipp: card-mod empfiehlt für Themes, es zusätzlich als `extra_module_url` zu laden. Dann greifen die Stile schneller und auch außerhalb von Dashboards. Die Anleitung steht im [card-mod README](https://github.com/thomasloven/lovelace-card-mod#performance-improvements).

## Eigene Anpassungen

Die Dauer der Übergänge lässt sich über die Variablen `t01-duration`, `t01-duration-fast` und `t01-ease` am Anfang der Theme-Datei ändern.

## Manuelle Installation

`themes/theme01.yaml` in den Ordner `config/themes/` kopieren und ab Schritt 4 weitermachen.

## Lizenz

MIT
