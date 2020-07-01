---
title: Lerneinheit 4 - Analysen
toc: true
header:
  image: /assets/images/01-splash.jpg
  image_description: "John Snows "
  caption: "Map: [**Dr. John Snow**](https://de.wikipedia.org/wiki/John_Snow_(Mediziner)) [Wellcome Library via wikimedia](https://w.wiki/QtV)"

---
Neben den Lagebeziehungen stellen vor allem die Distanzbeziehungen quantitative Methoden zur Abgrenzung von im Raum ähnlichen Merkmalswerten oder auch der Schließung von Lücken fehlender räumlicher Information durch Interpolation zur Verfügung.


 <!--more-->

## Was wir in dieser Einheit vor haben


## Lernziele 

Nach dieser Übung können Sie:

  *  
  *  
  *  


## Benötigte Materialien

* Daten:
  * [SRTM Geländemodell](http://srtm.csi.cgiar.org/SELECTION/inputCoord.asp)




## Aufgabe 04-01


*   Laden Sie sich unter der obigen Adresse die passende Kachel (Ausschnitt) des SRTM Geländemodell von Marburg herunter. 
*   Was zeigt Ihnen der Datensatz?
*   Projizieren Sie das Geländemodell in ETRS89 UTM32 und schneiden es auf den Marburg Ausschnitt zu.
*   Berechnen Sie auf der Grundlage des Geländemodells von wo aus die E-Kirche sichtbar ist.
*   Berechnen Sie die Hangneigung, Exposition und Abflussrichtung. 
*   Extrahieren Sie für den Marktplatz (Brunnen) diese Werte.
*   Wenden Sie einen 5*5 Mittelwertsfilter auf die Geländehöhe an. Beschreiben Sie das Resultat in ein bis zwei Sätzen. 
*   Berechnen Sie, die minimale, maximale und mittlere Hangneigung in städtischem Gebiet (Verwaltungsgrenze). 
{: .notice--success}

## Hilfestellung 

*  Verwenden Sie zum Ausschneiden des Rasters einen der Marburg-Layer aus den vorherigen Sitzungen als Vorlage.
*  Das Stichwort für die QGIS Hilfe zum Mittelwertsfilter ist "Focal Statistics", zur Sichtbarkeitsanalyse können sie das Plugin "Visibility Analysys" installieren. Es wird unter den Verarbeitungswerkzeugen angezeigt.
  * Zu Aufgabe 6.6: Gehen Sie zur Lösung wie folgt vor:
      * Reklassifizieren Sie die Corine Daten, sodass Stadt den Wert 1 hat und alle anderen Pixel "NoData"
      * Konvertieren Sie das Raster zu einem Polygondatensatz
      * Verwenden Sie zonale Statistiken um sich die min/max/mittel Werte als Tabelle auszugeben 

