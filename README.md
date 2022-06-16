# Semantisk HTML

Dette prosjektet er laget for å gi innsikt i hvordan vi kan skrive semantisk korrekt html på prosjektene våre. Vi
starter med usemantisk HTML, og gjør det sakte men sikkert om til semantisk HTML.

OBS SE OVER DETTE!!
Åpne terminalen og last ned repoet ved å skrive `git clone git@github.com:sisselfladby/semantic-workshop.git.`

Her finner du tre filer - `README.md` er denne fila, `oppgave.html` er fila du starter med, og `fullstendig-eksempel.html` 
er løsningsforslaget.

For å se nettsiden åpner du `oppgave.html` i en nettleser.

## Oppgave 1 - Headeren i et HTML-dokument (bør flyttes til siste oppgave?)

Før vi gyver løs på innholdet, skal vi ta en titt på metadataen i et HTML-dokument.

<b>Legg inn språk i dokumentet.</b> Dette gjøres ved å legge inn `lang`-attributten i `<html>`-taggen i starten av 
dokumentet.

<details><summary>Hint</summary>

```html
<html lang="nb">
```
</details>

<b>Legg inn en tittel på nettsiden din i `<head>`-taggen.</b> 
Det er denne tittelen som vises i fanen i nettleseren når du åpner fila, og forteller søkemotorer og lignende hva 
tittelen på hele nettstedet er. Denne er ikke synlig på siden. Dette gjøres ved å bruke `<title>`-taggen.


<details><summary>Hint</summary>

```html
<head>
    <meta charset="UTF-8">
    <title>Semantisk HTML</title>
</head>
```
</details>

<b>Legg inn en beskrivelse av innholdet på nettsiden din i `<head>`-taggen.</b>
Det er dette som vises når noen søker på nettsiden din i en søkemotor. Dette gjøres ved å bruke en `<meta>`-tag med
attributten `name="description"`. Innholdet skrives i attributten `content`.

<details><summary>Hint</summary>

```html
<head>
    <meta charset="UTF-8">
    <title>Fullstendig HTML eksempel</title>
    <meta name="description" content="Dette er en eksempel HTML for å demonstrere hvordan man kan lage god semantisk HTML.">
</head>
```
</details>

## Oppgave 2 - Titler og tekst


## Oppgave 2 - Titler, paragrafer, sitater, .. andre tekstlige ting

## Oppgave 3 - Lister

## Oppgave 4 - Links and buttons

## Oppgave 5 - Input

## Oppgave 6 - Struktur

