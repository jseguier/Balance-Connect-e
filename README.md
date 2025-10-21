# ⚖️ Balance Connectée

<img width="2868" height="874" alt="image" src="https://github.com/user-attachments/assets/f7682111-006a-4866-8290-25ec8bca5528" />


# Introduction

Dans le cadre d'un **projet en Instrumentation Avancée** au département Mesures Physiques de Marseille, nous avons réalisé en **binôme** une **balance connectée** dont l'objectif était de **mesurer** une masse dans un intervalle compris entre 0 et 200g et de **transmettre** les données à une **interface Node-RED** via un **protocole MQTT**.

La balance s'appuie sur une **cellule de charge** associée à un **convertisseur/amplficateur HX711**, l'ensemble étant relié à un **ESP32**. L'exploitation du système, <ins>à l'exception de la **tare qui est effectuée directement via la console série**</ins>, est réalisée sur une **interface Node-RED**.

Ce projet se divise en deux axes de travail  : <ins>**programmation**</ins> et <ins>**métrologie**</ins>.


# Fonctionnalités 

- Tare de la balance avec une masse étalon de 100g.
  
- Bouton de peser pour la mesure d'une masse comprise entre 0 et 200g.
  
- Lecture & affichage de la témpérature à l'aide du capteur DHT11.

- Affichage de l'heure et de la date de la mesure.

- Background animé : dégradé *blanc -> gris*.
  
- Choix de l'affichage : **Balance étalonnée** ou **Balance classée**.
  
- Affichage formaté de la masse sur Node-RED: **m = [masse] ± [incertitude] g**.


# Matériels utilités

<p align="center">
  <img width="1362" height="620" alt="Capture d’écran 2025-10-20 à 22 24 05" src="https://github.com/user-attachments/assets/c5e84c0d-e4f9-4483-9fb4-bf41827d58ee" />
  <br>
  <em>Figure 1 – Illustration de l'assemblage de la balance</em>
  <br>
  <br>
</p>



<div align="center">
  
| Identification | Quantité | Principaux composants | 
|  :---:  |  :---:  | :---:  | 
| 1 | 1 | `Microcontrôleur ESP32` | 
| 2 | 1 | `Capteur de température DHT11` | 
| 3 | 1 | `Convertiseur & amplificateur HX711` | 
| 4 | 1 | `Cellule de charge` | 
| 5 | 2 | `BreadBoard` | 
| 6 | 1 | `Masses d'essais` | 

</div>
<br>
<br>


# Logiciels utilisés

<div align="center">

| Logiciels |  Description | 
|  :---:  |  :---:  |
| `Visual Studio Code &  PlatformIO` | Éditeur de code source développé par Microsoft| 
| `Mosquitto (protocole MQTT)` | Brocker open-source utilisant le protocole MQTT : collecte les données des capteurs | 
| `Node-RED (interface utilisateur)` | Outil de développment " low-code" : programmation visuelle basé sur des flux | 

</div>

<br>
<br>
<br>

> [!WARNING]
> En cas d’instabilité de la mesure, il suffit de redémarrer la carte ESP32, ce qui relancera automatiquement la tare à l’aide de la masse étalon de 100g.

