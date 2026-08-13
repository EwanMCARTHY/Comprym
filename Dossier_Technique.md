# Dossier Technique : Projet Comprym

**Objectif :** Conception, fabrication par impression 3D et essai d'un compresseur basé sur un moteur brushless A2212, visant le taux de compression le plus élevé possible.

---

## 1. Cahier des charges et Contraintes

### 1.1 Matériel imposé
*   **Moteur :** Brushless Outrunner A2212
*   **Constante de vitesse (KV) :** 900 KV
*   **Tension d'alimentation :** 11.1 V (Batterie LiPo 3S)
*   **Vitesse de rotation théorique à vide :** 900 * 11.1 = 9 990 tr/min (~ 10 000 tr/min)
*   **Puissance estimée :** ~ 150 W

### 1.2 Moyens de fabrication
L'ensemble des pièces spécifiques devra être réalisable avec les technologies d'impression 3D suivantes :
*   **FDM (Dépôt de fil fondu) :** PLA, TPU
*   **SLA (Stéréolithographie) :** Résine (permet une très haute précision et un état de surface lisse, idéal pour l'aérodynamisme, mais potentiellement plus cassant).

### 1.3 Contraintes techniques
*   **Thermiques :** La compression d'un gaz génère de la chaleur. Le PLA se ramollit autour de 60°C. Il faudra surveiller l'échauffement ou utiliser la résine pour les pièces les plus exposées si elle résiste mieux à la chaleur.
*   **Mécaniques :** La force centrifuge sur les pièces tournantes à 10 000 tr/min impose des contraintes de traction importantes. Le matériau doit résister à l'éclatement.
*   **Moteur unique :** Un seul moteur A2212 doit entraîner l'ensemble du système.
*   **Étanchéité :** Le TPU pourra être utilisé pour concevoir des joints sur mesure.

---

## 2. Conception Préliminaire : Choix de l'Architecture

*(En cours de rédaction avec l'utilisateur...)*
