# Lernquiz

Kleine Web-App für die tägliche Lernkontrolle: Vorlesungsfolien hochladen, Gemini erstellt daraus 5 bis 10 Fragen, und was du falsch beantwortest, kommt an den folgenden Tagen wieder.

## Einrichtung (ca. 10 Minuten)

### 1. Gemini-API-Key holen

1. Geh auf https://aistudio.google.com und melde dich mit deinem Google-Konto an.
2. Klick auf „Get API key“ und dann auf „Create API key“.
3. Kopier den Key. Neue Keys beginnen mit `AQ.`, ältere mit `AIza`. Beides funktioniert.

Der Key ist kostenlos, solange du kein Abrechnungskonto verknüpfst. Wichtig: In der Gratis-Stufe darf Google die Inhalte zur Produktverbesserung nutzen. Vorlesungsfolien sind dafür unproblematisch, vertrauliche Unterlagen aus dem Praxisbetrieb solltest du aber nicht hochladen.

### 2. Repository auf GitHub anlegen

1. Auf github.com oben rechts auf „+“ und dann „New repository“.
2. Name: `lernquiz`, Sichtbarkeit: **Public** (GitHub Pages ist im Gratis-Account nur für öffentliche Repos verfügbar).
3. „Create repository“ klicken.
4. Auf der leeren Seite den Link „uploading an existing file“ anklicken, `index.html` und `README.md` hineinziehen und unten „Commit changes“ drücken.

Keine Sorge wegen „öffentlich“: Im Repo liegt nur der Programmcode. Dein API-Key, deine Fragen und dein Lernstand werden ausschließlich in deinem Browser gespeichert und landen nie auf GitHub.

### 3. GitHub Pages einschalten

1. Im Repo auf „Settings“ und links auf „Pages“.
2. Unter „Branch“ `main` und `/ (root)` wählen, dann „Save“.
3. Nach ein bis zwei Minuten ist die App erreichbar unter `https://DEIN-NUTZERNAME.github.io/lernquiz/`.

### 4. App einrichten

1. Seite öffnen, auf „Einstellungen“ gehen, den API-Key einfügen und „Verbindung testen“ drücken.
2. Falls das voreingestellte Modell nicht verfügbar ist, ins Modellfeld klicken und ein anderes Flash-Modell wählen. Flash-Modelle sind in der Gratis-Stufe enthalten und für Quizfragen schnell genug.
3. Seite als Lesezeichen speichern.

## Nutzung

- **Neues Quiz:** Fach wählen oder anlegen, PDF-Folien und/oder Notizen hinzufügen, Anzahl und Fragetypen festlegen, „Quiz erstellen“.
- **Heute:** zeigt, wie viele Fragen fällig sind, und startet das Tagesquiz. Falsch beantwortete Fragen kommen zuerst.
- **Fragen:** alle gespeicherten Fragen pro Fach, mit Lernstufe und nächstem Abfragetermin. Schlechte Fragen kannst du hier löschen.
- **Ohne API:** Ist das Tageslimit erreicht, unter „Neues Quiz“ den Bereich „Ohne API über die Gemini-App“ öffnen. Prompt kopieren, in der Gemini-App mit der PDF ausführen, Antwort zurück einfügen.

## So funktioniert die Wiederholung

Jede Frage hat eine Stufe von 0 bis 5. Richtig beantwortet steigt sie eine Stufe und kommt erst nach 2, 5, 10, 21 bzw. 45 Tagen wieder. Falsch (bei offenen Fragen auch „teilweise“) fällt sie auf Stufe 1 zurück und kommt am nächsten Tag erneut.

## Daten sichern

Alles liegt im Speicher deines Browsers. Wenn du die Browserdaten löschst oder im privaten Modus surfst, ist der Lernstand weg. Unter „Einstellungen“ kannst du deshalb ein Backup als Datei herunterladen und später wieder laden. Am besten alle paar Wochen.
