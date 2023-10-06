# Galgje Spel

Dit is een eenvoudige implementatie van het Galgje-spel in pseudocode. Het Galgje-spel is een woordraadspel waarbij een speler een geheime woord probeert te raden door letters te kiezen. De speler heeft een beperkt aantal pogingen voordat het figuur van een hangende man compleet wordt getekend (de galg).

## Spelregels

- Het spel selecteert willekeurig een geheim woord uit een lijst met woorden.
- De speler heeft een beperkt aantal kansen om letters te raden voordat de galg compleet wordt getekend.
- De speler wint als hij het geheime woord raadt voordat de galg compleet is.
- De speler verliest als de galg compleet wordt getekend voordat hij het woord raadt.

## Pseudocode

Hier is een vereenvoudigd voorbeeld van de pseudocode voor het Galgje-spel:
```
procedure galgje_spel()
    woordlijst = ["appel", "banaan", "perzik", "aardbei", "kers"]
    geheim_woord = willekeurig_kies(woordlijst)
    pogingen_over = 6
    geraden_letters = []

    toon_welkomstboodschap()

    zolang pogingen_over > 0 en niet woord_geraden(geheim_woord, geraden_letters)
        toon_huidige_toestand(geheim_woord, geraden_letters, pogingen_over)
        letter = vraag_speler_naar_letter()
        
        als letter al geraden
            toon("Je hebt deze letter al geraden. Probeer een andere.")
        anders als letter in geheim_woord
            voeg letter toe aan geraden_letters
            toon("Goed geraden!")
        anders
            verminder pogingen_over met 1
            toon("Fout geraden. Je hebt nog " + pogingen_over + " pogingen over.")

    als woord_geraden(geheim_woord, geraden_letters)
        toon("Gefeliciteerd! Je hebt het geheime woord geraden: " + geheim_woord)
    anders
        toon("Helaas, je hebt verloren. Het geheime woord was: " + geheim_woord)
    einde spel
```

## Aan de slag

Om het Galgje-spel te spelen, voer je de code uit in een geschikte programmeeromgeving. Zorg ervoor dat je de benodigde functies (zoals `willekeurig_kies`, `toon_welkomstboodschap`, enz.) implementeert voordat je het spel start.

## Licentie

Dit project is gelicentieerd onder de MIT-licentie. Zie het `LICENSE`-bestand voor meer informatie.



