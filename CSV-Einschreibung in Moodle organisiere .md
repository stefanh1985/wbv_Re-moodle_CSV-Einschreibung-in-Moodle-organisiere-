<!--
author: Stefan Hierholzer
email:
version: 1.0
language: de
narrator: German Male

comment: Selbstlernkurs Kohorten und CSV-Einschreibung in Moodle.
         Für Moodle-Administrator:innen, Bereichsverantwortliche und Sekretariat an Fachschulen für Sozialwesen,
         Berufsschulen und außerschulischen Bildungsorganisationen. DQR Niveau 6.

logo: kohorten_csv_moodle.png

import: https://raw.githubusercontent.com/LiaScript/docs/master/README.md

link: https://fonts.googleapis.com/css2?family=Source+Sans+Pro:wght@300;400;600&display=swap
-->

# Kohorten und CSV-Einschreibung in Moodle

> **Ein kompakter Selbstlernkurs für Admins, Bereichsverantwortliche und Sekretariat vor dem Schuljahresstart**

---

## 📋 Kursübersicht

| Angabe | Information |
|--------|-------------|
| **Thema** | Kohorten und CSV-Einschreibung in Moodle |
| **Anknüpfungspunkt** | Vor dem Schuljahresstart |
| **Zielgruppe** | Admins, Bereichsverantwortliche, Sekretariat |
| **Zeitaufwand** | ca. 45–60 Minuten |
| **Niveau** | DQR Stufe 6 |
| **Format** | Selbstlernkurs mit CSV-Mapping, Fehlersuche, Mini-Fallstudie und Upload-Simulation |
| **Benötigtes Material** | Muster-CSV, Rollenmatrix, Klassenlisten, Testinstanz |

---

## 🎯 Kompetenzorientierte Lernziele (DQR 6)

Nach Abschluss dieses Kurses sind Sie in der Lage:

**Wissen und Verstehen**

1. Kohorten, Nutzer:innenkonten, Kurse, Gruppen und Rollen funktional voneinander zu unterscheiden.
2. zu erklären, warum Kohortenpflege vor dem Schuljahresstart als wiederkehrender Serienprozess geplant werden muss.
3. zentrale CSV-Felder für Nutzer:innen- und Kohortenpflege fachlich korrekt zu deuten.

**Können – instrumentale und systemische Kompetenzen**

4. Klassenlisten in ein prüfbares CSV-Schema für Moodle zu übertragen.
5. typische Fehler in CSV-Dateien zu erkennen, zu begründen und vor dem Upload zu bereinigen.
6. einen sicheren Ablauf für Testupload, Voransicht, Korrektur und produktiven Import zu planen.

**Können – kommunikative und soziale Kompetenzen**

7. Zuständigkeiten zwischen Admins, Bereichsverantwortlichen und Sekretariat über eine Rollenmatrix zu klären.
8. datenschutzsensible Entscheidungen zur Nutzer:innenpflege nachvollziehbar zu dokumentieren.

---

## ⏱️ Zeitplanung

```ascii
Modul 0: Einstieg und Prozessblick                 5 min
Modul 1: Kohorten fachlich sauber einordnen       10 min
Modul 2: CSV-Datenmodell prüfen                   15 min
Modul 3: Upload-Simulation und Mapping            15 min
Modul 4: Fehlersuche und Mini-Fallstudie          10 min
Abschluss: Serienprozess für den Schuljahresstart 5 min
──────────────────────────────────────────────────────
Gesamt:                                      ca. 45–60 min
```

---

## Modul 0: Einstieg – Warum Kohortenpflege kein Nebenjob ist

### Ausgangspunkt

Vor dem Schuljahresstart müssen Nutzer:innenkonten, Klassenzugehörigkeiten und Kurszugänge zuverlässig vorbereitet werden. In kleinen Systemen kann vieles noch manuell gelöst werden. In größeren Fachschulen, Berufsschulen oder Bildungsorganisationen führt manuelle Einzelpflege schnell zu Fehlern: doppelte Konten, falsche Kurszugänge, fehlende Teilnehmende, veraltete Klassenzuordnungen oder unklare Zuständigkeiten.

