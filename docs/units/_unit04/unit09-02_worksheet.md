---
title: Lerneinheit 2 - Warm Up QGIS
toc: true
header:
  image: /assets/images/01-splash.jpg
  image_description: "John Snows "
  caption: "Map: [**Dr. John Snow**](https://de.wikipedia.org/wiki/John_Snow_(Mediziner)) [Wellcome Library via wikimedia](https://w.wiki/QtV)"
---
Der Einstieg in ein komplexe Software ist mühsam. Es ist sinnvoll Analog-Wissen aufzubauen und sich den Zugang logisch-strukturiert und nicht durch *auswendig lernen* der einzelnen Arbeitsschritte zu **erarbeiten**. Das ist nicht geschenkt zumal GIS Softwarepakete zu den komplexesten Konstrukten überhaupt gehören.
<!--more-->
Zur Mühsal des Erlernens einer neuen Graphischen Nutzer Schnittstelle (GUI) kommt noch die konzeptuellen und IT-verknüpften Probleme hinzu. Deshalb fangen wir Schritt für Schritt an. 

## Lernziele 

Nach dieser Übung können Sie:

  *  eine QGIS Projektdatei mit sinnvollen Einstellungen anlegen
  *  Datenformate und Datenmodelle unterscheiden und sowohl Raster- als auch Vektordatensätze in QGIS öffnen
  *  Projektionen kontrollieren, korrekt definieren und falls notwendig vereinheitlichen



## Benötigte Materialien

