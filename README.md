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

4. 1.Sie muss über HTTPS ausgeliefert werden.
   2.Sie muss ein Web-App-Manifest besitzen. 
   3.Sie muss Service Worker verwenden, um Inhalte im Cache zu speichern und offline verfügbar zu machen. Ein Service worker ist eine java skirpt datei die im Hintergrund läuft und bestimmte Aufgaben übernimmt, z.B. das Cachen von Inhalten, das Empfangen von Push-Benachrichtigungen oder das Synchronisieren von Daten im Hintergrund, selbst wennd er Browser geschlossen ist.



# VibeCoding / AgenticEngineering mit VS-Code und Github Copilot

VibeCoding passiert in VS-Code in erster Linie über die neu eingeführte Agent View. Dort können alle Anpassungenö des "_Coding Harness_" vorgenommen werden. Wir könnnen unseren _Harness_ mit verschiedenen Methoden anpassen:

-**MCP-Server**:
MCP steht für _Model Context Protocoll_. Es ist ein Standart der von Anthropic entwickelt wurde. Mit Hilfe von MCP können Chatbots/LLMs (_Large Language Model_) auf zusätzliche Tools zugreifen, die sie zu Experten in einem bestimmten Themenbreich machen.

# Javascript-Frontendentwicklung mit Framework (Svelt, React, Vue, Angular)

Frontend Frameworks wenden folgende Arichitekturprizipien an, em eine möglichst gute *User Expirience* (Ux) zu erreichen:

- **Komponenten** - Komponenten sind die wiederverendbaren "Lego"-Bausteine einer Webapp. Sie kapseln HTML, CSS und JavaScript in einer einzigen Einheit, die unabhängig von anderen Komponenten entwickelt und getestet werden kann. Komponenten können verschachtelt werden, um komplexe Benutzeroberflächen zu erstellen.

- **Deklarative Programmierung** - der Javascript- und Template(HTML)-Code beschreibt, wie die Benutzeroberfläche aussehen soll, anstatt wie sie erstellt werden soll. Das Framework übernimmt die Aufgabe, den DOM (Document Object Model) zu aktualisieren, wenn sich der Zustand der Anwendung ändert. Dabei kommt **Reaktivität** ins Spiel: Wenn sich der Zustand einer Komponente ändert, wird die Benutzeroberfläche automatisch aktualisiert, um den neuen Zustand widerzuspiegeln. Wenn die Aktualisierung auch in die andere funktioniert (d.h. wenn sich der Zustand (_state_) der Anwendung entsprechend aktualisiert wird), spricht man von bildrektionaler Datenbindung (_two-way data binding_). Logikbausteine (Schleifen zur Darstellung von Listen und Bedingungen für das konditionale Ein- und Ausblenden von UI-Elementen) werden in den Templates (HTML) der Komponenten definiert. Die Templates werden vom Framework in die eigentliche Benutzeroberfläche übersetzt. Komponenten können auch **Props** (Eigenschaften) und **Events** (Ereignisse) verwenden, um Daten zwischen Eltern- und Kindkomponenten zu übergeben. Props sind schreibgeschützte Daten, die von der Elternkomponente an die Kindkomponente weitergegeben werden. Events sind benutzerdefinierte Ereignisse, die von der Kindkomponente ausgelöst werden, um die Elternkomponente über Änderungen zu informieren.

---

# Frontend-Entwicklung

## Ordnerstruktur

Die Ordnerstruktur einer typischen Frontend-Anwendung sieht in etwa so aus:

![Ordnerstruktur einer Svelte-Anwendung](image.png)

Der Ordner `.vscode` enthält Einstellungen für den VS-Code-Editor. Der Ordner `node_modules` enthält die Abhängigkeiten (*dependencies*) der Anwendung. Das sind jede Pakete, die bei der Entwicklung (*build time*) und/oder bei der Ausführung (*run time*) der Anwendung benötigt werden. Alle Abhängigkeiten sind in der Datei `package.json`. Informationen über die Anwendung selbst (Name, Version, Lizenz, etc.) und Skripte, die bestimmte Aufgaben automatisieren (z. B. Starten der Anwendung, Testen der Anwendung, Erstellen einer Produktionsversion der Anwendung). Der Ordner `public` enthält statische Dateien (z. B. Bilder, Fonts, Icons), die direkt vom Browser unter den jeweiligen Pfad geladen werden können.

![Unterstruktur des src-Ordners](image-1.png)

Der Ordner `src` enthält den Quellcode der Anwendung. Die Dateien `app.css` und `main.js` sind die Einstiegspunkte der Anwendung (in diesem Fall eine SPA). Sie werden vom Browser als erstes geladen, wenn die entsprechende Website aufgerufen wird. Die Datei `app.css` enthält die globalen CCS-Stile der Anwendung. Die Datei `App.svelte` ist die Hauptkomponente der Anwendung, die andere Komponenten importiert und in der Benutzeroberfläche anzeigt. Die Datei `main.js` ist der Einstiegspunkt für das JavaScript/TypeScript der Anwendung. Sie initialisiert die Anwendung in der `App.svelte` und bindet sie an das HTML-Dokument (`index.html` im Root-Ordner).    

Der Ordner `lib` enthält benutzerdefinierte Bibliotheken und Hilfsfunktionen, die in der Anwendung verwendet werden. Der Ordner `components` enthält die wiederverwendbaren Komponenten der Anwendung. Sie sind Bausteine der Benutzeroberfläche. Der Ordner `game` enthält die Logik für das Spiel. Die Datei `store.svelte.ts` enthält den Zustand (_state_) der Anwendung. D. h. sie speichert die Daten, die sich im Laufe der Zeit ändern können (z.B. Spielergebnisse, Einstellungen, etc.) und fungiert als zentrale Datenquelle - _single source of truth_ - .
 