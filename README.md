# ⚖️ Balance-Connectée

<img width="2868" height="874" alt="image" src="https://github.com/user-attachments/assets/f7682111-006a-4866-8290-25ec8bca5528" />


# Introduction

  Dans le cadre d'un **projet en Instrumentation Avancée** au département Mesures Physiques de Marseille, nous avons réalisé en **binôme** une **balance connectée** dont l'objectif était de **mesurer** une masse dans un intervalle compris entre 0 et 200g et de **transmettre** les données à une **interface Node-RED** via un **protocole MQTT**.


# Fonctionnalités 

- Tare de la balance avec une masse étalon de 100g.
  
- Bouton de peser pour la mesure d'une masse comprise entre 0 et 200g.
  
- Lecture & affichage de la témpérature à l'aide du capteur DHT11.
  
- Affichage formaté de la masse sur Node-RED: **m = [masse] ± [incertitude] g**.
  
- Choix de l'affichage : **Balance étalonnée** ou **Balance classée**.

- Affichage de l'heure et de la date de la mesure

- Background animé : dégradé blanc/gris


# Matériels utilités

| Quantité | Composant | 
|  :---:  | :---:  | 
| 1 | `Microcontrôleur ESP32` | 
| 1 | `Capteur de température DHT11` | 
| 1 | `Convertiseur & amplificateur HX711` | 
| 1 | `Cellule de charge` | 

# Logiciels utilisés

| Logiciels | 
|  :---:  |
| `Visual Studio Code &  PlatformIO` | 
| `Mosquitto (protocole MQTT)` | 
| `Node-RED (interface utilisateur)` | 





> [!WARNING]
> En cas d'instabilité de la mesure, relancer la tare avec la masse étalon de 100g.