Kohorten und CSV-Uploads sind deshalb kein rein technisches Thema. Sie bilden einen schulorganisatorischen Serienprozess ab: Daten werden aus Klassenlisten übernommen, fachlich geprüft, technisch formatiert, in einer Testinstanz kontrolliert und erst danach produktiv eingespielt.

> **📝 Merksatz**
>
> *Kohortenpflege ist Organisationsarbeit mit technischen Mitteln. Wer den Prozess nicht plant, produziert im System genau die Unordnung, die Moodle eigentlich reduzieren soll.*

---

> **💭 Reflexionsfrage 0.1 – Erste Bestandsaufnahme**
>
> Denken Sie an den letzten Schuljahresstart:
>
> - Wo entstanden die meisten Fehler bei Nutzer:innenkonten oder Kurszugängen?
> - Welche Daten kamen aus dem Sekretariat, welche aus den Bildungsgängen und welche aus der Administration?
> - Gab es eine Testphase vor dem produktiven Import?
>
> Notieren Sie zwei funktionierende Routinen und zwei Schwachstellen.

---

### ✅ Selbstüberprüfung Modul 0

Welche Aussage beschreibt den Zweck dieses Kurses am treffendsten?

- [( )] Der Kurs zeigt, wie alle Moodle-Kurse manuell mit Teilnehmenden befüllt werden.
- [(X)] Der Kurs unterstützt dabei, Nutzer:innen- und Kohortenpflege als wiederkehrenden Serienprozess sicher zu planen.
- [( )] Der Kurs ersetzt die technische Moodle-Administration vollständig.
- [( )] Der Kurs behandelt ausschließlich die Gestaltung von Kursseiten.

---

## Modul 1: Kohorten fachlich sauber einordnen

![Illustration Modul 1: Ein Admin, eine Bereichsverantwortliche und eine Person aus dem Sekretariat stehen vor einer Moodle-Tafel. Karten mit Nutzer:innen, Kohorten, Kursen, Gruppen und Rollen werden in eine klare Prozesslogik sortiert. Comic-Stil, sachlich und übersichtlich.](kohorten_csv_modul1.png "Modul 1 – Kohorten fachlich einordnen")

### 1.1 Die zentrale Unterscheidung

| Baustein | Funktion | Typische Leitfrage |
|----------|----------|--------------------|
| **Nutzer:innenkonto** | Individueller Zugang zu Moodle | Wer ist diese Person eindeutig im System? |
| **Kohorte** | Standortweite oder kursbereichsbezogene Sammlung von Nutzer:innen | Welche Personen gehören organisatorisch zusammen? |
| **Kurs** | Konkreter Lern-, Arbeits- oder Verwaltungsraum | Wo findet die Arbeit in Moodle statt? |
| **Gruppe** | Unterteilung innerhalb eines Kurses | Welche Teilgruppen brauchen im Kurs getrennte Ansichten oder Aktivitäten? |
| **Rolle** | Rechteprofil in einem Kontext | Wer darf in welchem Bereich was sehen, bearbeiten oder verwalten? |

Eine Kohorte ist keine Klasse im pädagogischen Sinn, sondern eine technische Sammlung von Nutzer:innen, die organisatorisch gemeinsam behandelt werden können. Gerade deshalb eignet sie sich für Klassen, Jahrgänge, Bildungsgänge, Kollegiumsgruppen oder Funktionsgruppen.

> **📝 Merksatz**
>
> *Kohorten bündeln Personen. Kurse organisieren Arbeit. Gruppen strukturieren Arbeit innerhalb eines Kurses. Rollen regeln Rechte.*

---

### 1.2 Sortieraufgabe: Was gehört wohin?

Ordnen Sie die folgenden Elemente dem passenden Baustein zu.

| Element | Passender Baustein |
|---------|--------------------|
| `fs24a` als technische Sammlung aller Studierenden einer Klasse | [[Kohorte]] |
| Lernfeldkurs „LF 2 – Pädagogische Beziehungen gestalten“ | [[Kurs]] |
| Person „m.mustermann“ mit eigener E-Mail-Adresse | [[Nutzer:innenkonto]] |
| Kleingruppe „Fallanalyse 1“ innerhalb eines Kurses | [[Gruppe]] |
| Bildungsgangleitung darf Kurse in einem Kursbereich anlegen | [[Rolle]] |
| Alle Lehrkräfte eines Bildungsgangs | [[Kohorte]] |
| Praxisreflexion im 3. Semester | [[Kurs]] |
| Korrekturteam innerhalb eines Prüfungsraums | [[Gruppe]] |

