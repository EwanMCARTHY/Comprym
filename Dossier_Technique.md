# Plan du Dossier Technique : Projet Comprym

*(Ce fichier sert de brouillon et de trame pour le document final Google Docs).*

## Introduction
*(À rédiger : Présentation de l'ambition du projet, créer un compresseur 3D haute performance avec du matériel accessible).*

## Sommaire
*(Généré automatiquement à la fin)*

---

## 1. Cahier des charges

### 1.1. Contexte
*(À rédiger : Pourquoi ce projet ? Cadre amateur/étudiant/personnel, volonté de repousser les limites de l'impression 3D, etc.)*

### 1.2. Cahier des charges
*   **Moteur imposé :** Brushless Outrunner A2212 (900 KV).
*   **Alimentation :** Batterie LiPo 3S (11.1 V) - Vitesse max ~ 10 000 tr/min.
*   **Contraintes de fabrication :** Utilisation exclusive de l'impression 3D pour la mécanique fluide (SLA/Résine pour l'aérodynamisme et la précision, FDM/PLA/TPU pour la structure et l'étanchéité).
*   **Objectif principal :** Obtenir le taux de compression le plus élevé possible avec ce seul moteur.
*   **Sécurité :** Prévention de l'éclatement des pièces tournantes.

---

## 2. Étude Préliminaire et Architecture

### 2.1. Analyse des architectures possibles
*(Explication des raisons qui ont poussé à éliminer les compresseurs volumétriques (frottements/étanchéité FDM) et les compresseurs centrifuges mono-étagés (vitesse de 10 000 tr/min trop faible pour générer une bonne pression).*

### 2.2. Choix de l'architecture : Compresseur Axial Multi-étages
*(Justification du choix : capacité à additionner les taux de compression à chaque étage, excellente synergie avec la précision de l'impression SLA pour les pales, forme tubulaire adaptée au moteur).*

---

## 3. Modélisation Thermodynamique et Aérodynamique

### 3.1. Théorie et Équations d'Euler
*(Rappels des équations des turbomachines, triangles des vitesses).*

### 3.2. Dimensionnement préliminaire
*(Calcul de l'angle des pales, de la vitesse d'écoulement, estimation du nombre d'étages requis pour maximiser la puissance de 150W du moteur).*

### 3.3. Sélection des profils aérodynamiques
*(Choix des profils NACA pour le rotor et le stator).*

---

## 4. Conception Mécanique (CAO)

### 4.1. Modélisation du Rotor et du Stator
*(Conception des disques, moyeux et ailettes, respect des tolérances radiales d'impression).*

### 4.2. Intégration du Moteur A2212
*(Conception de l'accouplement moteur-rotor, gestion de l'alignement).*

### 4.3. Carter et Étanchéité
*(Assemblage de la coque externe, utilisation de joints TPU).*

### 4.4. Analyse des Contraintes Mécaniques
*(Validation de la résistance à la force centrifuge des pales en résine à 10 000 tr/min).*

---

## 5. Fabrication Additive

### 5.1. Matériaux retenus et Paramètres de tranchage
*(SLA pour les aubages, PLA pour le carter, réglages d'impression, orientation pour éviter la rupture par clivage).*

### 5.2. Post-traitement et Assemblage
*(Nettoyage de la résine, ajustements, équilibrage dynamique du rotor).*

---

## 6. Banc d'Essai et Validation Expérimentale

### 6.1. Protocole de Test et Sécurité
*(Mise en place d'un variateur (ESC), mesure du courant, protections physiques).*

### 6.2. Résultats : Débit, Pression et Échauffement
*(Tableaux et graphiques de relevés expérimentaux au manomètre).*

### 6.3. Confrontation Théorie / Pratique
*(Analyse des écarts, rendement global estimé, fuites, pertes aérodynamiques).*

---

## Conclusion
*(Bilan du projet, atteinte des objectifs, limites du plastique, pistes d'amélioration pour une V2).*

## Annexes
*(Datasheet moteur, scripts de calcul, plans de détail).*
