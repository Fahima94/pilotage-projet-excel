# Pilotage de saison — production touristique

Classeur qui formalise le pilotage d'une saison de tour-opérateur : trois départs par semaine vers l'Égypte et la Turquie, 180 places hebdomadaires, une équipe de sept personnes.

## Onglets
- **Lecture** : contexte, mode d'emploi, ce que le fichier remplace.
- **Rétroplanning** : 12 étapes de la négociation des contrats au bilan, Gantt sur 30 semaines.
- **Ventes** : les ventes des trois canaux (site, agences, plateforme), consolidées par Power Query.
- **Départs** : sièges achetés et vendus, prix moyen, coût, marge, taux et sièges restants par départ.
- **Budget** : 7 postes, engagé, facturé, disponible, alerte à 90 %.
- **Risques** : surbooking, release dates, annulation de vol, défaillance hôtelière.
- **Tableau de bord** : remplissage, sièges restants, marge, départs sous 50 %, vue par destination.

## Ce que le fichier automatise
- Fin d'étape : WORKDAY(début; durée-1)
- Statut : Terminé / En retard / À risque / Dans les temps, calculé sur TODAY()
- Taux de remplissage et sièges restants par départ
- Marge par départ : (prix moyen - coût) x sièges vendus
- Criticité des risques : probabilité x impact

## Power Query
Le fichier power-query.txt contient le code M : consolidation des trois exports de ventes, nettoyage des libellés de destination et de canal, typage des dates et des montants. À coller dans l'éditeur avancé.

## Le récit à tenir en entretien
1. Le problème : trois exports, des prix qui bougent, des release dates à ne pas dépasser.
2. Ce que je faisais : recalcul à la main chaque lundi, arbitrages en réunion.
3. Ce que l'outil change : les chiffres se rafraîchissent seuls, le lundi sert à décider.

## Auteure
Fahima Behillil — chargée de projet IA & automatisation
