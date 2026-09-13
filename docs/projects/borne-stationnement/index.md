# Borne de stationnement intelligente

**Projet 2 du département R&D.** Borne de paiement pour le stationnement urbain, combinant matériel embarqué et logiciel.

## Objectif

Concevoir une borne capable de gérer le stationnement urbain de bout en bout : détecter un véhicule, encaisser le paiement (carte ou mobile money) et remonter les transactions vers un backend cloud consultable via un tableau de bord opérateur.

Le projet s'appuie, pour la partie détection, sur une approche caméra **ANPR** (*Automatic Number Plate Recognition* — lecture automatique de plaque) en péage à flux libre, plutôt que sur une barrière physique classique. Pour la connectivité, la borne réutilise la brique **LoRa** déjà étudiée dans le [Projet 1](../dongle-multisupport/index.md), afin de remonter les données de stationnement même dans les zones peu couvertes.

!!! info "Section à préciser ensemble"
    Le scénario détaillé (parcours utilisateur, choix définitif entre ANPR et détection par capteur, mode de paiement retenu, architecture logicielle) reste à finaliser. Cette page sera complétée au fur et à mesure des décisions.

## Grandes briques envisagées

- **Détection véhicule** : caméra ANPR (lecture de plaque), en péage à flux libre
- **Paiement** : carte bancaire et/ou mobile money
- **Connectivité** : module LoRa (SX1276) pour la remontée des données
- **Alimentation** : batterie Li-ion 18650 rechargeable, avec capteur de tension pour le suivi de charge
- **Backend cloud** : centralisation des transactions
- **Dashboard opérateur** : suivi des places, des paiements et de l'état des bornes

## Statut

⚪ **À l'étude** — le scénario détaillé et l'architecture restent à définir ; le chiffrage du budget (BOM) est en cours (voir les [objectifs de la semaine](../../index.md)).
