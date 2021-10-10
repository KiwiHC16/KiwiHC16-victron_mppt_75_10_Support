Work in progress

# Documentation

Ce plugin permet de recuperer les informations d'un MPPT Victron.

![image](https://user-images.githubusercontent.com/8549674/134874152-3f3604e7-d54e-4f51-98df-b5b13bd21c0e.png)

Les MPPT Victron possède un port applelé VE.Direct sur lequel on peut connecter un cable USB:

![iu](https://user-images.githubusercontent.com/8549674/136688462-14dac985-45f7-4b51-94a3-1fc031d51e7b.jpeg)

Ce plugin permet de lire en permanence les informations depuis le port USB:

![Capture d’écran 2021-10-10 à 10 29 56](https://user-images.githubusercontent.com/8549674/136688499-b78631fc-8247-40de-846f-2457bf440ddd.png)

Il est necessaire de créer un equipement par MPPT.

Ensuite il est important de définir les informations relative à la batterie:

![Capture d’écran 2021-10-10 à 10 32 01](https://user-images.githubusercontent.com/8549674/136688548-dcdff6ea-6336-4b9b-bc1f-21a8dcae07e6.png)

Suite à la creation d'un equipement MPPT, il faut relance le daemon du plugin.

# Changelog

10/10/2021:
- Ajout des caracteristique de la batterie

27/09/2021: 
- Version initiale soumise au market Jeedom.
- Testée avec un Victron MPPT 75 10

# Support

Ouvrez des issues dans https://github.com/KiwiHC16/victron_mppt_75_10_Support/issues si vous souhaitez du support.


