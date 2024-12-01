---
title: "Codebuch Billionaires"
author: "Franziska Zeller"
date: "2024-10-07"
output:
  md_document:
    variant: "markdown_github"
---

# Codebuch Billionaires

Codebuch Stand 2024-11

## **Ursprung und Datenerhebung**

Wir erheben die Daten der 50 reichsten Milliardäre weltweit nach der Forbes Liste “The World’s Billionaires”: <https://www.forbes.com/billionaires/>.

Das Netzwerk ist ein ungerichtetes two-mode Netzwerk, dass aus Milliardären und Institutionen besteht. Institutionen können sein: Unternehmen, Vereine, Universitäten, oder auch Länder.

## **Nodelist**

**id:** "Person und Universität: erste zwei Buchstaben des Vornamens und erste zwei Buchstaben des Nachnamens; (klein geschrieben) Bsp.: Bill Gates = biga Unternehmen: die ersten vier Buchstaben, Land: Abkürzung nach Iso-Code (Übersicht siehe: <https://www.oenb.at/Statistik/Klassifikationen/ISO-Codes/ISO-Code-Verzeichnis-fuer-Laender--und-Waehrungscodes.html>"

**id_name**: echter Name der Person oder Institution (wenn Institution/Land nur Name, in den weiteren Spalten NA) 

**wealth**: " Vermögen in Billionen (mit punkt (zb: 19.5), auch mit Punkt wenn eine 0) (Auf Forbes die rechte Zahl, 2024 Billionaires Net Worth); bei Institutiontn/Firmen einfach eine 0 " 

**forbes_ranking**: Platz in der Forbes Liste (bei gleichplatzierten gleiche Nummer angeben) 

**gender**: Geschlecht: 1= Männer, 2= Frauen, 3= Divers 

**birth_year**: Geburtsjahr (bei Institution/Firmen:0) 

**nationality** Nationalität nach ISO-Code (zwei Buchstaben!) Orientierung an Forbes Liste (bei Institution/Firma: Land, in dem die Institution ihren Sitz hat)

**university**: Universität/Ausbildungsstätte, ganzer Name mit Unterstrich und kleingeschrieben, bei mehreren Abschlüssen den höchsten (bei Institution/Firma: NA)

**learned_job**: gelernter Beruf, Name auf Englisch (Kleingeschrieben und Unterstrich bei Leerzeichen); (bei Institution/Firma: NA)

**money_source**: "1= Erbe, 2= Gründung/Erfindung, 3= Hedgefund/Aktien, 4= Immobilien, 5= Scheidung, 6= Unternehmensführung; Prinzip doppelte zahlen: 12=Erbe&Gründung/Erfindung, 13=Erbe&Aktien, 14=Erbe&Immobilien --\> max 2 Gründe nennen"

**industry**: welcher Branche gehört die Person an? Name auf Englisch, kleingeschrieben nach forbes liste, bei leerzeichen und &: weglassen und snake case! NEU: wenn eine NGO/was soziales dann welfare

**type**: 1= Person, 2=Institution (Firma/Uni/Organisation etc.) 3= Land

\##**Edgelist**:

**relation**: 1= Besitzer/Eigentümer, 2=Gründer, 3=Arbeitsbeziehung/ehemaliger wichtiger Job, 4= investiert in/spendet an , 5=besitzt Anteile, 6= Unternehmen sponsert, 7= Mitgliedschaft, 8= ist Staatsbürger\*in, 9= hat dort studiert, 10= Bekanntschaft/Freundschaft, 11= Familie, 12=Verheiratet, 13=Geschieden

Verbindungen, die wir angeben: Beziehungen zwischen Milliardäre, Universität, Land (das was auch in der Nationalität angegeben ist), relevante Firmen/Institution