---

### 1.3 Rollenmatrix für den Serienprozess

| Prozessschritt | Sekretariat | Bereichsverantwortliche | Admins |
|----------------|-------------|--------------------------|--------|
| Klassenliste bereitstellen | verantwortlich | prüft fachliche Zuordnung | erhält geprüfte Datei |
| Bildungsgang und Kohortennamen prüfen | liefert Stammdaten | verantwortlich | berät bei Namenslogik |
| CSV technisch prüfen | arbeitet mit Vorlage | prüft Plausibilität | verantwortlich |
| Testupload durchführen | keine Produktivänderung | kontrolliert Ergebnis | verantwortlich |
| Produktivimport freigeben | bestätigt Datenstand | bestätigt fachliche Richtigkeit | führt Import durch |
| Nachkontrolle dokumentieren | meldet Korrekturen | prüft Stichprobe | dokumentiert Importergebnis |

> **💭 Reflexionsfrage 1.1 – Zuständigkeit klären**
>
> Welche Person oder Rolle darf bei Ihnen aktuell entscheiden, ob eine Klassenliste technisch importiert wird?
> Falls diese Entscheidung nicht eindeutig geregelt ist: Welche Risiken entstehen dadurch für Datenschutz, Kurszugang und Support?

---

### ✅ Selbstüberprüfung Modul 1

**Frage 1:** Welche Aussage ist fachlich korrekt?

- [( )] Eine Kohorte ist immer identisch mit einer Moodle-Gruppe.
- [(X)] Eine Kohorte bündelt Nutzer:innen, damit diese gemeinsam in Kurse eingebunden werden können.
- [( )] Eine Kohorte enthält direkt Lernmaterialien und Aktivitäten.
- [( )] Eine Kohorte ersetzt individuelle Nutzer:innenkonten.

---

**Frage 2:** Welche Aufgaben gehören vor allem in die fachliche Verantwortung der Bereichsverantwortlichen?

- [[X]] Prüfen, ob die richtige Klasse dem richtigen Bildungsgang zugeordnet ist.
- [[ ]] Serverupdates installieren.
- [[X]] Freigeben, ob die fachliche Zuordnung produktiv genutzt werden kann.
- [[ ]] Browsercache der Nutzer:innen löschen.
- [[X]] Rückmelden, wenn Kohortennamen organisatorisch missverständlich sind.

---

## Modul 2: CSV-Datenmodell prüfen

![Illustration Modul 2: Eine große CSV-Tabelle liegt auf einem Schreibtisch. Markierte Spalten wie username, firstname, lastname, email und cohort1 werden mit einer Moodle-Checkliste abgeglichen. Comic-Stil, klar und praxistauglich.](kohorten_csv_modul2.png "Modul 2 – CSV-Datenmodell prüfen")

### 2.1 CSV ist kein Excel-Problem, sondern ein Datenmodell

Eine CSV-Datei ist eine Textdatei mit Spaltenüberschriften und Datensätzen. Moodle erwartet für den Nutzer:innenimport eindeutige Feldnamen. Für einfache neue Nutzer:innenkonten sind die Felder `username`, `firstname`, `lastname` und `email` zentral. Weitere Felder, zum Beispiel `auth`, `idnumber`, `department`, `institution` oder `cohort1`, können den Prozess fachlich stabiler machen.

Bei der Kohortenpflege ist besonders wichtig: In `cohort1`, `cohort2` usw. wird die **Kohorten-ID** genutzt, nicht der frei formulierte Anzeigename. Wer Anzeigenamen und technische IDs nicht trennt, erzeugt schnell doppelte oder falsch benannte Kohorten.

> **📝 Merksatz**
>
> *Die Spaltenüberschrift ist in Moodle kein Dekor. Sie entscheidet, welche Aktion der Upload auslöst.*

---

### 2.2 Minimaldatei für neue Nutzer:innen

