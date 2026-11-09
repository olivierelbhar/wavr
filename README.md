# WAVR

**Synthèse granulaire à couches, dans le navigateur.** Charge un son, et sculpte-le en grains : fige un instant, étire-le, superpose plusieurs lectures du même son jusqu'à obtenir une texture qu'on n'a jamais entendue.

**▶ Essayer WAVR : https://olivierelbhar.github.io/wavr/**

WAVR fait partie d'une collection d'outils audio vulgarisés (BREAKR, SCANR, TRACR, DRIFTR…) : une technique de production, un outil, une interface qui l'explique en jouant.

> Statut : prototype en cours. Tout tient dans un seul fichier HTML, sans dépendance ni serveur.

## Essayer

Ouvre `index.html` dans un navigateur récent (Chrome, Safari, Firefox), clique sur **▶ Jouer**. Un son d'exemple (un break et une nappe) est déjà chargé ; tu peux charger ou glisser ton propre fichier audio. Rien n'est envoyé nulle part : tout se passe dans le navigateur.

## Le problème

La synthèse granulaire produit des sons qu'aucune autre technique ne donne, mais les outils existants (plugins, machines comme le Torso S-4, apps comme GrainHeads) s'adressent à des sound designers qui maîtrisent déjà le vocabulaire : têtes de lecture, spray, enveloppes. Pour un curieux, la porte d'entrée est fermée.

## Les choix produit

- **Des familles plutôt que des « têtes ».** Le multi-têtes existe ailleurs ; WAVR le présente comme des couches nommées (Nuage, Gel, Glitch, Rewind, Octaves, Hasard) qu'on allume et qu'on superpose. Chaque couche garde ses réglages en mémoire.
- **Chaque réglage s'explique en une phrase**, au lieu d'un manuel.
- **Zéro installation.** Un lien, un clic, du son. C'est ce qui rend l'outil partageable.
- **Des échelles pensées pour l'oreille**, pas pour la technique : le défilement est logarithmique pour donner de la place aux ralentis extrêmes (jusqu'à 1/1000), là où se trouvent les sons intéressants.

## Fonctionnalités

- 7 couches granulaires indépendantes, chacune avec sa tête de lecture
- Par couche : taille, densité, dispersion, défilement (gel, ralenti, inversé), balayage aléatoire, hauteur, désaccord, inversion, stéréo, enveloppe, irrégularité, volume
- Par couche, une chaîne d'effets : saturation → flanger → phaser → écho → reverb
- Réglages mémorisés dans le navigateur

## Feuille de route

- [ ] Enregistrer : export WAV, puis vidéo courte pour le partage
- [ ] Modulations (LFO assignables sur la position et la taille)
- [ ] Jouer au clavier, une note = une couche transposée
- [ ] Version plugin (VST/AU) pour les couches les plus utilisées

## Technique

HTML, CSS et JavaScript sans framework. Le son passe par la Web Audio API : chaque grain est un court extrait du fichier, joué avec sa propre enveloppe, sa hauteur et sa position stéréo.

---

Un projet d'[Olivier Elbhar](https://olivierelbhar.com), product manager et producteur.