* Daten:
  * [Marburg Luftbild](https://raw.githubusercontent.com/GeoMOER/moer-bsc-geoinfo-basic/master/docs/assets/data/marburg_RE.tif)
  * [Open Streetmap Daten](https://raw.githubusercontent.com/GeoMOER/moer-bsc-geoinfo-basic/master/docs/assets/data/mr_nat.zip)
  * [Open Streetmap Daten](https://raw.githubusercontent.com/GeoMOER/moer-bsc-geoinfo-basic/master/docs/assets/data/mr_roads.shp)
  * [Attributtabelle](https://raw.githubusercontent.com/GeoMOER/moer-bsc-geoinfo-basic/master/docs/assets/data/mr_objects.xls)




## Aufgabe 02-01

Dieses Arbeitsblatt dient der Einführung in die verschiedenen Datenmodelle im GIS. Zudem lernen Sie, wie Sie eigene Raumdaten ins GIS importieren oder auch selbst im GIS erstellen können. 


  * Laden Sie die Datei `mr_RE.tif` in ein zuvor neu angelegtes `QGIS` Projekt. 
     * Informieren Sie sich über die Eigenschaften des Datensatzes. (Projektion, Datenmodell, Werte).
  *  Laden Sie sich von http://download.geofabrik.de/ den Datensatz von Hessen herunter und laden Sie das *Shapefile* `points` in Ihr QGIS Projekt.
    * Informieren Sie sich auch bei diesem Datensatz über die Eigenschaften. (Projektion, Datenmodell, Werte).
    * Beschneiden Sie den `points` Datensatz auf den Ausschnitt von Marburg. 
  * Importieren Sie die Tabelle `mr_objects.xls` in QGIS. Erstellen Sie einen räumlichen Layer aus der Tabelle.
  * Erstellen Sie auf Grundlage der Rasterdatei: Drei beliebige Flächen (Polygone), drei beliebige Straßen (Linienzüge) und ergänzen Sie schließlich den Layer `points` um 3 Positionen (Punkte) Ihrer Wahl. Geben Sie bei den neu erstellten Datensätzen als Koordinatensystem WGS 84 an. Tipp: Sie können zur besseren Orientierung auch eine Webkarte in Ihr Projekt laden.
{: .notice--success}




## Aufgabe 02-02 

Leider können wir Sie nicht vollständig an dem Thema der korrekten Verortung von Geodatensätzen - also der adäquaten Projektion- vorbei manövrieren. Im Rahmen der Aufgabe 02-01 haben Sie Raster- und Vektordaten in QGIS importiert sowie eigene Vektordaten erstellt. Die räumliche Information der Daten lag jeweils in geographischen Koordinaten vor. Die von Ihnen benutzte Software benutzt immer eine Echtzeitprojektion um diese Kugelkoordinaten auf den flachen Monitor zu projizieren. Wenn Sie weiter denken müssen jedoch echte kartographische Darstellungen korrekt projiziert werden und viele räumliche Analysen und geometrische Berechnungen funktionieren nur auf korrekt projizierten Daten.

Für den Beginn können wir Ihnen nur sehr deutlich raten das CRS (Coordinate Reference System) bzw KBS (Koordinatenbezugssystem) ihres *Projekts* identisch mit dem KBS einer jeden Datenebene zu halten. So kann sehr einfach einer der häufigsten Alltagsfehler vermieden werden.

* Erstellen Sie ein neues QGIS Projekt. Laden Sie als erstes die Rasterdatei `marburg_RE.tif` und dann im Anschluss die Vektordaten `mr_roads` und `mr_nat` ein.
  * Welche Projektionen besitzen die einzelnen Datensätze?
  * In welcher Projektion werden die Daten angezeigt? 
  * Wo können Sie die Projektion definieren, die zur Darstellung der Daten verwendet werden soll?
  * Was versteht man unter einer *on the fly* bzw. *Echtzeit* Projizierung und wie steht das in Zusammenhang mit den vorrausgehenden Fragen?
* Weisen Sie dem Layer `mr_nat` das geographische Referenzsystem `WGS 84` zu. 
  * Projizieren Sie anschließend alle Datensätze in ETRS89 UTM 32 
  * Warum können Sie dem Layer `mr_nat` die Projektion ETRS89 UTM 32 nicht direkt zuweisen
  * Haben Sie einen Weg gefunden diesen Datensatz gemäß der Anweisung korrekt zu projizieren? Wenn ja welchen?
{: .notice--success}

## Hilfestellungen

Als konkreten Einstieg für die Bearbeitung von Aufgabe 02 möchten wir Ihnen noch einige Einstiegshilfen für QGIS anbieten. QGIS ist ein sehr komplexes Softwareprodukt das nicht nur in den unterschiedlichsten Versionen  auf allen gängigen OS-Plattformen verfügbar ist sondern zusätzlich vollständig individuell anpassbar ist. Daher kursieren aus den vergangenen 15 Jahren eine Vielzahl von Hilfen, Handbüchern und Tutorials - nicht jedes ist geeignet und erst recht nicht jedes passt auf Ihre Version.

Ein erster Anlaufpunkt für konkrete Informationen stellt die integrierte Hilfe des Softwarepakets dar. Darüber hinaus ist eine umfangreiche Dokumentation verfügbar. Die jeweils aktuelle [QGIS Landing Page](https://www.qgis.org/de/site/forusers/index.html) ist der zentrale Zugang zu allen offiziell vom Projekt verfügbar gemachten Dokumentationen. Bei allen Seiten gilt achten Sie darauf die Hilfe zu Ihrer passenden QGIS Version anzuschauen.


### Einrichtung eines QGIS-Projekts 

Neben den jeweils aufgaben-spezifischen Einstellungen ist es auf Uni- bzw. Rechnern mit einem Heimatverzeichnis in der Cloud /im Netz  sehr sinnvoll die Daten lokal vorzuhalten. Hierfür müssen Sie zunächst eine Ordnerstruktur für Ihr Projekt anlegen. Bitte achten sie darauf keine Sonderzeichen Umlaute oder Leerzeichen zu verwenden. Hilfe zur Projektdatei finden sie unter [Arbeiten mit Projektdateien](https://docs.qgis.org/3.10/de/docs/user_manual/introduction/project_files.html).

### Digitalisieren von Geometriedaten

Die manuelle Erzeugung von Vektordaten wird allgemein als *digitalisieren* bezeichnet. Dabei erzeugen Sie auf z.B. Grundlage von Rasterbilddateien wie Satellitenbildszenen, Luftbildern, thematischen und topographischen Karten, einfachen Screenshots oder anderen Vorlagen Ihre eigenen vektorbasierten Datensätze. Schauen Sie sich dazu die QGIS Hilfe zur  [Digitalisierung](https://docs.qgis.org/3.10/de/docs/user_manual/working_with_vector/editing_geometry_attributes.html) an. Ein ausführliches Anwendungsbeispiel finden Sie unter [Digitizing Forest Stands](https://docs.qgis.org/3.10/en/docs/training_manual/forestry/stands_digitazing.html)

###  Tabellen in QGIS importieren
Der Import von Tabellen beinhaltet eine Vielzahl von Fallstricken. Ganz generell nutzen Tabellendaten in QGIS nur dann etwas wenn sie entweder selbst Koordinaten (also geographische Informationen) enthalten oder aber einen Schlüssel wie z.B eine ID die bereits existierenden Geometriedaten zuzuordnen ist. Generell können Sie aber folgendem Schema folgen:
[Import von Tabellenblättern oder CSV-Dateien](http://www.qgistutorials.com/de/docs/3/importing_spreadsheets_csv.html)
