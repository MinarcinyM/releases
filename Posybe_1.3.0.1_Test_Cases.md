# Posybe 1.3.0.1 Test Cases

Test cases for Posybe 1.3.0.1 release.

# List of changed components

PEM.Loyalty 1.0.1.3<br>
CPHOSToolOrchestrator 1.0.3.1<br>
PEM 1.0.22.1<br>
DMS 1.2.6.5<br>
PosybeOperationsManagerService 1.0.15.4<br>
ERP2Posybe 1.0.28.0

# Test scenarios for changed components

## PEM.Loyalty 1.0.1.3
### Stlpcove operacie v stlpci Loyalty shop a doplatok
- Otvorime aplikaciu PEM
- Prihlasime sa s uzivatelom, ktory ma prislusne prava pre cast Loyalty
- Vyskusame stlpcove operacie nad stlpcom Loyalty shop a doplatok
- Korektne spravanie je take, ze stlpcove operacie nad stlpcom Loyalty shop a doplatok je mozne vykonat

## CPHOSToolOrchestrator 1.0.3.1 a PEM 1.0.22.1
### Vytvorenie kopie reportu v Kontrole definicie tovarov
- Otvorime aplikaciu PEM
- Prihlasime sa s uzivatelom, ktory ma prislusne prava pre cast Kontrola definiecie tovarov
- Z akehokolvek zobrazeneho reportu vytvorime kopiu
- Zelany stav je taky, aby kopiu reportu bolo mozne vytvorit.

### Porovnanie combopacku v Kontrole definicie tovarov
- Otvorime aplikaciu PEM
- Prihlasime sa s uzivatelom, ktory ma prislusne prava pre cast Kontrola definiecie tovarov
- Vytvorime reportu na kontrolu takeho tovaru, ktory je combopackom
- Zelany stav je taky, ze report s porovnanim combopacku bude korektne zobrazeny

### Kontrola nacitanej predajnej ceny v reporte v casti Kontrola definicie tovarov
- Otvorime aplikaciu PEM
- Prihlasime sa s uzivatelom, ktory ma prislusne prava pre cast Kontrola definiecie tovarov
- Vytvorime porovnanie lubovolnych tovarov
- Vo vygenerovanom porovnani skontrolujeme, ci sa korektne nacitala predajna cena artiklov


## DMS 1.2.6.5
### Viacnasobne paralelne prihlasenie do DMS
- Do aplikacie DMS sa prihlasime s viacerymi uzivatelmi v rovnakom case
- Pozadovane spravenie je take, ze uzivatelia sa korektne prihlasia

### Viacnasobne paralelne prihlasenie do DMS a zaroven paralelne nahravanie dokumentov do DMS
- Do aplikacie DMS sa prihlasime s viacerymi uzivatelmi v rovnakom case
- Kazdy prihlaseny uzivatel v rovnakom case ulozi dokument do DMS
- Pozadovane spravanie je take, ze vsetci uzivatelia budu moct ulozit dokument a nasledne bude mozne kazdy takto ulozeny dokument zobrazit v DMS.

### Vytvorenie noveho DMS dokumentu s ulozenim suboru
- Prihlasime sa do aplikacie DMS
- Vytvorime novy DMS dokument s notifikaciou pre skupinu uzivatelov
- Ulozime don subor
- Korektne spravanie je take, ze novy DMS dokument bude uspesne vytvoreny s ulozenym suborom a zvolena skupina uzivatelov bude notifikovana

### Vytvorenie noveho DMS dokumentu bez ulozenia suboru
- Prihlasime sa do aplikacie DMS
- Vytvorime novy DMS dokument s notifikaciou pre skupinu uzivatelov, ale neulozime ziaden subor
- Korektne spravanie je take, ze novy DMS dokument bude uspesne vytvoreny aj bez ulozeneho suboru a zvolena skupina uzivatelov bude notifikovana

### Editacia existujuceho DMS dokumentu s ulozenim suboru
- Prihlasime sa do aplikacie DMS
- Pri editacii ulozime k tomuto DMS dokumentu subor
- Korektne spravanie je take, ze editovany DMS dokument s pridanym suborom bude korektne ulozeny a subor bude nasledne mozne zobrazit v DMS

### Editacia existujuceho DMS dokumentu bez ulozenia suboru
- Prihlasime sa do aplikacie DMS
- Pri editacii neulozime k tomuto DMS dokumentu ziadny subor
- Korektne spravanie je take, ze editovany DMS dokument bude korektne ulozeny

## PosybeOperationsManagerService 1.0.15.4
### Vytvorenie cenovkoveho suboru v ramci uzavierky obchodneho dna
- Cez testovaci SAP vytvorime zmeny cien pre sledovanu CS s nasledovnymi parametrami: zmena ceny tovaru zacinaju v minulosti a pokracujuca do buducnosti (platna v aktualny den), okamzita zmena ceny tovaru, naplanovana zmena ceny tovaru do buducnosti o jeden/dva dni
- Otvorime aplikaciu Uzavierka obchodneho dna
- Prihlasime sa s uzivatelom s potrebnymi opravneniami
- V ramci prebiehajucej uzavierky obchdoneho dna sa prepneme do casti menu "Zmeny cien"
- V hornej casti menu klikneme na talcitko "Cenovky"
- Korektne spravanie je take, ze sa zobrazi cenovkovy subor s cenovkami pre tovary, ktore mali nastavenu zmenu ceny pre aktualne uzatvarany den a zaroven pre nasledujuce dni podla nastavenia v konfiguracii servisu (PROD nastavenie 10 dni do buducnosti)

### Regresny test funkcionality akciovych balickov
- Vytvorime akciove balicky typu 2,5,6,7
- Cez testovaci SAP vytvorime zmeny cien pre sledovanu CS pre tovary, ktore su zaradene vo vytvorenych akciovych balickoch s nasledovnymi parametrami: zmena ceny tovaru zacinaju v minulosti a pokracujuca do buducnosti (platna v aktualny den), okamzita zmena ceny tovaru, naplanovana zmena ceny tovaru do buducnosti o jeden/dva dni
- Zmeny cien tovarov v akciovych balickoch musia byt take, aby neboli nizsie nez je akciova cena tovaru v ramci vytvorenych akciovych balickov
- Pozadovane spravanie je take, ze vyska poskytovanej zlavy pre tovary v akciovych balickoch bude korektne prepocitana a akciove balicky bude mozne predavat na pokladni (tie ktore, budu aktivovane na sledovanej CS)

## ERP2Posybe 1.0.28.0
### Vytvorenie objednavky s mensim poctom poloziek ako vstupny DESADV (EDI)
- Cez testovaci SAP vytvorit objednavku, ktora ma menej poloziek ako vstupny DESADV subor
- Skontrolovat, ci sa v sklade objavil dodaci list bez tychto poloziak a ci sa vytvoril chybovy APERAK subor

### Vytvorenie objednavky s mensim mnozstvom niektorej polozky ako ma vo vstupnom DESADV (EDI)
- Cez testovaci SAP vytvorit objednavku, ktora ma mensie mnozstvo niektorej polozky ako vo vstupnom DESADV subore
- Skontrolovat, ci sa vytvoril chybovy APERAK subor

### Regresny test spracovania interface
- Poslat na testovacie pracovisko vsetky aktualne pouzivane IF v produkcii (ArticleMaster, SiteArticleMaster, ProcurementDocument, atď.) pre vsetky typy tovarov. 
- Skontrolovat, ci sa prijate IF spracovali bez chyby. 
- Skontrolovat, ci sa zmeny aplikovali spravne na vsetkych urovniach az po pokladnu. 