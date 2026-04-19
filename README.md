# trmnl_ha_netatmo
Station météo Netatmo sur écran TRMNL via Home Assistant

<img width="2048" height="1536" alt="image" src="https://github.com/user-attachments/assets/e118030c-8d4c-4d6b-98ac-c169708cfda0" />


Je voulais vous présenter un petit projet de "station météo améliorée" que je viens de terminer sur base d’écran e-ink.

Depuis longtemps, je possède une station météo Netatmo qui marche plutôt bien mais qui est dépourvue d’écran. J’ai donc corrigé cette lacune en utilisant un écran TRMNL que j’ai fait venir des USA.

La station météo est connectée à HA en mode API (bien plus fiable !!!). L’affichage de l’écran est en fait un tableau de bord HA codé à la main, avec amour, en YAML/CSS. Ce tableau de bord est repris par le plugin officiel de TRMNL qui se charge de générer une image et de l’envoyer vers l’écran toutes les 10 minutes.

Avec cette méthode, on a une liberté totale car on peut afficher n’importe quel capteur disponible sur HA !

Dans mon cas, j’affiche :
la qualité de l’air
les données de ma station
la météo prédictive de Météo-France
la quantité d’eau de pluie disponible dans ma citerne

>>> Matériel

Station météo :
https://www.netatmo.com/fr-fr/smart-weather-station

Ecran :
https://trmnl.com/

Sonde de cuve :
https://www.shelly.com/fr/products/shelly-blu-distance

>>> HA APPS

TRMNL :
https://github.com/usetrmnl/trmnl-home-assistant/compare/v0.6.9...v0.7.0

Cloudflared (pour l'accès https utilisé par l'API netatmo)
https://github.com/homeassistant-apps/app-cloudflared/

>>> HACS

apexcharts-card 
https://github.com/RomRider/apexcharts-card/

Atmo France pour Home Assistant
https://github.com/sebcaps/atmofrance/

card-mod
https://github.com/thomasloven/lovelace-card-mod/

MeteoFrance weather card
https://github.com/hacf-fr/lovelace-meteofrance-weather-card/
