# vorschaubilder.analyse
Projekt um die Erzeugung von Vorschaubildern (Facebook, Google, etc) zu analyiseren

Die Techniken der einzelnen Plattformen benutzen folgende Buzzwords:

* Facebook: Open Graph-Markup
* Google: Google (Rich) Snippet Vorschau für SERP
* Twitter: Twitter Card


Zur Testseite für Vorschaubilder Verlinkungen: https://funthomas424242.github.io/vorschaubilder.analyse/

## Analyseergebnisse

### Metadaten
Die wichtigste Komponente scheint die Anreicherung der Webseite mit Metadaten zu sein. Wer hier Open Graph Markup verwendet scheint sehr viele Zielplattformen und Message Dienste zu erreichen. Wichtigste Infos die im Head einer Webseite untergebracht werden müssen, sind:

~~~~
  <title>Überschrift des Vorschaubildes</title>
  <meta name="description" content="Beschreibung des Vorschaubildes">
  <link rel="canonical" href="kanonische url - üblicherweise der seo link" />

  <meta property="og:url"                content="kanonische url - üblicherweise der seo link" />
  <meta property="og:type"               content="article" />
  <meta property="og:title"              content="Überschrift des Vorschaubildes" />
  <meta property="og:description"        content="Beschreibung des Vorschaubildes" />
  <meta property="og:image"              content="url des Vorschaubildes" />
  
  <meta name="twitter:card" content="summary">
  <meta name="twitter:title" content="Überschrift des Vorschaubildes">
  <meta name="twitter:url" content="kanonische ulr - üblicherweise der seo link">
  <meta name="twitter:description" content="Beschreibung des Vorschaubildes">
  <meta name="twitter:image" content="url des Vorschaubildes">
~~~~

### Bild Anforderungen

* Für Facebook kann es gar nicht groß genug sein
* Twitter scheint nur Bilder bis zu einer Größe von 800x400 zu unterstützen
* Hochformate scheinen nicht immer unterstützt zu werden (z.B. Twitter)


## Internetquellen

* Rechtliche Aspekte: https://drschwenke.de/vorschaubilder-beim-teilen-von-inhalten-in-social-media-praxistipps-zur-minderung-des-abmahnrisikos/
* Techniken für Vorschaubilder: https://medienkompass.de/facebook-vorschau-link-bild/
* Übergreifende Techniken: http://www.community1x1.de/google-facebook-link-vorschau/

## Verbreitete APIs
### GraphQL (Facebook, Instagram, Whatsapp, ...) 
#### Konzept und Spezifikation
Wird von Sharing Diensten oder auch Teilen Buttons genutzt um Artikelvorschauen zu erzeugen. 
* Open Graph-Markup: https://developers.facebook.com/docs/sharing/webmasters#markup
* https://developers.facebook.com/docs/sharing/3d-posts/open-graph-sharing

#### API & Tools 

* Facebook Crawler: https://developers.facebook.com/docs/sharing/webmasters/crawler
* Facebook Debugger: https://developers.facebook.com/tools/debug/ 
* Facebook Objekt Debugger: https://developers.facebook.com/tools/debug/og/object

### Instant Artikel API (Facebook, Instagram, ...)
#### Konzept uns Spezifikation
Dient Autoren, ihre Artikel schnell auf Facebook & Co. zu veröffentlichen

* https://developers.facebook.com/docs/instant-articles
* https://developers.facebook.com/docs/instant-articles/api

### Google (Rich) Snippets https://de.ryte.com/wiki/Rich_Snippets

#### Konzepte

https://www.gruenderszene.de/allgemein/rich-snippets-website-traffic

* Mikrodaten
* Mikroformate
* RDFa
* JSON-LD

#### Tools

* Snippet Tester: https://search.google.com/structured-data/testing-tool
* Snippet Generator https://seorch.de/html/snippet-optimization-tool.html

## Technische Erklärungen
 * PPI (Digitalbild) vs. DPI (Drucktechnik):https://fotovideotec.de/ppi_und_dpi/
