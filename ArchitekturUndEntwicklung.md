# Alle möglichen Themen zu Architektur & Entwicklung

## Passwort-Sicherheit

https://security.stackexchange.com/questions/4781/do-any-security-experts-recommend-bcrypt-for-password-storage

## ORM

- "home-grown object registry", das nur "CREATE/UPDATE/DELETE" vermerkt; Assoc-Getter setzen dort "RETRIEVE" ab - auch Kinder; Composition-Assocs müssen "cascading-intelligent" sein für löschen & register; SQL hinter Abstraktion = es gibt auch simples InMemory-Registry;
- Fehler in Transaktion macht immer Rollback.
- Retrieve kann mit Optimistic- oder Pessimistic-Lock passieren, Lock ist auch später in Transaktion möglich; Pessimistic-Lock setzt (in eigener Transaktion) Lease (Zeit+Account).

## Serviceaufteilung?

Prinzipiell wäre eine Aufteilung in "Funktionsblöcke" wohl möglich (alles um Account+Person; alles um Veranstaltungen; alles um Rechnungen; alles um Produkte) - bis hin zu MicroServices = getrennten Webservern. Bei dieser Minimalanwendung (kleine Datenmenge = max. einige 1000 Records, kleine Benutzeranzahl = max. einige Dutzen, vielleicht 100e) ist das aber unnötig und hätte nur einen "Lerneffekt" -> ersparen wir uns ...

## Mögliches Hosting:

- https://www.hetzner.de/virtual-server    4,64/Monat
- https://www.df.eu/de/cloud-hosting/     14,99/Monat, aber abschaltbar
- https://www.keyweb.de/de/produkte/server/root-virtual-server       4,90/Monat

## Eclipse 

Eclipse mit Maven und DropWizard zum Gehen bringen:

1. [How to solve No compiler is provided in this environment while running Maven build](http://learn-automation.com/maven-no-compiler-is-provided-in-this-environment-selenium/)
1. In Eclipse ein Java-Projekt anlegen ("Hello world").
  * Right-Click auf Projekt -> Convert to Maven (... es entsteht pom.xml)
  * Compilieren und Laufen lassen - getrennt unter "Run Configuration"
3. _Archive for required library: '.../.m2/repository/com/google/guava/guava/23.1-jre/guava-23.1-jre.jar' in project 'JIGally' cannot be read or is not a valid ZIP file	JIGally_ -> C:/Users/h.mueller/.m2/repository/... löschen, wird von Maven neu heruntergeladen.

## Edit

[Edit dieser Seite](https://github.com/hmmueller/jigally/edit/master/ArchitekturUndEntwicklung.md)
