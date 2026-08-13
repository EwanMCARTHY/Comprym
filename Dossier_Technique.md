# Plan du Dossier Technique : Projet Comprym

Ce document servira de base (brouillon) pour le document Google Docs final. Voici le plan détaillé de notre dossier technique, couvrant toutes les étapes de l'ingénierie du compresseur.

---

## 1. Introduction
*   **1.1. Contexte du projet** : Création d'un compresseur imprimé en 3D autour d'un moteur standard de modélisme.
*   **1.2. Objectifs** : Atteindre un taux de compression maximal avec les moyens de fabrication additive disponibles.
*   **1.3. Indicateurs de réussite** : Pression statique cible, rendement, intégrité mécanique.

## 2. Cahier des charges et Contraintes
*   **2.1. Contraintes motrices** : Spécifications du moteur brushless A2212 (900 KV, ~150W) et de l'alimentation (LiPo 3S 11.1V).
*   **2.2. Contraintes de fabrication** : Capacités et limites de l'impression 3D FDM (PLA/TPU) et SLA (Résine). Tolérances dimensionnelles.
*   **2.3. Contraintes opérationnelles** : Résistance thermique (échauffement lié à la compression) et résistance mécanique (force centrifuge à ~10 000 tr/min).

## 3. Étude et Conception Préliminaire
*   **3.1. Analyse des architectures possibles** : Comparatif (Centrifuge, Axial, Volumétrique).
*   **3.2. Justification du choix architectural** : Explication du choix de l'**architecture axiale multi-étages** (adaptation aux 10 000 tr/min, viabilité en impression 3D, addition des taux de compression).

## 4. Dimensionnement Thermodynamique et Aérodynamique
*   **4.1. Théorie d'Euler pour les turbomachines** : Définition de l'échange d'énergie entre le fluide et le rotor.
*   **4.2. Calcul des triangles de vitesse** : Modélisation des vecteurs vitesse (absolue, relative, d'entraînement) en entrée et sortie de rotor/stator.
*   **4.3. Détermination des paramètres aérodynamiques** : Angles des pales, section de passage, et estimation du nombre d'étages requis pour la pression cible.

## 5. Conception Mécanique Détaillée (CAO)
*   **5.1. Dimensionnement du moyeu, du rotor et du carter (stator)**.
*   **5.2. Tolérances et jeux de fonctionnement** : Définition des jeux entre les pales tournantes et le carter pour limiter les fuites sans frottement.
*   **5.3. Intégration électromécanique** : Montage du moteur A2212, accouplement sur l'axe, gestion des efforts axiaux (roulements supplémentaires).
*   **5.4. Système d'étanchéité** : Utilisation du TPU pour les joints statiques.

## 6. Fabrication Additive
*   **6.1. Choix finaux des matériaux** : Répartition des pièces entre Résine (profils aéro) et PLA (structure).
*   **6.2. Paramètres d'impression** : Orientation des pièces (pour contrer le délaminage sous force centrifuge), densité de remplissage, gestion des supports.
*   **6.3. Post-traitement** : Nettoyage, lissage, équilibrage dynamique du rotor, et assemblage final.

## 7. Protocole d'Essai et Validation
*   **7.1. Présentation du banc d'essai** : Instrumentation (Manomètre, anémomètre/débitmètre, sonde de température), procédure de test en sécurité.
*   **7.2. Résultats expérimentaux** : Relevés de pression à débit nul, relevés de débit, courbes caractéristiques, et suivi thermique.
*   **7.3. Analyse critique** : Comparaison entre les résultats théoriques (Partie 4) et pratiques. Identification des sources de pertes (fuites, frottements fluides).

## 8. Conclusion et Perspectives
*   **8.1. Bilan du projet** : Atteinte des objectifs initiaux.
*   **8.2. Pistes d'amélioration (Version 2)** : Optimisations aérodynamiques, autres moteurs, autres matériaux.
