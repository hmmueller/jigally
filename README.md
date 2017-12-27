## JIGally

Alles, was wir im JIG brauchen ... 

### Use-Cases

- Getränke zählen und abrechnen
- Rechnungen verwalten
- Veranstaltungen und Künstler verwalten

![Skizze](https://github.com/hmmueller/jigally/edit/master/IMG_20171227_144950_Usecases.jpg)

### Ideen & Gedanken

- Alle Arten von Objekten sollten über CSV+Excel verändert werden können; Identifikation erfolgt über definierte Spalten heuristisch, mit optionaler "NEU/VORHANDEN/LÖSCHEN"-Spalte; Rückmeldung über Rückgabe Excels mtt Fehlereinträgen - bei Fehlern immer Rollback.
- ORM: "home-grown object registry", das nur "CREATE/UPDATE/DELETE" vermerkt; Assoc-Getter setzen dort "RETRIEVE" ab - auch Kinder; Composition-Assocs müssen "cascading-intelligent" sein für löschen & register; SQL hinter Abstraktion = es gibt auch simples InMemory-Registry;
- Fehler in Transaktion macht immer Rollback.
- Retrieve kann mit Optimistic- oder Pessimistic-Lock passieren, Lock ist auch später in Transaktion möglich; Pessimistic-Lock setzt (in eigener Transaktion) Lease (Zeit+Account).
- Jede Operation wird als Webservice angeboten = HTML-Frontend ist Client des Webservices.

### Architektur

- **Java-Software**
- **Web-Applikation** - Mitglieder tun was an Browsern auf Handys (_warum nicht Apps? ... nunja: Warum Apps?_)
- Let's use [DropWizard](http://www.dropwizard.io/1.2.2/docs/getting-started.html)

### Klassenmodell

![Skizze](https://github.com/hmmueller/jigally/edit/master/IMG_20171227_144935_Klassenmodell.jpg)


## Hilfe für Editieren

[Edit dieser Seite](https://github.com/hmmueller/jigally/edit/master/README.md)

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/hmmueller/jigally/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
