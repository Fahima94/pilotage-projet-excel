# Pilotage de saison — production touristique

Classeur qui formalise le pilotage d'une saison de tour-opérateur : trois départs par semaine vers l'Égypte et la Turquie, 180 places hebdomadaires, une équipe de sept personnes, un portefeuille de contrats hôteliers en ferme et en allotement.

## Onglets
- **Lecture** : contexte, mode d'emploi, ce que le fichier remplace.
- **Rétroplanning** : 12 étapes de la négociation des contrats au bilan, Gantt sur 30 semaines.
- **Départs** : sièges achetés et vendus, prix moyen, coût, marge, taux et sièges restants.
- **Contrats hôtels** : 12 hôtels, garanties, prix de revient chambre, marge, alerte et action (renégocier, baisser ou augmenter la garantie).
- **Rotations & legs** : optimisation des legs aller/retour, économie réalisée en passant des clients de 7 à 15 nuits.
- **Ventes** : les trois canaux (site, agences, plateforme) consolidés par Power Query.
- **Budget** : 7 postes, engagé, facturé, disponible, alerte à 90 %.
- **Risques** : surbooking, release dates, annulation de vol, défaillance hôtelière.
- **Incidents** : registre de crise, reprotections, coût et délai de prise en charge, suites juridiques.
- **Tableau de bord** : remplissage, sièges restants, marge, contrats en alerte, économie legs, clients reprotégés.
- **Revue DAF** : point hebdomadaire avec la direction financière.

## Ce que le fichier automatise
- Fin d'étape : WORKDAY(début; durée-1)
- Statut : Terminé / En retard / À risque / Dans les temps
- Alerte hôtel : rouge si marge négative ou garantie ferme sous 60 % de taux ; orange au-dessus de 85 %
- Marge par départ : (prix moyen - coût) x sièges vendus
- Économie de legs : pax en 15 nuits x 2 legs x coût du leg

## Power Query
power-query.txt contient le code M de consolidation des trois exports de ventes et de nettoyage des libellés.

## Le récit à tenir en entretien
1. Le problème : trois canaux de vente, des prix qui bougent, des garanties hôtelières à tenir et des release dates à ne pas dépasser.
2. Ce que je faisais : recalcul à la main chaque lundi, alertes hôtel par hôtel, arbitrages en revue DAF.
3. Ce que l'outil change : les chiffres se rafraîchissent seuls, la réunion sert à décider.
4. La crise : trois reprotections en trois ans, 278 clients, 65 500 € engagés — le registre garde la trace des décisions et des suites juridiques.

## Auteure
Fahima Behillil — chargée de projet IA & automatisation
