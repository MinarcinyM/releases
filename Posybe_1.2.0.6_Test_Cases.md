# Posybe 1.2.0.6 Test Cases

Test cases for Posybe 1.2.0.6 release.

# List of changed components

|EETService|1.0.1.1|
|HOSSchedulerProcessor|2.0.36.0|

# Test scenarios for changed components

## EETService 1.0.1.1
### Aplikovanie timeout pri proxy
- Nasimulujeme situaciu, kedy je pre EET dostupna proxy, ale cielovy statny server (statny test server) nie je dostupny
- Vykoname niekolko predajov tovaru na pokladni
- Pri kazdom predaji musi vytlacit doklad s PKP a BKP kodmi a nesmie byt na vytlacenom doklade vytlaceny FIK kod pricom EET komunikacia nesmie trvat dlhsie ako je nastaveny timeout v konfiguracii EETServisu

## HOSSchedulerProcessor 2.0.36.0
### Zmena ceny tovaru do minulosti
- Prostrednicstvom testovacieho SAPu zasleme zmenu ceny artiklu ktorej platnost zacina aj konci v minulosti
- Skontrolujeme, ze sa takto zmena ceny neaplikovala na CS

### Zmena ceny tovaru zacinajuca v minulosti ale pokracujuca do buducnosti
- Prostrednicstvom testovacieho SAPu zasleme zmenu ceny artiklu ktorej platnost zacina v minulosti, ale pokracuje dalej do buducnosti
- Zelany stav je taky, ze sa takato zmena ceny artiklu spravne aplikovala na CS

### Zmena ceny tovaru nastavena do buducnosti
- Prostrednicstvom testovacieho SAPu zasleme zmenu ceny artiklu ktorej platnost zacina v buducnosti
- Skontrolujeme, ze sa zmena ceny artiklu nenastavila na CS okamzite
- V case nastavenej platnosti zmeny ceny skontrolujeme cenu artiklu
- Zelany stav je taky, ze cena artiklu sa zmeni v case, odkedy ma nastavenu platnost
