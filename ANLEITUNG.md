# Änderungen mit Git verwalten – Kurzanleitung

Dieser Ordner (`Webseite`) ist ein Git-Repository. Die Webseiten-Dateien liegen in `site/` –
genau dieser Inhalt wird auf den Webspace (IONOS) hochgeladen.

## Ablauf bei jeder Änderung
1. Dateien in `site/` ändern.
2. In `CHANGELOG.md` unter „Unveröffentlicht“ kurz notieren, was geändert wurde.
3. Speichern als Commit (Terminal im Ordner `Webseite`):
   ```
   git add -A
   git commit -m "Kurzbeschreibung der Änderung"
   ```
4. Wenn die Version fertig ist und online geht:
   - In `CHANGELOG.md` „Unveröffentlicht“ in „V59_02 – Datum“ umbenennen, neuen leeren Abschnitt „Unveröffentlicht“ anlegen.
   - Committen und Version markieren:
     ```
     git commit -am "V59_02: Kurzbeschreibung"
     git tag -a v59_02 -m "Version V59_02"
     ```

## Nützliche Befehle
| Zweck | Befehl |
|---|---|
| Was ist geändert, aber noch nicht gespeichert? | `git status` / `git diff` |
| Verlauf ansehen | `git log --oneline` |
| Alle Versionen | `git tag` |
| Unterschied zwischen zwei Versionen | `git diff v59_00 v59_01` |
| Nur die geänderten Dateien (für den Upload) | `git diff --name-only v59_00 v59_01` |
| ZIP einer Version erzeugen | `git archive --format=zip --prefix=Hofmetzgerei-Kronseder-V59_01/ v59_01:site -o ../Versionen/Hofmetzgerei-Kronseder-V59_01.zip` |
| Datei auf alten Stand zurückholen | `git restore --source v59_00 site/index.html` |

## Ohne Terminal
GitHub Desktop (kostenlos) funktioniert auch rein lokal, ohne GitHub-Konto:
„File → Add Local Repository…“ → Ordner `Webseite` wählen. Dort sieht man Änderungen farbig
und speichert Commits per Klick. Tags lassen sich im Verlauf per Rechtsklick setzen.
