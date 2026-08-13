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

L'objectif est d'atteindre un taux de compression le plus élevé possible, en utilisant un moteur de 900 KV alimenté en 11.1V (soit environ 10 000 tr/min à vide) et la fabrication additive.

Deux architectures principales sont envisagées pour notre système dynamique : **Axiale** et **Centrifuge**. (Les architectures volumétriques comme le piston ou les lobes ont été écartées à ce stade en raison des frottements et des difficultés d'étanchéité propres à l'impression 3D plastique).

### 2.1 Analyse de l'Architecture Centrifuge
Un compresseur centrifuge utilise la force centrifuge pour accélérer l'air radialement avant de le ralentir dans un diffuseur (volute) pour augmenter sa pression statique.
*   **Avantages :** Très simple à concevoir et à imprimer en 3D en une seule pièce (rotor). Pas de frottement mécanique entre le rotor et le stator (seulement des jeux d'air).
*   **Inconvénients :** Pour obtenir un taux de compression important, un compresseur centrifuge nécessite des vitesses de rotation extrêmement élevées (souvent > 50 000 tr/min). À 10 000 tr/min, un seul étage fournira une pression très faible à moins d'augmenter drastiquement le diamètre du rotor, ce qui augmente le risque d'éclatement dû à la force centrifuge sur le plastique (PLA ou résine SLA).
*   **Multi-étage :** Réalisable, mais complexe à canaliser (l'air sort radialement et doit revenir au centre de l'étage suivant).

### 2.2 Analyse de l'Architecture Axiale
Un compresseur axial utilise une série d'ailettes tournantes (rotor) et fixes (stator) pour compresser l'air de manière graduelle le long de l'axe de rotation.
*   **Avantages :** Très bien adapté à la mise en série de multiples étages (multi-étagement). L'ajout d'étages augmente la pression totale sans augmenter la vitesse de rotation requise. De plus, son format tubulaire est facile à assembler autour de l'axe du moteur.
*   **Inconvénients :** Conception aérodynamique plus complexe (profil des pales). Impression des rotors plus délicate en FDM (supports nécessaires), mais réalisable avec une grande finesse grâce à la résine SLA.

### 2.3 Choix Final (Pré-étude)
Compte tenu de notre vitesse de rotation relativement faible (10 000 tr/min), l'approche la plus réaliste pour obtenir une *pression* significative est d'adopter une **architecture axiale multi-étages**. Un seul compresseur centrifuge tournant à cette vitesse se comporterait davantage comme un ventilateur que comme un compresseur de pression.

L'impression en **résine SLA** sera privilégiée pour les rotors et stators, garantissant un état de surface optimal (réduisant les pertes aérodynamiques) et une très bonne définition des bords d'attaque et de fuite des ailettes. Le carter externe pourra être réalisé en PLA pour des raisons de coût et de rigidité globale, et l'étanchéité assurée par des joints en TPU.

**Conclusion :** Nous partons sur la conception d'un **compresseur axial multi-étages** entraîné en prise directe par le moteur A2212.
