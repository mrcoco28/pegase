Voici un exemple de fichier README pour votre projet basé sur le code que vous avez fourni :

---

# Projet STM32 avec Capteurs et Affichage LED

## Description
Ce projet utilise un microcontrôleur STM32 pour interagir avec des capteurs d'environnement et un affichage LED à travers des manipulations de GPIO et des communications SPI.

## Table des matières
- [Description](#description)
- [Dépendances](#dépendances)
- [Installation](#installation)
- [Utilisation](#utilisation)
- [Licence](#licence)

## Dépendances
Ce projet nécessite les bibliothèques suivantes :
- [STM32Cube HAL](https://www.st.com/en/embedded-software/stm32cube-mcu-packages.html) : Bibliothèque de support pour les microcontrôleurs STM32.
- [MAX7219 Library](https://github.com/username/max7219_lib) : Bibliothèque pour contrôler les matrices de LED MAX7219.
- [IKS01A3 Motion Sensors Library](https://www.st.com/en/ecosystems/iks01a3.html) : Bibliothèque pour les capteurs de mouvement IKS01A3.
- [IKS01A3 Environmental Sensors Library](https://www.st.com/en/ecosystems/iks01a3.html) : Bibliothèque pour les capteurs d'environnement IKS01A3.

## Installation
1. **Clonage du Dépôt :**
   ```bash
   git clone https://github.com/votre/répertoire.git
   ```
2. **Configuration du Projet :**
   - Ouvrez le projet dans STM32CubeIDE.
   - Configurez et générez le projet pour votre microcontrôleur STM32 spécifique.

## Utilisation
Assurez-vous de connecter correctement tous les périphériques et capteurs avant d'exécuter le programme sur votre matériel cible.

1. **Compilation et Flash :**
   - Compilez le projet dans STM32CubeIDE.
   - Flasher le binaire généré sur le microcontrôleur.

2. **Exécution du Programme :**
   - Alimentez le microcontrôleur et observez la console série pour les messages de débogage.
   - Utilisez les boutons BTN1 et BTN2 pour interagir avec les fonctionnalités spécifiques du programme.

3. **Affichage sur les LED MAX7219 :**
   - Lorsque le programme est en cours d'exécution, les capteurs d'environnement détectent la température et l'humidité.
   - Ces valeurs sont affichées sur les matrices de LED MAX7219 connectées.

## Licence
Ce logiciel est sous licence selon les termes que vous pouvez trouver dans le fichier LICENSE situé à la racine de ce projet. Si aucun fichier LICENSE n'est fourni, le logiciel est fourni TEL QUEL.

---

Assurez-vous d'adapter les liens des dépendances aux ressources spécifiques que vous utilisez et de fournir plus de détails sur les configurations matérielles spécifiques et les procédures d'installation si nécessaire. Ce README devrait permettre à tout nouvel utilisateur de comprendre rapidement comment installer, configurer et utiliser votre projet sur un microcontrôleur STM32.
