# Intro til semantisk HTML

Dette prosjektet er laget for å gi innsikt i hvordan vi kan skrive semantisk korrekt html på prosjektene våre. Vi
starter med usemantisk HTML, og gjør det sakte men sikkert om til semantisk HTML.

Åpne terminalen og last ned repoet (f. eks ved å skrive `git clone git@github.com:sisselfladby/semantic-workshop.git.`)

Her finner du tre filer i roten - `README.md` er denne fila, `index.html` er fila du starter med, og `fullstendig.html` 
er løsningsforslaget.

For å se nettsiden åpner du `index.html` i en nettleser, for å se hvordan sluttproduktet skal se ut åpner du `fullstendig.html`.

Gjennom hele oppgavesettet kan du bruke https://developer.mozilla.org/en-US/docs/Web/HTML/Element som referanse, eller
huk tak i oss!

<em>Etter hver oppgave: legg merke til endringer på siden. Mange HTML-elementer kommer med default styling.</em>

## Oppgave 1 - Titler og tekster
I HTML har vi taggene `<h1>` til `<h6>` som spesifiserer titler på siden. `<h1>` er sidetittelen, og må kun settes èn gang
per HTML-dokument. `<h2>` til `<h6>` kan være flere steder i samme dokument.

<b>Oppgave: Endre til semantiske titler der det passer inn på siden.</b>

For å lage en paragraf med tekst kan vi bruke `<p>`.

<b>Oppgave: Endre til paragrafer der det passer inn på siden.</b>

Når det gjelder tekstlig innhold finnes det forøvrig mange varianter
man kan bruke for å gjenspeile bl. a tid, sitater, forkortelser etc. Se mer om dette på 
https://developer.mozilla.org/en-US/docs/Web/HTML/Element#text_content.

## Oppgave 2 - Lister
Det finnes i hovedsak to typer semantiske lister, `<ol>` og `<ul>`. I førstnevnte er rekkefølgen viktig. For å benevne et
listeelement bruker vi `<li>`. `<menu>` er et alternativ til `<ul>` dersom du ønsker å lage en semantisk meny. Da bør 
hvert av elementene inneholde en lenke.

<b>Oppgave: legg inn riktig listetype der det passer inn.</b>

## Oppgave 3 - Links and buttons
`<a>` med `href`-attributten danner en lenke som tar deg til en ny side, filer, epostadresser, steder innad i samme side
eller annet som en URL kan adressere. Knapper `<button>` gjør noe interaktivt på siden du er på. 

<b>Oppgave: legg inn knappe- og lenketagger i appen.</b>

<details><summary>Hint</summary>

Lenke:
```html
<a href="https://bekk.no">Bekk</a>
```
Knapp:
```html
<button type="button" onClick={() => console.log("Hallo")}>Logg "hallo" til konsollen</button>
```
</details>

<em>Dersom et element ser ut som en knapp, men oppfører seg som en lenke, skal det fortsatt kodes som en lenke. (Og aller 
helst bør det se ut som en lenke og!)</em>

<em>Knapper (`<button>`) kan være av tre ulike typer. `type="submit"` er default og sender inn `<form>`-data. Der brukes også `type="reset"`.
`type="button"` er bare en button og må styres med javaScript. Til gjengjeld er det den som typisk er hyppigst brukt.</em>

## Oppgave 4 - Form, input og labler
For å motta brukerinput trenger vi et `<input>`-element. Taggen brukes for mange forskjellige elementer, f.eks 
tekst, tall, sjekkbokser, radioknapper osv. Hvilken type input-felt det er justeres med attributten `type`.
Hvert inputfelt trenger en assosiert `<label>`, for å tydeliggjøre hva brukeren skal fylle inn.

<b>Oppgave: Endre til input-element med label passende sted på siden.</b>

<details><summary>Hint</summary>

```html
<label>
    Fyll inn tekst i feltet under
    <input type="text" />
</label>
```
eller
```html
<label for="mitt-input-felt">Fyll inn tekst i feltet under</label>
<input id="mitt-input-felt" type="text" />
```
</details>


Rundt et `<input>`-felt og en submit-`<button>` bør det ligge en `<form>`-komponent, slik at det blir et skjema.

<b>Oppgave: Legg en `<form>`-tag rundt inputfelt og submitknapp.</b>

<em>Med riktig og god implementasjon av skjemaer og input-tags, vil nettleser/operativsystem hjelpe til med å fylle ut, det 
gjør det langt enklere for brukere!</em>


## Oppgave 5 - Struktur og innholdsoppdeling
Innholdet på siden er typisk oppdelt i semantisk struktur, som sier noe om hvordan siden er organisert.

<b>Oppgave: Del innholdet i `<body>` opp i `<header>`, `<main>` og `<footer>`.</b>

Det finnes mange HTML-tagger som deler HTMLen din i inn i logiske bestanddeler, ta en titt på lista over disse her: 
https://developer.mozilla.org/en-US/docs/Web/HTML/Element#content_sectioning. 

<b>Oppgave: Er det noen av disse som bør benyttes på siden?</b> 

<details><summary>Hint</summary>

Ta f. eks en titt på `<nav>` og `<address>`
</details>

## Oppgave 6 - Headeren i et HTML-dokument

Nå har vi sett på innholdet i body, og avslutter med å ta en titt på metadataen i et HTML-dokument.

<b>Oppgave: Legg inn språk i dokumentet.</b> Dette gjøres ved å legge inn `lang`-attributten i `<html>`-taggen i starten av
dokumentet.

<details><summary>Hint</summary>

```html
<html lang="nb">
```
</details>

<b>Oppgave: Legg inn en tittel på nettsiden din i `<head>`-taggen.</b>
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

<b>Oppgave: Legg inn en beskrivelse av innholdet på nettsiden din i `<head>`-taggen.</b>
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

## Avslutning

<b>Oppgave: Sammenlign ditt svar med løsningsforslaget. Hva er likt, og hva er ulikt? Har du noen spørsmål?</b>

Hvis ikke, så... Det var det! Klapp deg selv på skulderen og ta en kopp kaffe, du er klar til å skrive semantisk HTML på ditt neste prosjekt!