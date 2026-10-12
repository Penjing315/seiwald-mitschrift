# seiwald mitschrift

Das ist die README.md-Datei. MD steht für Markdown. Markdown ist eine heutzutage weit verbreitete Auszeichnungssprache (_Markup Language_, [Wikipedia](https://de.wikipedia.org/wiki/Auszeichnungssprache))

Weitere bekannte Aufzeichnungssprachen sind:

- Hypertext Markup Language (HTML)
- Extensible Markup Language (XML)
- Yeat Another Markup Language (YAML, YML)

## Installation von nodeJS

Javascript läuft unter normalen Umständen in einer Browser-Sandbox (nur im Browser).
Seit ca. 2010 gibt es eine Laufzeitumgebung (_Runtime Environment_) für JS, damit man auch serverseitig JS programmieren und ausführen kann: [Node.js](https://nodejs.org/en)

## Installation von pnpm

Der standardmäßige _Package Manager_ für Node.js ist `npm` (_node package manager_). Eine etwas modernere und inzwischen beliebtere Variante ist [`pnpm`](https://pnpm.io/)

## Installation von strapi

Installation mit dem Skript `pnpm create strapi`. Daraufhin führt das CLI durch die Installation. Falls bei der Installation sogenannte `build scripts` nicht ausgeführt werden können, schlägt die CLI (_Command line interface_) die Fehlermeldung selbstständig vor:

1. Wechsel in das Installationsverzeichnis (z. B. mit`cd Kanuric-strapi`)
2. Neuerliche Versuch der Installation mit `pnpm install`. Dieser scheitert in der Regel - die Build-Skripte müssen mit `pnpm approve-builds` manuell freigegeben werden.

# Historische Entwicklung von WebDev

Webdevelopment hat im Lauf der letzten rund 35 Jahre einige Evolutionsstufen durchlaufen

1. Statische Webseiten (HTML, CSS, JS) - initale Phase des Webdevelopments, bei der Inhalte fest im HTML-Code hinterlegt sind. Dominant in den 1990er Jahren.

2. Dynamische Website (mit serverseitiger Programmiersprache - PHP, Python, Ruby, Java, C#) - Inhalte werden in einer Datenbank gespeichert und bei Bedarf dynamisch in HTML-Seiten eingebunden. Dominant in den 2000er Jahren.

3. Single Page Applications (SPA) - mit Javascript-Frameworks erstellte "Web-Apps", die ähnliche Funktionen wie Desktop-Apps bieten. Dominant in den 2010er Jahren.Um Handy-Apps möglichst nah zu kommen, wurde der Progressive Web App (PWA)-Standard entwickelt werden. Damit können Webbapps offline funktionieren, Push-Benachrichtigungen senden und auf bestimmte native Funktionenn des Geräts zugreifen. Es gibt drei Vorausetzungen, die eine Webbapp erfüllken muss, um als PWA zu gelten:

4. 1.Sie muss über HTTPS ausgeliefert werden. 2.Sie muss ein Web-App-Manifest besitzen. 3.Sie muss Service Worker verwenden, um Inhalte im Cache zu speichern und offline verfügbar zu machen. Ein Service worker ist eine java skirpt datei die im Hintergrund läuft und bestimmte Aufgaben übernimmt, z.B. das Cachen von Inhalten, das Empfangen von Push-Benachrichtigungen oder das Synchronisieren von Daten im Hintergrund, selbst wennd er Browser geschlossen ist.



# VibeCoding / AgenticEngineering mit VS-Code und Github Copilot

VibeCoding passiert in VS-Code in erster Linie über die neu eingeführte Agent View. Dort können alle Anpassungenö des "_Coding Harness_" vorgenommen werden. Wir könnnen unseren _Harness_ mit verschiedenen Methoden anpassen:

-**MCP-Server**:
MCP steht für _Model Context Protocoll_. Es ist ein Standart der von Anthropic entwickelt wurde. Mit Hilfe von MCP können Chatbots/LLMs (_Large Language Model_) auf zusätzliche Tools zugreifen, die sie zu Experten in einem bestimmten Themenbreich machen.

# Javascript-Frontendentwicklung mit Framework (Svelt, React, Vue, Angular)

Frontend