---
---
# Wie definiere ich Preise ?

## �bersicht
Um einen Partnerspezifischen Preis f�r einen Artikel zu definieren ben�tigst Du mindestens:

1. Ein Preissystem
1. Eine Preisliste
1. Eine Preislistenversion 
1. Einen Preisdatensatz
1. Das Preissystem muss dem Partner zugeordnet sein

![Preise](../_images/de_drawing_preissystem_hierachie.png)

## Schritte

1. **Preissystem anlegen**
	1. [Fenster "Preise" �ffnen](Howto_DE_Wie_finde_und_�ffne_ich_ein_Fenster.md) 
	1. [Neuen Datensatz anlegen](Howto_DE_Wie_lege_ich_einen_neuen_datensatz_an.md)
	1. Feld **Name** ausf�llen
	1. [Speichern](Howto_DE_Wie_lege_ich_einen_neuen_datensatz_an.md)
1. **Preisliste anlegen**
	1. Register "Preisliste" �ffnen 
	1. [Neuen Datensatz anlegen](Howto_DE_Wie_lege_ich_einen_neuen_datensatz_an.md) 
	1. Feld **Name** ausf�llen 
	1. Feld **Land**: Das Land muss mit dem Land Liefer- und Rechnungsadresse des Partners �bereinstimmen.
	1. Feld **Preise inkl. Steuern**: Steuert ob die Preise inklusive Mehrwertsteuer (Brutto) oder exklusive (netto) zu verstehen sind. metasfresh rechnet dem entsprechend die Steuer entweder aus dem Preis oder auf den Preis.
	1. Feld **Verkaufspreisliste**: Steuert ob diese Preisliste f�r den Verkauf verwendet werden soll.
	1. [Speichern](Howto_DE_Wie_lege_ich_einen_neuen_datensatz_an.md) 
1. **Preissystem anlegen**
	1. Register "Preislistenversion" �ffnen 
	1. [Neuen Datensatz anlegen](Howto_DE_Wie_lege_ich_einen_neuen_datensatz_an.md)
	1. Feld **Name** ausf�llen
	1. Feld **g�ltig ab** bestimmt ab wann diese Version g�ltig ist. Das Datum kann in der Vergangenheit liegen falls die Version sofort gelten soll oder auch in der Zukunft falls die Preise erst ab einem bestimmten Datum verwendet werden sollen. metasfresh holt sich anhand des zugesagten Datum in Auftrag oder Bestellung die Preise von der jeweiligen Preislistenversion mit dem passenden g�ltig ab Datum.
	1. [Speichern](Howto_DE_Wie_lege_ich_einen_neuen_datensatz_an.md)
1. **Preis anlegen**
	1. Register "Produkt-Preis" �ffnen 
	1. [Neuen Datensatz anlegen](Howto_DE_Wie_lege_ich_einen_neuen_datensatz_an.md)
	1. Feld **Produkt** ausf�llen
	1. Feld **Steuerkategorie** enth�lt die jeweilige Mehrwertsteuerkategorie wie z.B. Normal, Reduziert, Steuerfrei enthalten.
	1. Feld **Auszeichnunspreis** dient nur zur Anzeige des Listenpreises auf Belegen
	1. Feld **Standardpreis** ist der Preis der effektiv gilt.
	1. Feld **Limitpreis** darf durch eine manuelle Preis�nderung nicht unterschritten werden.
	1. Feld **Ma�einheit** ist die Preiseinheit und nicht zu verwechseln mit der Ma�einheit des Artikels f�r die Bestandsf�hrung.
	1. [Speichern](Howto_DE_Wie_lege_ich_einen_neuen_datensatz_an.md)
1. **Preissystem dem Partner zuordnen**
	1. [Fenster "Gesch�ftspartner" �ffnen](Howto_DE_Wie_finde_und_�ffne_ich_ein_Fenster.md) 
	* **Fall Kunde**
		1. Register "Kunde" �ffnen
		1. Feld **Preissystem**
			1. rechte Maustaste auf das Feld klicken und "aktualisieren" klicken
			1. das zuvor erstellte Preissystem ausw�hlen
	* **Fall Lieferant**
		1. Register "Lieferant" �ffnen
		1. Feld **Preissystem**
			1. rechte Maustaste auf das Feld klicken und "aktualisieren" klicken
			1. das zuvor erstellte Preissystem ausw�hlen
		
## H�ufige Fragen
**Frage:** Warum taucht das von mir erstellte Preissystem nicht im Fenster Gesch�ftsparnter auf?

**Antwort**: Taucht das Preissystem nicht auf bitte das Feld **Verkaufspreisliste** in der Preisliste �berpr�fen.
Au�erdem �berpr�fe ob Du das Feld mit **rechte Maustaste => aktualisieren** neu geladen hast.