```csv
username,firstname,lastname,email
m.meyer,Marie,Meyer,marie.meyer@example.edu
j.schulz,Jonas,Schulz,jonas.schulz@example.edu
s.aksoy,Selin,Aksoy,selin.aksoy@example.edu
```

Diese Datei eignet sich nur für den Basisimport. Sie legt noch keine fachliche Zugehörigkeit fest.

---

### 2.3 Erweiterte Datei mit Kohortenzuordnung

```csv
username,firstname,lastname,email,auth,idnumber,department,cohort1
m.meyer,Marie,Meyer,marie.meyer@example.edu,manual,STU-2026-001,FS Sozialpädagogik,fs26a
j.schulz,Jonas,Schulz,jonas.schulz@example.edu,manual,STU-2026-002,FS Sozialpädagogik,fs26a
s.aksoy,Selin,Aksoy,selin.aksoy@example.edu,manual,STU-2026-003,FS Sozialpädagogik,fs26b
```

**Fachliche Lesart:**

| Feld | Bedeutung | Prüffrage |
|------|-----------|-----------|
| `username` | eindeutiger Loginname | Ist die Schreibweise stabil und schulweit eindeutig? |
| `firstname` | Vorname | Stimmen Sonderzeichen und Großschreibung? |
| `lastname` | Nachname | Stimmen Schreibweise und Reihenfolge? |
| `email` | E-Mail-Adresse | Ist die Adresse eindeutig und aktiv? |
| `auth` | Authentifizierungsmethode | Passt der Wert zur schulischen Login-Strategie? |
| `idnumber` | interne Kennung | Kann die Person damit später eindeutig abgeglichen werden? |
| `department` | Bereich oder Bildungsgang | Hilft das Feld bei Suche und Support? |
| `cohort1` | erste Kohortenzuordnung | Ist die Kohorten-ID vorhanden und exakt geschrieben? |

---

### 2.4 Datei für bestehende Nutzer:innen in vorhandene Kohorten

Wenn Nutzer:innenkonten bereits existieren, kann die Kohortenzuordnung schlanker erfolgen. Entscheidend ist, dass `username` und Kohorten-ID exakt stimmen.

```csv
username,cohort1,cohort2
m.meyer,fs26a,wpk_sexualpaedagogik_26
j.schulz,fs26a,
s.aksoy,fs26b,wpk_sexualpaedagogik_26
```

> **📝 Merksatz**
>
> *Für bestehende Nutzer:innen ist die Frage nicht: Welche Person wird neu angelegt? Sondern: Welche vorhandene Person wird welcher Kohorte eindeutig zugeordnet?*

---

### 2.5 CSV-Mapping-Aufgabe

Ordnen Sie die Spalten der passenden Funktion zu.

| CSV-Spalte | Funktion |
|------------|----------|
| `username` | [[Eindeutiger Loginname]] |
| `email` | [[Eindeutige Kontaktadresse]] |
| `cohort1` | [[Erste Kohortenzuordnung]] |
| `auth` | [[Authentifizierungsmethode]] |
| `idnumber` | [[Interne eindeutige Kennung]] |
| `suspended` | [[Konto sperren oder aktiv halten]] |
| `deleted` | [[Konto zur Löschung markieren]] |
| `course1` | [[Manuelle Kurseinschreibung per CSV]] |

---

### ✅ Selbstüberprüfung Modul 2

**Frage 1:** Welche Felder bilden eine tragfähige Minimaldatei für neue Nutzer:innenkonten?

- [( )] `name,email,course,group`
- [(X)] `username,firstname,lastname,email`
- [( )] `class,teacher,room,password`
- [( )] `cohort,role,category,visible`

---

**Frage 2:** Was ist bei `cohort1` besonders kritisch?

- [( )] Dort muss immer der Anzeigename der Klasse stehen.
- [(X)] Dort muss die Kohorten-ID exakt verwendet werden.
- [( )] Das Feld darf nur bei Lehrkräften genutzt werden.
- [( )] Das Feld ersetzt die E-Mail-Adresse.

---

**Frage 3:** Welche Aussagen sind richtig?

