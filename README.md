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

Installation mit dem Skript `pnpm create strapi`. Daraufhin führt das CLI durch die Installation. Falls bei der Installation sogenannte `build scripts` nicht ausgeführt werden können, schlägt die CLI die Fehlermeldung selbstständig vor:

1. Wechsel in das Installationsverzeichnis (z. B. mit`cd Kanuric-strapi`)
2. Neuerliche Versuch der Installation mit `pnpm install`. Dieser scheitert in der Regel - die Build-Skripte müssen mit `pnpm approve-builds`
