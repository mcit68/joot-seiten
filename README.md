# Joot – Seiten für TestFlight

Fünf statische Dateien. Kein Generator, kein Build, keine Abhängigkeiten.

```
index.html          Startseite (DE)
support.html        Support + häufige Fragen (DE)
datenschutz.html    Datenschutzerklärung (DE)
en/index.html       Startseite (EN)
en/support.html     Support (EN)
en/privacy.html     Privacy policy (EN)
stil.css            gemeinsames Aussehen
```

## Online stellen

```bash
cd seiten
git init -b main
git add .
git commit -m "Joot: Support- und Datenschutzseiten"
gh repo create joot-seiten --public --source=. --push
```

Danach auf github.com im Repo: **Settings ▸ Pages ▸ Source: Deploy from a branch ▸
main / (root) ▸ Save**. Nach ein bis zwei Minuten liegt die Seite unter

```
https://<dein-github-name>.github.io/joot-seiten/
```

Das Repo muss öffentlich sein – GitHub Pages aus privaten Repos gibt es nur mit einem
bezahlten Plan.

## Diese beiden URLs braucht App Store Connect

| Feld in App Store Connect | URL |
|---|---|
| Privacy Policy URL | `https://<name>.github.io/joot-seiten/datenschutz.html` |
| Support URL / Marketing URL | `https://<name>.github.io/joot-seiten/support.html` |

## Später ändern

Datei bearbeiten, `git commit`, `git push` – nach etwa einer Minute ist die Änderung
online. Ändert sich etwas am Datenschutz, oben im Dokument das Datum mitziehen.