- [[X]] Eine CSV-Datei sollte vor dem Import in einem Texteditor geprüft werden.
- [[X]] Sonderzeichen, Trennzeichen und leere Pflichtfelder können Uploadfehler auslösen.
- [[ ]] Die Reihenfolge der Personen ist wichtiger als die Spaltenüberschriften.
- [[X]] Ein Testupload mit wenigen Datensätzen reduziert Risiken.
- [[ ]] Kohorten-IDs dürfen beliebig zwischen Anzeigename und Kurzname wechseln.

---

## Modul 3: Upload-Simulation und Mapping

![Illustration Modul 3: Auf einem Bildschirm ist eine Moodle-Voransicht für einen CSV-Upload zu sehen. Daneben liegt eine Checkliste mit den Schritten Testinstanz, Voransicht, Fehlerkorrektur und Produktivimport. Comic-Stil, konzentrierte Arbeitsatmosphäre.](kohorten_csv_modul3.png "Modul 3 – Upload-Simulation und Mapping")

### 3.1 Der sichere Importablauf

Ein belastbarer Uploadprozess folgt nicht dem Muster „Datei hochladen und hoffen“. Er folgt einer kontrollierten Abfolge:

```ascii
Klassenliste
   │
   ▼
Fachliche Prüfung durch Bereichsverantwortliche
   │
   ▼
CSV-Vorlage befüllen
   │
   ▼
Technische Prüfung der CSV-Datei
   │
   ▼
Testupload mit wenigen Datensätzen
   │
   ▼
Voransicht und Fehlermeldungen auswerten
   │
   ▼
Korrektur und zweiter Test
   │
   ▼
Produktivimport
   │
   ▼
Nachkontrolle und Dokumentation
```

> **📝 Merksatz**
>
> *Die Voransicht ist kein formaler Zwischenschritt. Sie ist die fachliche und technische Prüfschleife vor der produktiven Änderung.*

---

### 3.2 Upload-Simulation: Welche Einstellung passt?

Lesen Sie die Fälle und wählen Sie die fachlich passende Entscheidung.

| Fall | Passende Entscheidung |
|------|-----------------------|
| Neue Studierende sollen erstmals Moodle-Konten erhalten | [[Neue Nutzer:innen anlegen]] |
| Bestehende Nutzer:innen sollen nur der Kohorte `fs26a` zugeordnet werden | [[Bestehende Nutzer:innen aktualisieren]] |
| Ein bereits vorhandener Username taucht erneut in der Datei auf | [[Nicht automatisch neue Nummern anhängen]] |
| Die Datei enthält nur `username,cohort1` | [[Nur für bestehende Nutzer:innen und vorhandene Kohorten verwenden]] |
| Die Upload-Voransicht zeigt unbekannte Kohorten-IDs | [[Import abbrechen und IDs prüfen]] |

---

### 3.3 Kohorten zuerst, Nutzer:innen danach

Für den Schuljahresstart ist eine klare Reihenfolge hilfreich:

1. **Kohortenlogik festlegen:** Welche Klassen, Bildungsgänge, WPKs, Praxisgruppen oder Kollegiumsgruppen werden benötigt?
2. **Kohorten anlegen oder per CSV erzeugen:** mit stabiler ID, sprechendem Namen und Beschreibung.
3. **Nutzer:innendaten prüfen:** eindeutige Usernames, E-Mail-Adressen, Status, Authentifizierung.
4. **Nutzer:innen zu Kohorten zuordnen:** über `cohort1`, `cohort2` usw.
5. **Kurse per Kohortensynchronisation anbinden:** wenn spätere Änderungen automatisch in Kurszugänge einfließen sollen.

---

### 3.4 Muster-CSV: Kohorten anlegen

```csv
name,idnumber,description,visible
FS 26 A,fs26a,Fachschule Sozialpädagogik Klasse FS 26 A,1
FS 26 B,fs26b,Fachschule Sozialpädagogik Klasse FS 26 B,1
WPK Sexualpädagogik 2026,wpk_sexualpaedagogik_26,Wahlpflichtkurs Sexualpädagogik Jahrgang 2026,1
Kollegium FS Sozialpädagogik,kollegium_fs_sozpaed,Lehrkräfte und Funktionsrollen im Bildungsgang,0
```

**Prüfhinweis:**

- `name` ist der lesbare Anzeigename.
- `idnumber` ist die stabile technische ID.
- `visible` steuert, ob die Kohorte sichtbar ist.
- Beschreibungen helfen später beim Support.

