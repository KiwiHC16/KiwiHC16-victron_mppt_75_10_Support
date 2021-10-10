Work in progress

# Documentation

Ce plugin permet de recuperer les informations d'un MPPT Victron.

![image](https://user-images.githubusercontent.com/8549674/134874152-3f3604e7-d54e-4f51-98df-b5b13bd21c0e.png)

Les MPPT Victron possède un port applelé VE.Direct sur lequel on peut connecter un cable USB:

![iu](https://user-images.githubusercontent.com/8549674/136688462-14dac985-45f7-4b51-94a3-1fc031d51e7b.jpeg)

Ce plugin permet de lire en permanence les informations depuis le port USB:

![Capture d’écran 2021-10-10 à 10 29 56](https://user-images.githubusercontent.com/8549674/136688499-b78631fc-8247-40de-846f-2457bf440ddd.png)

mais ne controle en rien le systeme. La configuration du module Victron MPPT se fait par l intermediaire de l application mobile en bluetooth.

Il est necessaire de créer un equipement par MPPT.

Ensuite il est important de définir les informations relative à la batterie:

![Capture d’écran 2021-10-10 à 10 32 01](https://user-images.githubusercontent.com/8549674/136688548-dcdff6ea-6336-4b9b-bc1f-21a8dcae07e6.png)

* Autocalibration: Lorsque le MPPT passe en Float le plugin considere que la batterie est pleine, passe la valeur Capacity à la valeur Capacity Max.
* Battery Capacity: Capacité constructeur en Wh. Si vous avez une batterie 12V à 14Ah ca nous donne 12*14 = 168
* Battery Usage Max: Indiquez l energie maximum que vous souhaitez recuperer de la batterie. 0.75 pour 75%. 168*75% = 126 Wh.
* Rendement Charge: Indique le ratio entre l energie injectée et celle effectivement stockée dans la batterie. Ici 1 => 100%.
* Rendement Decharge: Indique le ratio entre l energie stockée dans la batterie et celle effectivement restituée. Ici 1 => 100%.
* Ces informations permettent de calculer et renseigner l'estimation de l 'état de charge de la batterie: Commande Capacity et Commande SOC.

Exemple d'utilisation:

Batterie de moto de 12V à 14Ah, soit 168Wh. Max 4.2A de charge CC (Courant Constant), 13.6V-13.8V en Float et 14.6V Max en charge.

N'hésitez pas à lire: Wikipedia (https://fr.wikipedia.org/wiki/Batterie_au_plomb).

La configuration faite dans le MPPT:
![Capture d’écran   2021-10-09 à 11 19 46](https://user-images.githubusercontent.com/8549674/136689051-5cfd121d-3fe4-4fc9-ba60-77a072d97035.jpeg)


![Capture d’écran   2021-10-09 à 11 20 27](https://user-images.githubusercontent.com/8549674/136689053-2e9c1e6c-e8f2-47de-87ee-76bb162bcbe6.jpeg)


Suite à la creation d'un equipement MPPT, il faut relance le daemon du plugin.

# Changelog

10/10/2021:
- Ajout des caracteristique de la batterie

27/09/2021: 
- Version initiale soumise au market Jeedom.
- Testée avec un Victron MPPT 75 10

# Support

Ouvrez des issues dans https://github.com/KiwiHC16/victron_mppt_75_10_Support/issues si vous souhaitez du support.


