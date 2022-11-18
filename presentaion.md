# Service Cutter


## Anwenungsfall

Recycleing Company


## Entities

- Kunde
- Geraet
- Preisangebot
- Bewertung


## UseCases

- Angebot wird erstellt
- ....

## Auswahl der Kriterien

Gewichtung wird von 0-10 vergeben. Je nach Kriterium unterscheiden sich aber die Werte. Es gibt welche (zB Storage Similarity) bei denen 3 für "Mittel" steht.


### Identity & Lifecycle Commonality

#### Bewertung
Kunden, Geräte, Preisangebot und Bewertung teilen sich keinen Lebenszyklus.
- Kunde ist unabhängig vom Gerät
- Gerät kann vor einem Preisangebot bestehen
- Bewertung ist unabhängig von allem. Es soll glaub ich ein Bewertungskriterium darstellen. ?


### Semantic Proximity

#### Bedeutung
Zwei Nanoentitäten sind bespielsweise semantic proximated, wenn in einem Usecase auf beide zugegriffen wird.

#### Bewertung
Nanoentitäten von:
- Gerät und von Preisangebot oder
- Preisangebot und Bewertung oder
- Kunde und Gerät


### Shared Owner

#### Bedeutung
Personen, Rollen, Organisationseinheiten sind für eine Gruppe von Nanoentitäten verantwortlich. Diese sollten nicht gemischt werden.

#### Bewertung
- Vielleicht pflegt eine Gruppe Gerätetypen und erstellt entsprechende Bewertungskrterien. Diese Gruppe spielt bestimmt auch bei der Angebotserstellung mit.
- Dann gibt es noch eine Gruppe, die Kunden verwaltet und die Zahlungen veranlasst, wenn ein Angebot angenommen wurde.


### Structural Volatility

#### Bedeutung
Wie oft change requests implementiert werden, die die Nanoentitäten beeinflussen.

#### Bewertung
keine Ahnung was wohl oft angefasst wird. Vllt der Preisbildungsalgorithmus?


### Latency

#### Bedeutung
High performance Nanoentities..

#### Bewertung
Produktsuche, wenn der Kunde nach dem entsprechenden gerät sucht. Die Preisberechnung kann ruhig länger dauern.


### Consistency Criticality

#### Bedeutung
Wie kritisch ist es das Daten konsistent sind?

#### Bewertung
Preisangebote und sämtliche Zahlungsangelegenheiten sollten unbedingt konsistent sein.


### Availability Criticality

#### Bewertung
Selbes wie bei Latency. (Produktsuche, wenn der Kunde nach dem entsprechenden gerät sucht. Die Preisberechnung kann ruhig länger dauern.)


### Content Volatility

#### Bedeutung
Nanoentities die sich häufig ändern und solche die sich nur selten ändern, sollten ggf in unterschiedlichen Storages untergebracht werden.

#### Bewertung
- Bewertungskriterien sehr selten
- Kundendaten eher selten
- Preisangebote & Geräte häufiger
- Wenn preisangebote nach einer gewissen Zeit verfallen oder geblockt werden oder sich ändern, oft


### Consistency Constraint

#### Bedeutung
Eine Gruppe von Nanoentities soll konsistent mit einander sein.

#### Bewertung
- Presiangebot und Rechnungsbetrag


### Storage Similarity

#### Bedeutung
Für einige Nanoentitäten wird uU viel mehr speicherplatz benötigt. (Nicht sich ob es so gemeint ist)

#### Bewertung
Sieht alles eher nach geringem Speicherbedarf aus. Ggf Kundenbilder, die zu den eingestellten Produkten gehören nehmen viel Speicherbedarf.


### Predefined Service Constraint

#### Bedeutung
Einige Nanoentitäten sollten ggf unbedingt in einem bestimmten Service liegen. ZB aus technologischen oder legacy Günden.

#### Bewertung
nope


### Security Contextuality

#### Bedeutung
Eine Rolle, die Berechtigung zum Zugriff auf eine Gruppe von Nanoentities hat, vereint diese ggf zu einem Service, um Berechtigungsprobleme zu vermeiden.

#### Bewertung
zB
- Kundendaten, Rechnungsdetails
- Bewertungskreíterien und Angbotserstellung


### Security Criticality

#### Bedeutung
Wie daramtisch ist der Datenverlust einer Gruppe von Nanoentities?

#### Bewertung
- Bewertungskriterien, die die Preisbildung beeinflussen: super wichtig.
- Kundendaten, Rechnungsdaten, Preisangebote: wichtig.
- Produktbilder: eher unwichtig


### Security Constraint

#### Bedeutung
.... hab ich nicht verstanden.