---

### 3.5 Upload-Simulation als Arbeitsauftrag

> **🧩 Aufgabe 3.1 – Upload trocken durchspielen**
>
> Arbeiten Sie mit einer Testinstanz oder simulieren Sie den Ablauf auf Papier:
>
> 1. Legen Sie drei Kohorten für einen neuen Jahrgang fest.
> 2. Definieren Sie für jede Kohorte einen Anzeigenamen und eine technische ID.
> 3. Erstellen Sie eine CSV mit drei fiktiven Nutzer:innen.
> 4. Ordnen Sie mindestens eine Person zwei Kohorten zu.
> 5. Markieren Sie die Stelle, an der der Import abgebrochen werden muss, falls die Voransicht unerwartete Änderungen zeigt.

---

### ✅ Selbstüberprüfung Modul 3

**Frage 1:** Welche Reihenfolge ist für einen sicheren Schuljahresstart am sinnvollsten?

- [( )] Produktivimport, Dateiprüfung, Testupload, fachliche Freigabe.
- [(X)] Fachliche Prüfung, CSV-Erstellung, Testupload, Voransicht, Korrektur, Produktivimport.
- [( )] Kursgestaltung, Bildauswahl, Nutzer:innenimport, Klassenliste.
- [( )] Alle Nutzer:innen manuell eintragen und später die CSV-Datei nachbauen.

---

**Frage 2:** Was spricht für Kohortensynchronisation bei häufig wechselnden Zugehörigkeiten?

- [( )] Sie verhindert jede Änderung an Nutzer:innenkonten.
- [(X)] Änderungen in der Kohorte werden automatisch auf die Kursmitgliedschaft übertragen.
- [( )] Sie ersetzt alle Moodle-Rollen.
- [( )] Sie löscht nicht mehr benötigte Kurse automatisch.

---

## Modul 4: Fehlersuche und Mini-Fallstudie

![Illustration Modul 4: Eine Checkliste mit roten Markierungen liegt neben einer CSV-Tabelle. Drei Personen prüfen gemeinsam Fehler: doppelte E-Mail, falsche Kohorten-ID und fehlender Nachname. Comic-Stil, ruhig und lösungsorientiert.](kohorten_csv_modul4.png "Modul 4 – Fehlersuche und Mini-Fallstudie")

### 4.1 Fehlerhafte CSV-Datei

Die folgende Datei soll neue Nutzer:innen anlegen und direkt Kohorten zuordnen. Sie enthält mehrere Fehler.

```csv
username,firstname,lastname,email,cohort1
M.Meyer,Marie,Meyer,marie.meyer@example.edu,FS 26 A
j.schulz,Jonas,,jonas.schulz@example.edu,fs26a
s.aksoy,Selin,Aksoy,selin.aksoy@example.edu,fs26b
s.aksoy,Selin,Aksoy,selin.aksoy@example.edu,fs26b
l.nguyen,Linh,Nguyen,linh.nguyen@,fs26c
```

---

### 4.2 Fehlersuche

Ordnen Sie die Fehler der passenden Diagnose zu.

| Beobachtung | Diagnose |
|-------------|----------|
| `M.Meyer` enthält Großbuchstaben | [[Username entspricht nicht der empfohlenen stabilen Schreibweise]] |
| `FS 26 A` steht in `cohort1` | [[Anzeigename statt Kohorten-ID verwendet]] |
| Bei `j.schulz` fehlt der Nachname | [[Pflichtfeld unvollständig]] |
| `s.aksoy` kommt doppelt vor | [[Doppelter Datensatz]] |
| `linh.nguyen@` ist eingetragen | [[Ungültige E-Mail-Adresse]] |
| `fs26c` ist in Moodle noch nicht geplant | [[Ungeprüfte oder fehlende Kohorten-ID]] |

---

### 4.3 Korrigierte Fassung

```csv
username,firstname,lastname,email,cohort1
m.meyer,Marie,Meyer,marie.meyer@example.edu,fs26a
j.schulz,Jonas,Schulz,jonas.schulz@example.edu,fs26a
s.aksoy,Selin,Aksoy,selin.aksoy@example.edu,fs26b
l.nguyen,Linh,Nguyen,linh.nguyen@example.edu,fs26b
```

