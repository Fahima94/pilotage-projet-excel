# Pilotage de saison — production touristique

Classeur de pilotage d'une saison de tour-opérateur, calé sur mon expérience réelle chez Partir Pas Cher (Switch PPC France) : production interne, achats hôteliers et aériens, revenue management, gestion de crise.

Le portefeuille dépassait la dizaine de millions d'euros d'engagement annuel, avec des contrats hôteliers à sept chiffres sur les destinations phares — République dominicaine (destination lancée par le fondateur, sans marché français à l'époque), Égypte, Turquie, Thaïlande, Dubaï, Costa Rica.

## Onglets
- **Lecture** : contexte, mode d'emploi, ce que le fichier remplace.
- **Rétroplanning** : 12 étapes de la négociation des contrats au bilan, Gantt sur 30 semaines.
- **Départs** : sièges achetés et vendus, prix moyen, coût, marge, taux, sièges restants.
- **Contrats hôtels** : 12 hôtels, chambres par départ, départs par an, coût de la chambre, engagement annuel, marge séjour, alerte et action.
- **Cellule invendus** : le dispositif créé pour écouler les places restantes à J-7 — push clients fidèles, push ADV à J-3, avenant hôtelier, baisse de prix — avec CA récupéré et reste.
- **Rotations & legs** : optimisation des legs aller/retour et économie annuelle extrapolée.
- **Ventes** : les trois canaux (site, agences, plateforme) consolidés par Power Query.
- **Budget** : 7 postes, engagé, facturé, disponible, alerte à 90 %.
- **Risques** : surbooking, release dates, annulation de vol, défaillance hôtelière.
- **Incidents** : registre de crise, reprotections, coût et délai de prise en charge, suites juridiques.
- **Tableau de bord** : remplissage, marge, engagement hôtelier, contrats à plus d'un million, sièges récupérés, CA récupéré.
- **Revue DAF** : point hebdomadaire avec la direction financière.

## Ce que le fichier automatise
- Engagement annuel d'un contrat : chambres par départ x départs par an x nuits x coût/nuit
- Fin d'étape : WORKDAY(début; durée-1)
- Alerte hôtel : rouge si marge séjour négative ou garantie ferme sous 60 % de taux ; orange au-dessus de 85 %
- Reste à écouler et résultat net d'une action de reprotection
- Taux de récupération : sièges écoulés / sièges invendus

## Power Query
power-query.txt contient le code M de consolidation des trois exports de ventes et de nettoyage des libellés.

## Le récit à tenir en entretien
1. Le problème : des contrats hôteliers fermes à sept chiffres, des places d'avion achetées d'avance, et l'obligation de tout vendre avant le départ.
2. Ce que je faisais : achat des hôtels avec mon équipe, places d'avion avec l'acheteur aérien, combinaison en séjours viables, puis arbitrage chaque semaine avec l'ADV.
3. Ce que j'ai construit : une cellule de reprotection des invendus à trois leviers — push clients fidèles, push ADV à J-3, avenant au contrat hôtelier quand la destination ne partait plus.
4. Le résultat : sur huit rotations premium, 220 sièges récupérés sur 387, 318 k€ de CA, 301 k€ net, 57 % de récupération.
5. La crise : trois reprotections en trois ans, 278 clients, 65 500 € engagés, et un registre qui garde la trace des décisions et des suites juridiques.

## Auteure
Fahima Behillil — chargée de projet IA & automatisation
