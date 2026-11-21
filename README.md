# Pilotage de projet — tableau de bord Excel

Classeur de pilotage d'un déploiement sur trois sites, en six mois. Il montre la chaîne complète : donnée brute, préparation, puis pilotage.

## Onglets
- Lecture : objet du fichier, mode d'emploi, procédure Power Query.
- Données : 18 interventions brutes, volontairement imparfaites (casse, espaces, accents).
- Planning : 15 tâches, WBS, durées en jours ouvrés, fin calculée, statut automatique, Gantt sur 26 semaines.
- Budget : 8 postes, engagé, facturé, disponible, taux de consommation, alerte à 90 %.
- Risques : probabilité × impact, criticité et niveau automatiques.
- Tableau de bord : 8 indicateurs et une vue par phase, tous reliés aux autres onglets.
- Comitologie : instances, décisions, actions.

## Formules clés
- Fin de tâche : WORKDAY(début; durée-1)
- Statut : IF(%>=1;"Terminé";IF(TODAY()>fin;"En retard";...))
- Avancement pondéré : SUMPRODUCT(durées; %)/SUM(durées)
- Criticité : probabilité × impact

## Power Query
Le fichier power-query.txt contient le code M à coller dans l'éditeur avancé : suppression des lignes vides, nettoyage du texte, typage des colonnes, tri par date.

## Auteure
Fahima Behillil — chargée de projet IA & automatisation
