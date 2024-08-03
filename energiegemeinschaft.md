# Lokal versus Regional

Eine Energiegemeinschaft (EEG) kann sich auf lokaler oder regionaler Ebene organisieren. Der Hauptunterschied zwischen beiden Formen liegt in der Netzebene und der Verbindung zwischen den Teilnehmern. In dieser Übersicht beschränken wir uns ausschließlich auf Netzebene 7: Lokales Niederspannungsnetz (0,4 kV bis 1 kV).

<img src="./_media/NahbereichDefinition.svg" alt="Nahbereich - Definition">

## Lokale Energiegemeinschaft

- Die Teilnehmer sind über einen gemeinsamen Transformatorstation (Trafo) verbunden.
- Die Erzeugungsanlage und die Teilnehmer sind über das Niederspannungs-Ortsnetz dieser Trafostation verbunden.
- Keine fremden oder höheren Netzebenen sind involviert.

> Note: **Vorteile:** A) Höhere Netzkostenersparnisse (bis 57%), B) Einfachere Organisation und Verwaltung, C) Lokale Autarkie und regionale Wertschöpfung

> [!TIP|label:Hinweis]
> An alert of type 'note' using global style 'callout'.

## Regionale Energiegemeinschaft

- Die Teilnehmer sind über dasselbe Umspannwerk miteinander verbunden.
- Es werden regionale Mittelspannungsleitungen benötigt, um die Erzeugungsanlage und die Teilnehmer miteinander zu verbinden.
- Die Energiegemeinschaft übersteigt den Bereich einer Trafostation und umfasst mehrere Netzebenen.

```bash
docsify init ./docs
```

## Inhalt schreiben

Nachdem der Befehl `init` vollständig ausgeführt wurde, kannst du folgende Dateien im Unterordner `./docs` finden:

* `index.html` als zentrale Datei
* `README.md` als die Startseite für die Dokumentation
* `.nojekyll` verhindert, dass Github Pages Dateien ignoriert, die mit einem Unterstrich beginnen.

Du kannst die Dokumentation über die Datei `./docs/README.md` nach Belieben ändern, und natürlich [weitere Seiten](de-de/more-pages.md) hinzufügen.

## Vorschau der eigenen Seiten

Du kannst einen lokalen Server mit dem Befehl `docsify serve` laufen lassen, und auf eine Vorschau deiner Webseite über `http://localhost:3000` zugreifen.

```bash
docsify serve docs
```

?> Für weitere Informationen hinsichtlich der Verwendung von `docsify-cli`, siehe [docsify-cli Dokumentation](https://github.com/docsifyjs/docsify-cli).

## Manuelle Inbetriebnahme

Wenn du `npm` nicht verwenden möchtest, oder Probleme bei der Installation des Tools hast, kannst du auch manuell die Datei namens `index.html` erstellen:

```html
<!-- index.html -->

<!DOCTYPE html>
<html>
<head>
  <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <meta charset="UTF-8">
  <link rel="stylesheet" href="//unpkg.com/docsify/themes/vue.css">
</head>
<body>
  <div id="app"></div>
  <script>
    window.$docsify = {
      //...
    }
  </script>
  <script src="//unpkg.com/docsify/lib/docsify.min.js"></script>
</body>
</html>
```

Solltest du Python installiert haben, kannst du einen statischen Server laufen lassen, um eine Vorschau deiner Webseite anzuschauen:

```bash
cd docs && python -m SimpleHTTPServer 3000
```

## Ladedialog

Wenn du möchtest, kann **docsify** einen Ladedialog anzeigen, während es deine Dokumentation umwandelt:

```html
  <!-- index.html -->

  <div id="app">Please wait...</div>
```

Du solltest das `data-app` Attribut anpassen, wenn du `el` geändert hast:

```html
  <!-- index.html -->

  <div data-app id="main">Please wait...</div>

  <script>
    window.$docsify = {
      el: '#main'
    }
  </script>
```

Vergleiche [el Einstellungen](configuration.md#el).
