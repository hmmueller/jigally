## JIGally

Alles, was wir im JIG brauchen ... 

### Use-Cases

- Getränke zählen und abrechnen
- Rechnungen verwalten
- Veranstaltungen und Künstler verwalten
- "Künstler" is a "Lieferant"?
- ics-Schnittstelle?
- Statistiken: Wieviel X pro Person wird auf Veranstaltungen der Art Y getrunken? (für Planung)

![Skizze](https://github.com/hmmueller/jigally/blob/master/IMG_20171227_144950_Usecases.jpg)

### Ideen & Gedanken

- Alle Arten von Objekten sollten über CSV+Excel verändert werden können; Identifikation erfolgt über definierte Spalten heuristisch, mit optionaler "NEU/VORHANDEN/LÖSCHEN"-Spalte; Rückmeldung über Rückgabe Excels mtt Fehlereinträgen - bei Fehlern immer Rollback.
- Jede Operation wird als Webservice angeboten = HTML-Frontend ist Client des Webservices. Allerdings kann das Frontend "Wizards" anbieten, die erst nach einer Sequenz von GUI-Bedienungen eine Transaktion auslösen ... dann ist aber das Frontend für den State zuständig.
- Account-Tracking bei Aktionen - fachlich (mit expliziten semantischen Assoziationen) oder technisch (Trigger für jede Änderung)? Sinnvoller scheint mir erstes - zu klären.

### Architektur

- **Java-Software**
- **Web-Applikation** - Mitglieder tun was an Browsern auf Handys (_warum nicht Apps? ... nunja: Warum Apps?_)
- Let's use [DropWizard](http://www.dropwizard.io/1.2.2/docs/getting-started.html)
- [Architektur & Entwicklung](https://github.com/hmmueller/jigally/blob/master/ArchitekturUndEntwicklung.md)

### Klassenmodell

![Skizze](https://github.com/hmmueller/jigally/blob/master/IMG_20171227_144935_Klassenmodell.jpg)


## Hilfe für Editieren

[Edit dieser Seite](https://github.com/hmmueller/jigally/edit/master/README.md)

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/hmmueller/jigally/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
