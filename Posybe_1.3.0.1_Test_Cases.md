# Posybe 1.3.0.1 Test Cases

Test cases for Posybe 1.3.0.1 release.

# List of changed components

PEM.Loyalty 1.0.1.3
CPHOSToolOrchestrator 1.0.3.1
PEM 1.0.22.1

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