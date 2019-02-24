# Posybe 1.3.0.1

# Major changes

## Slovak fiscalization
Posybe is now compliant with new Slovak fiscalization law e-Kasa

## Site pricing reworked
Site pricing has been reworked to provide faster execution, better conflict and timing handling and logging.

# Minor changes

## Kalibrate interface
Kalibrate can now be integrated to Posybe to support automated fuel price changes.

# Bugfixes
> Zoznam bugfixov s referenciou na jira a cislo ticketu v zakaznickom systeme

# Known issues
> Zoznam znamych issues

# Installation and upgrade
## Installation
Standard installation procedure is reqiured

## Upgrade
Direct upgrade from Posybe 1.3.* is supported

# Changed components
|Component|Version|Changelog|
|---|---|---|
|EvidCDL|?|Gzip compression for webservices calls (DEV-297)|
|CommProcessor|2.4.2.1|Communication resiliency improvement|
|PosybeDB|V41| |
|DomsTGDeliveryProcessor|?|Tool to clear tank deliveries from DOMS|
|PSCreator|?|Update to match database and other changes|
|POS|0.2.2.?|- SiteController now displays ullage in tanks (DEV-233)<br>- Dispenser totals can be printed on any POS (DEV-236)|
|Pricing on BOS|?|Reworked pricing on BOS|