> **📝 Merksatz**
>
> *Ein erfolgreicher Upload beginnt nicht in Moodle, sondern in der Qualität der Ausgangsdaten.*

---

### 4.4 Mini-Fallstudie: Schuljahresstart unter Zeitdruck

Eine Fachschule startet in zwei Wochen mit zwei neuen Klassen. Das Sekretariat liefert eine Excel-Liste mit Namen und privaten E-Mail-Adressen. Die Bereichsverantwortliche ergänzt handschriftlich die Bildungsgangzuordnung. Der Admin erhält die Datei am Freitagmittag und soll die Moodle-Zugänge bis Montag bereitstellen. Eine Testinstanz ist vorhanden, wird aber im Alltag selten genutzt.

> **🧩 Aufgabe 4.1 – Fallanalyse**
>
> Analysieren Sie den Fall entlang von drei Ebenen:
>
> 1. **Datenqualität:** Welche Informationen fehlen oder sind unsicher?
> 2. **Prozessqualität:** Welche Freigaben und Prüfschritte sind nicht geklärt?
> 3. **Systemqualität:** Welche Risiken entstehen beim direkten Produktivimport?
>
> Formulieren Sie anschließend drei verbindliche Mindeststandards für den nächsten Schuljahresstart.

---

### ✅ Selbstüberprüfung Modul 4

**Frage 1:** Was ist die fachlich beste Reaktion, wenn die Upload-Voransicht unerwartet neue Kohorten anzeigt?

- [( )] Den Import trotzdem starten, weil Moodle die Kohorten automatisch ergänzt.
- [(X)] Den Import abbrechen und die Kohorten-IDs sowie vorhandenen Kohorten prüfen.
- [( )] Alle betroffenen Nutzer:innen löschen.
- [( )] Die CSV-Datei in Excel öffnen und sofort erneut speichern.

---

**Frage 2:** Welche Mindeststandards gehören in den Serienprozess?

- [[X]] Testupload mit wenigen Datensätzen.
- [[X]] Dokumentierte fachliche Freigabe.
- [[ ]] Produktivimport ohne Voransicht, wenn Zeitdruck besteht.
- [[X]] Eindeutige Namenslogik für Kohorten-IDs.
- [[X]] Nachkontrolle nach dem Import.

---

## Abschluss: Serienprozess für den Schuljahresstart

![Illustration Abschluss: Ein klarer Jahresstart-Prozess liegt als Checkliste auf einem Tisch. Admin, Bereichsverantwortliche und Sekretariat haken gemeinsam Schritte ab: Datenstand, CSV, Testupload, Freigabe, Produktivimport. Comic-Stil, klar und praxisnah.](kohorten_csv_abschluss.png "Abschluss – Serienprozess sichern")

### Rückblick

Dieser Kurs hat Kohorten- und CSV-Pflege nicht als isolierte Admin-Aufgabe behandelt, sondern als gemeinsamen Organisationsprozess. Entscheidend ist die Verbindung aus fachlicher Prüfung, technischer Genauigkeit und dokumentierter Verantwortung.

---

### 5.1 Checkliste für den produktiven Import

| Prüffrage | Ja/Nein/Notiz |
|-----------|---------------|
| Liegt eine aktuelle und freigegebene Klassenliste vor? |  |
| Sind alle Kohorten mit Anzeigename und technischer ID definiert? |  |
| Sind Nutzer:innennamen, E-Mail-Adressen und interne Kennungen geprüft? |  |
| Wurde die CSV-Datei im Texteditor kontrolliert? |  |
| Wurde ein Testupload mit wenigen Datensätzen durchgeführt? |  |
| Wurde die Moodle-Voransicht fachlich und technisch geprüft? |  |
| Wurde der Produktivimport ausdrücklich freigegeben? |  |
| Wurde das Ergebnis stichprobenartig kontrolliert? |  |
| Wurde dokumentiert, welche Datei wann durch wen importiert wurde? |  |

---

### 5.2 Transferauftrag

