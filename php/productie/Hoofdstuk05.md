# Hoofdstuk 5 - Get parameters

## 5.1 Wat ga je leren ?

Wat een Get parameter is. Hoe pas je deze aan in een URL. De eerste manier om iets door te geven aan een script.

Voorwaardelijke code: Hoe maak je in php een if else constructie.

## 5.2 Voorbeeld get en if

Bekijk allereerst dit voorbeeld
[Voorbeeldvideo met $_GET parameters](https://mix.office.com/watch/16sdvrg08ufjb)

~~~php
// 1. Maak een script aan in de map hoofdstuk 5 met de naam opdracht50.php
// 2. Neem de volgende code over in het script en launch het in je browser
// Wat zie je?
echo $_GET['leeftijd'];

$leeftijd = $_GET['leeftijd'];

if ($leeftijd > 17) {
    echo "Je bent volwassen";
} else {
    echo "Je bent nog een kind";
}


//3. Pas de URL in je browser aan door ?leeftijd=10 aan het eind toe te voegen
//   Wat zie je nu als je nu de pagina opvraagt?

//4. Voeg een tweede variabele toe aan je script

$naam = $_GET['naam'];

//5. Je kan een tweede get-parameter toevoegen aan het eind van de url door bijv &naam=Abu Saebu toe te voegen
//De volledige url is dan http://localhost:4567/voorbeeld.php?leeftijd=52&naam=Abu Saebu
// Pas je if statement aan alsvolgt:

if ($leeftijd > 17) {
    echo "$naam is volwassen";
} else {
    echo "$naam is nog een kind";
}

~~~

---
## 5.3 Opdracht 50

### Omschrijving 50
Volg alle stappen in het bovenstaande voorbeeld 5.1

### Visuele weergave
Uiteindelijke weergave opdracht50.php is:

> Giovanni is nog een kind

### Beoordelingscriteria 50
1. Launch van de opdracht50.php levert errors op in de browser
2. Toevoegen van de juiste get-parameters en waardes, voorkomen de error meldingen
3. De uitvoer (de visuele weergave) is afhankelijk van de invoer.

---

## 5.4 Opdracht 51

### Omschrijving 51
Maak een script met de naam opdracht51.php en test de script met een aantal get-parameters voor: naam, leeftijd en plaats

Zet in je script 2 if-else constructies met de volgende voorwaardes:
1. $plaats == "Den Bosch" // Is de plaats gelijk aan "Den Bosch"?
2. $leeftijd > 25         // Is de leeftijd hoger dan 25?

### Visuele weergave 51

Ik ben Abu Saebu. 
Ik ben een bosschenaar.
Ik ben best oud.

of

Ik ben Jan Lucassen.
Ik ben geen bosschenaar.
Ik ben nog best jong.

De visuele weergave hierboven is afhankelijk van de waardes van je GET-parameters.

### Programmastructuur 51

~~~php
// waar hieronder ... staan wil zeggen dat je er zelf nog code aan moet toevoegen
$leeftijd = $_GET['leeftijd'];
...

if ($leeftijd > 25) {
    echo ...
}
else {
    echo ...
}

if (bosschenaar?) ....

~~~

### Beoordelingscriteria 51
1. Je maakt gebruik van 3 get-parameters
2. Je script geeft foutmeldingen als je niet de get-parameters toevoegt aan je url
3. Je script geeft geen foutmeldingen als je de juiste get-parameters en waarden toevoegt aan je url
4. De visuele weergave van je script is afhankelijk van de waardes van de get-parameters.
---

## 5.5 Extra - hoe voorkom je foutmeldingen met gebruikte $_GET['parameters']?

~~~php

//Door het te testen op het bestaan van de  get-parameter met de isset() functie op de volgende manier:

if (isset($_GET['naam'])) {

    $naam = $_GET['naam'];
} else {

    $naam = "Een andere waarde als de get niet bestaat";
}

~~~