> **🧩 Aufgabe 5.1 – Eigene Prozessskizze erstellen**
>
> Erstellen Sie für Ihre Einrichtung eine einseitige Prozessskizze mit folgenden Elementen:
>
> - Datenquelle
> - verantwortliche Rolle
> - CSV-Vorlage
> - Testinstanz
> - Freigabeentscheidung
> - Produktivimport
> - Nachkontrolle
> - Ablageort der Dokumentation
>
> Ergänzen Sie eine Regel, wie kurzfristige Änderungen nach Schuljahresstart bearbeitet werden.

---

### 💭 Abschlussreflexion

> Welche Änderung hätte den größten Effekt auf die Qualität Ihrer Moodle-Nutzer:innenpflege: bessere Datenquelle, klarere Rollenmatrix, verbindliche Testinstanz oder einheitliche Kohorten-IDs?
>
> Begründen Sie Ihre Entscheidung in drei Sätzen.

---

### ✅ Abschlusstest

**Frage 1:** Welche Aussage fasst den Kern des Kurses zusammen?

- [( )] CSV-Upload ist vor allem eine Frage der Geschwindigkeit.
- [(X)] CSV-Upload ist ein kontrollierter Serienprozess aus Datenprüfung, Test, Voransicht, Freigabe und Nachkontrolle.
- [( )] Kohorten sollten möglichst spontan nach Bedarf benannt werden.
- [( )] Fachliche Prüfung ist bei technischen Importen nicht nötig.

---

**Frage 2:** Ergänzen Sie den Prozess in der richtigen Logik.

| Schritt | Reihenfolge |
|---------|-------------|
| Klassenliste fachlich prüfen | [[1]] |
| CSV-Vorlage befüllen | [[2]] |
| Testupload durchführen | [[3]] |
| Voransicht auswerten | [[4]] |
| Produktivimport freigeben | [[5]] |
| Ergebnis dokumentieren | [[6]] |

---

**Frage 3:** Welche Aussagen sind fachlich tragfähig?

- [[X]] Kohorten-IDs sollten stabil, eindeutig und dokumentiert sein.
- [[X]] Bestehende Nutzer:innen können über `username` und `cohort1` einer Kohorte zugeordnet werden, wenn die Daten eindeutig sind.
- [[ ]] Anzeigename und Kohorten-ID sind immer austauschbar.
- [[X]] Eine Testinstanz reduziert Risiken vor produktiven Änderungen.
- [[ ]] Der Produktivimport sollte bei Zeitdruck ohne Voransicht erfolgen.

---

## 📚 Weiterführende Ressourcen

- MoodleDocs. (2025). *Upload users*. https://docs.moodle.org/en/Upload_users
- MoodleDocs. (2025). *Cohorts*. https://docs.moodle.org/en/Cohorts
- MoodleDocs. (2025). *Upload cohorts*. https://docs.moodle.org/en/Upload_cohorts
- MoodleDocs. (2025). *Cohort sync*. https://docs.moodle.org/en/Cohort_sync
- MoodleDocs. (2025). *Cohort enrolment*. https://docs.moodle.org/en/Cohort_enrolment

---

## 🧾 Anhang: Kopiervorlagen

### A. Kohorten-CSV

```csv
name,idnumber,description,visible
FS 26 A,fs26a,Fachschule Sozialpädagogik Klasse FS 26 A,1
FS 26 B,fs26b,Fachschule Sozialpädagogik Klasse FS 26 B,1
WPK Sexualpädagogik 2026,wpk_sexualpaedagogik_26,Wahlpflichtkurs Sexualpädagogik Jahrgang 2026,1
```

### B. Nutzer:innen-CSV mit Kohorte

```csv
username,firstname,lastname,email,auth,idnumber,department,cohort1
m.meyer,Marie,Meyer,marie.meyer@example.edu,manual,STU-2026-001,FS Sozialpädagogik,fs26a
j.schulz,Jonas,Schulz,jonas.schulz@example.edu,manual,STU-2026-002,FS Sozialpädagogik,fs26a
s.aksoy,Selin,Aksoy,selin.aksoy@example.edu,manual,STU-2026-003,FS Sozialpädagogik,fs26b
```

### C. Bestehende Nutzer:innen in Kohorten einordnen

```csv
username,cohort1,cohort2
m.meyer,fs26a,wpk_sexualpaedagogik_26
j.schulz,fs26a,
s.aksoy,fs26b,wpk_sexualpaedagogik_26
```
