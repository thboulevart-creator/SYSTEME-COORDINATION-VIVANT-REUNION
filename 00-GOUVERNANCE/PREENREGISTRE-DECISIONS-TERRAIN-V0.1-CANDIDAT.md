# PREENREGISTRE-DECISIONS-TERRAIN-V0.1-CANDIDAT

**Date de préenregistrement :** 24 septembre 2026  
**Dépôt :** `thboulevart-creator/SYSTEME-COORDINATION-VIVANT-REUNION`  
**Branche :** `main`  
**HEAD parent :** `8f4ad1521c0d4dff389dd5969ba03a50292cc893`  
**Statut :** `CANDIDAT — AVANT TOUTE DONNEE TERRAIN`  
**Objet :** fixer à l'avance les règles permettant de sélectionner, éliminer ou déclarer inconclusifs les problèmes candidats du terrain T0.

---

# 0. Rôle de ce préenregistrement

Ce document existe pour empêcher une sélection a posteriori du problème qui correspondrait le mieux à la vision du projet après lecture des données.

Il complète :

- `06-TERRAIN/PROTOCOLE-CARTOGRAPHIE-TERRAIN-V0.1-CANDIDAT.md`
- les six instruments `06-TERRAIN/INSTRUMENTS-V0.1/`
- `00-GOUVERNANCE/CHECKPOINT-INSTRUMENTS-TERRAIN-V0.1.md`

Il ne remplace pas leurs règles de preuve, d'éthique, de confidentialité ou de qualification des frictions.

## Principe directeur

Les données terrain doivent pouvoir conduire aussi bien à :

- sélectionner un problème ;
- montrer qu'un problème imaginé n'existe pas de façon significative ;
- montrer que la cause est non logicielle ;
- constater qu'un outil existant suffit ;
- conclure `INCONCLUSIVE` ;
- conclure `C0_NO_BUILD`.

**Sélectionner un problème ne signifie jamais sélectionner une solution logicielle.**

---

# 1. Gel des règles

À partir de la première donnée terrain valide :

> **aucun seuil, critère de sélection, critère d'élimination, métrique principale, taille maximale d'échantillon ou règle d'arrêt défini ici ne peut être modifié silencieusement.**

Toute modification ultérieure nécessite un document séparé :

`AMENDEMENT-PREENREGISTRE-DECISIONS-TERRAIN-<VERSION>.md`

contenant obligatoirement :

1. date et heure ;
2. HEAD précédent ;
3. règle modifiée ;
4. justification ;
5. données déjà observées au moment de l'amendement ;
6. risque de biais introduit ;
7. analyses conservées selon l'ancien seuil ;
8. analyses produites selon le nouveau seuil.

Un amendement ne réécrit jamais l'historique.

---

# 2. Problèmes candidats préenregistrés

- `C1_ORIENTATION_CITOYENNE`
- `C2_FOURRIERE_ASSOCIATION_F6_F7`
- `C3_ASSOCIATION_FA`
- `C4_TRACABILITE_CONTINUITE`
- `C5_AUTRE_PROBLEME`
- `C0_NO_BUILD`

Un seul problème principal pourra être sélectionné au gate de décision suivant T0.

Les autres pourront rester :

- `SECONDAIRE`
- `ELIMINE`
- `INCONCLUSIVE`
- `NON_PROBLEME`

mais ne seront pas ajoutés au premier vertical slice.

---

# 3. Définitions transversales

## 3.1 Cas indépendant

Deux observations ne sont indépendantes que si elles ne décrivent pas exactement le même événement ou la même chaîne de communication.

Deux acteurs racontant les deux côtés du même transfert constituent :

- **un seul cas** ;
- mais **deux rôles concordants**.

## 3.2 Conséquence observable

Sont admissibles :

- délai mesuré ou estimé explicitement ;
- relance ;
- ressaisie ;
- mauvaise orientation ;
- erreur ;
- information perdue ;
- responsabilité ambiguë ;
- séjour prolongé ;
- opportunité de transfert manquée ;
- abandon du parcours ;
- action potentiellement risquée ;
- travail humain supplémentaire.

Une irritation ou préférence sans conséquence n'est pas suffisante.

## 3.3 Cause disqualifiante pour une intervention de coordination

Un problème peut être réel mais être **disqualifié comme cible du système** si sa cause dominante est démontrée comme :

- `CAPACITE_PHYSIQUE` — absence réelle de place compatible ;
- `JURIDIQUE` — règle ou habilitation empêchant l'action ;
- `FINANCEMENT` — absence de budget ou moyens ;
- `RECRUTEMENT` — absence réelle de familles d'accueil / bénévoles / personnels ;
- `EXISTANT_SUFFISANT` — un outil ou processus existant résout déjà suffisamment le problème ;
- `ABSENCE_PROPRIETAIRE_PROBLEME` — aucun acteur responsable ne souhaite ou ne peut porter l'amélioration.

Ces causes n'annulent pas l'observation. Elles changent la décision autorisée.

## 3.4 Résultat `INCONCLUSIVE`

`INCONCLUSIVE` signifie :

- données contradictoires ;
- couverture insuffisante ;
- effet possible mais non attribuable ;
- seuil de sélection et seuil d'élimination tous deux non atteints à la taille maximale prévue.

`INCONCLUSIVE` n'autorise jamais le développement.

---

# 4. Taille maximale du terrain T0 avant décision

Ces plafonds empêchent une recherche indéfinie jusqu'à obtention du résultat souhaité.

## Axe A

- objectif initial : 8 sessions valides ;
- plafond T0 : **12 sessions valides** ;
- minimum : au moins 2 scénarios couverts ;
- scénario principal pour `C1` : `A1_CHIEN_TROUVE`.

## Axe B

- plafond T0 : **8 entretiens opérationnels valides** ;
- avec, si accès possible :
  - au moins 1 rôle fourrière / EPCI ;
  - au moins 2 structures receveuses ;
  - au moins 2 perspectives famille d'accueil / gestion FA ;
  - autres rôles uniquement si nécessaires à une frontière observée.

## Axe C

- objectif initial : 5 dossiers ;
- plafond T0 : **10 dossiers anonymisés reconstructibles ou partiellement reconstructibles** ;
- au moins 1 dossier avec transfert inter-structures si accessible.

## Extension

Aucune extension générale au-delà de ces plafonds.

Si un candidat reste `INCONCLUSIVE`, une extension ultérieure nécessitera une décision spécifique nommant exactement :

- l'inconnue ;
- le nombre maximal d'observations supplémentaires ;
- la raison pour laquelle elles peuvent réellement trancher.

---

# 5. Baseline commune

Le terrain T0 est aussi la mesure de référence.

Pour toute intervention future, les indicateurs avant / après devront utiliser les mêmes définitions.

## Mesures communes

- temps ;
- nombre d'acteurs ;
- nombre de canaux ;
- nombre de recherches ;
- nombre de messages / appels ;
- nombre de relances ;
- nombre de ressaisies ;
- nombre de systèmes / supports ;
- nombre de statuts ambigus ;
- prochaine action identifiable ou non ;
- conséquence opérationnelle ;
- temps humain lorsque raisonnablement estimable.

Les métriques spécifiques sont définies par candidat ci-dessous.

---

# 6. C1 — ORIENTATION CITOYENNE

## Question

Un humain non initié peut-il atteindre rapidement et correctement la bonne action sans connaître préalablement l'organisation institutionnelle ?

## Preuve nécessaire

Au minimum :

- sessions Axe A valides ;
- comportement observé, pas seulement opinion ;
- scénario `A1_CHIEN_TROUVE` représenté ;
- validation documentaire ou opérationnelle de ce qui constitue l'action correcte ;
- si possible, confirmation par au moins un acteur opérationnel que les mauvaises orientations observées existent réellement hors simulation.

## Baseline

Par session :

- `TEMPS_ORIENTATION_CORRECTE`
- `ACTEUR_FINAL_CORRECT`
- `PROCHAINE_ETAPE_COMPRISE`
- `NOMBRE_SITES_VISITES`
- `NOMBRE_CULS_DE_SAC`
- `ACTION_INCORRECTE_OU_RISQUEE`
- `BESOIN_D_AIDE_EXTERNE`

## Métrique principale

`TAUX_ECHEC_ORIENTATION_A1`

Un échec A1 est défini par au moins un de ces événements :

- acteur final incorrect ;
- abandon ;
- absence d'orientation correcte après 10 minutes ;
- action incorrecte ou potentiellement risquée étayée ;
- impossibilité de déterminer la prochaine étape.

## Métriques secondaires

- médiane `TEMPS_ORIENTATION_CORRECTE` ;
- sites visités ;
- changements de stratégie ;
- contradictions rencontrées ;
- dépendance à une aide externe ;
- blocage linguistique.

## Signal de sélection

`C1` devient **sélectionnable** si :

1. sur les 8 premières sessions A1 valides, au moins **3** sont des échecs selon la définition ci-dessus ;

**OU**, si le lot A1 est étendu jusqu'au plafond,

2. au moins **un tiers** des sessions A1 valides sont des échecs ;

**ET**

3. au moins une conséquence autre qu'une simple préférence est observée.

La confirmation d'appels mal orientés par un acteur opérationnel renforce la preuve mais n'est pas requise pour qualifier la friction citoyenne.

## Signal d'élimination

`C1` est éliminé comme problème principal si :

- au moins 7 des 8 premières sessions A1 atteignent l'action correcte en moins de 10 minutes ;
- aucune action risquée n'est observée ;
- la prochaine étape est comprise dans au moins 7/8 cas ;
- aucun signal opérationnel crédible ne montre une mauvaise orientation récurrente.

## Cause disqualifiante

Même si `C1` est réel, une nouvelle couche d'orientation est disqualifiée si :

- une information publique erronée unique explique l'essentiel du problème et peut être corrigée à la source ;
- StopErrance ou un autre service existant couvre déjà correctement le parcours une fois son contenu réel connu ;
- le problème résulte principalement d'indisponibilités physiques, non de l'orientation.

## Taille maximale

12 sessions Axe A valides pour T0.

## Stop rule

Arrêt de collecte pour `C1` lorsque :

- le seuil de sélection est atteint avec le minimum de couverture requis ;

ou

- le seuil d'élimination est atteint ;

ou

- le plafond est atteint → `INCONCLUSIVE` si aucun seuil n'est atteint.

## INCONCLUSIVE

Exemples :

- 2 échecs sur 8 sans conséquence forte ;
- résultats très différents selon scénario sans motif clair ;
- action correcte elle-même juridiquement ou institutionnellement ambiguë.

## NO_BUILD associé

`C1` peut produire :

- `AMELIORER_INFORMATION`
- `CORRIGER_SOURCE`
- `CONTRIBUER_EXISTANT`

sans aucun nouveau système.

---

# 7. C2 — FOURRIERE ↔ ASSOCIATION — F6/F7

## Question

La proposition, la réponse et le transfert entre une fourrière et une structure receveuse créent-ils une friction informationnelle ou procédurale ayant une conséquence réelle ?

## Preuve nécessaire

Au minimum :

- cas F6/F7 réels ;
- reconstruction par un acteur opérationnel ;
- idéalement deux côtés d'une même frontière ou artefact opérationnel ;
- distinction explicite entre problème de coordination et absence de place.

## Baseline

Par cas :

- temps animal disponible/cessible → première proposition ;
- `NOMBRE_STRUCTURES_CONTACTEES`
- `NOMBRE_MESSAGES_APPELS`
- `NOMBRE_RELANCES`
- `DELAI_PROPOSITION_REPONSE`
- `DELAI_ACCEPTATION_TRANSFERT`
- existence d'un accusé de réception ;
- existence d'une trace d'acceptation ;
- issue ;
- cause d'un éventuel échec.

## Métrique principale

`TAUX_CAS_F6F7_AVEC_FRICTION_ATTRIBUABLE_COORDINATION`

Un cas est compté si :

1. une friction de communication / information / traçabilité est observée ;

ET

2. elle produit une conséquence ;

ET

3. la cause dominante n'est pas une absence réelle de capacité ou un blocage juridique.

## Métriques secondaires

- délai proposition → réponse ;
- nombre de relances ;
- messages / appels ;
- demandes sans réponse ;
- ressaisies ;
- acceptations sans trace ;
- opportunités de transfert manquées.

## Signal de sélection

`C2` devient sélectionnable si :

- au moins **2 cas indépendants** présentent une friction attribuable à la coordination avec conséquence observable ;

**ET**

- la mécanique est confirmée soit par deux rôles différents, soit par un artefact opérationnel ;

**ET**

- au moins un acteur propriétaire du processus considère la friction comme réellement utile à réduire.

## Signal d'élimination

`C2` est éliminé comme problème principal si, sur au moins 5 cas F6/F7 suffisamment reconstruits :

- aucune friction de coordination avec conséquence n'est observée ;

ou

- les délais / échecs observés sont expliqués principalement par l'absence de place, l'état de l'animal ou une contrainte juridique ;

et

- les deux côtés décrivent un processus actuel suffisamment fiable.

## Cause disqualifiante

- `CAPACITE_PHYSIQUE`
- `JURIDIQUE`
- `EXISTANT_SUFFISANT`
- aucun acteur ne souhaite porter l'amélioration.

## Taille maximale

Maximum **8 cas F6/F7** suffisamment reconstruits dans T0, dans la limite globale Axe C et des entretiens Axe B.

## Stop rule

Arrêt pour `C2` lorsque :

- 2 cas qualifiants + confirmation multi-rôle/artefact + propriétaire du problème sont obtenus ;

ou

- 5 cas suffisamment reconstruits soutiennent l'élimination ;

ou

- 8 cas sont atteints sans décision → `INCONCLUSIVE`.

## INCONCLUSIVE

- trop peu de cas accessibles ;
- causes mixtes impossibles à attribuer ;
- récits contradictoires sans artefact ;
- pratiques très différentes selon EPCI avec couverture insuffisante.

## NO_BUILD associé

Même si `C2` existe, la première intervention doit tester :

`SIMPLIFIER_PROCEDURE`
→ `STANDARDISER_FORMULAIRE`
→ `STANDARDISER_PROTOCOLE_HUMAIN`

avant tout outil.

---

# 8. C3 — ASSOCIATION ↔ FAMILLE D'ACCUEIL

## Question

Existe-t-il une perte d'efficacité entre besoin d'accueil, disponibilité réelle, proposition et acceptation, distincte du simple manque de familles d'accueil ?

## Preuve nécessaire

- cas réels de recherche de FA ;
- méthode réelle utilisée ;
- visibilité de la disponibilité ;
- nombre de contacts ;
- acceptation/refus ;
- distinction entre capacité déclarée et disponibilité réelle ;
- vérification de ce que BNO ou un outil existant couvre déjà.

## Baseline

Par cas :

- date/heure du besoin ;
- délai avant première proposition ;
- nombre de FA sollicitées ;
- canaux ;
- nombre de relances ;
- délai jusqu'à acceptation ;
- disponibilité réelle connue ou inconnue ;
- incompatibilités ;
- cause d'échec.

## Métrique principale

`TAUX_CAS_FA_AVEC_FRICTION_INFORMATIONNELLE_OU_COORDINATION`

## Métriques secondaires

- `DELAI_BESOIN_FA_ACCEPTATION`
- nombre de FA contactées ;
- nombre de canaux ;
- ressaisies ;
- disponibilités obsolètes ;
- places compatibles découvertes tardivement.

## Signal de sélection

`C3` devient sélectionnable si au moins **2 cas indépendants** montrent :

- une FA compatible et réellement disponible non identifiée ou contactée tardivement en raison d'un défaut de visibilité / coordination ;

ou

- une charge répétée de sollicitation / ressaisie avec conséquence observable ;

**ET**

- aucun outil existant déjà utilisé ne résout suffisamment le problème.

## Signal d'élimination

Éliminer `C3` si :

- les cas échouent principalement faute de FA réellement disponibles ou compatibles ;
- les disponibilités sont déjà correctement connues ;
- BNO ou un outil existant configuré couvre suffisamment le besoin ;
- aucune conséquence attribuable à l'information/coordination n'est observée.

## Cause disqualifiante

- `RECRUTEMENT`
- `CAPACITE_PHYSIQUE`
- `EXISTANT_SUFFISANT`
- absence de propriétaire du problème.

## Taille maximale

Maximum **6 cas de recherche / placement FA** reconstruits dans T0.

## Stop rule

- sélection dès 2 cas qualifiants + preuve multi-rôle ou artefact ;
- élimination dès 4 cas suffisamment reconstruits soutenant une cause non informationnelle ;
- plafond 6 → `INCONCLUSIVE` si aucun seuil.

## INCONCLUSIVE

- disponibilité impossible à dater ;
- pas de distinction entre capacité théorique et disponibilité ;
- cas trop hétérogènes.

## NO_BUILD associé

Priorité :

`UTILISER_EXISTANT`
→ `CONFIGURER_EXISTANT`

avant toute nouvelle liaison.

---

# 9. C4 — TRACABILITE / CONTINUITE

## Question

Peut-on reconstruire, pour un animal, qui est responsable maintenant, quel est son statut et quelle action doit suivre ?

## Preuve nécessaire

Dossiers Axe C avec plusieurs étapes, idéalement un transfert inter-structures.

## Baseline

Par dossier :

- nombre d'étapes ;
- étapes avec responsable identifiable ;
- étapes avec statut identifiable ;
- étapes avec prochaine action identifiable ;
- contradictions entre sources ;
- reprise de dossier possible ou non.

## Métrique principale

`TAUX_DOSSIERS_AVEC_RUPTURE_CONTINUITE_CONSEQUENTE`

Un dossier est positif si :

- responsable courant, statut ou prochaine action ne peut être reconstruit à une étape importante ;

**ET**

- cette ambiguïté produit une conséquence observable.

## Métriques secondaires

- taux d'étapes reconstructibles ;
- contradictions ;
- statuts ambigus ;
- appels nécessaires pour reprendre le dossier ;
- ressaisies.

## Signal de sélection

`C4` devient sélectionnable si au moins **2 dossiers indépendants** sur les 5 premiers suffisamment reconstruits présentent une rupture de continuité avec conséquence observable.

## Signal d'élimination

Éliminer `C4` si les 5 premiers dossiers suffisamment reconstruits permettent tous de déterminer :

- responsable courant ;
- statut ;
- prochaine action ;

sans conséquence notable liée à la traçabilité.

## Cause disqualifiante

- données volontairement non partagées pour raison légitime ;
- ambiguïté seulement apparente mais correctement résolue par les registres ;
- absence de conséquence ;
- une simple procédure de clôture / transmission suffit.

## Taille maximale

Maximum **10 dossiers Axe C** au total ; `C4` utilise ce même plafond.

## Stop rule

- sélection à 2 dossiers qualifiants ;
- élimination après 5 dossiers tous reconstructibles sans conséquence ;
- plafond 10 → `INCONCLUSIVE`.

## INCONCLUSIVE

- cas incomplets pour raison de confidentialité ;
- absence de traces accessibles ;
- impossibilité de distinguer une vraie rupture d'une limitation de notre observation.

## NO_BUILD associé

Une rupture de continuité peut être corrigée par :

- standard de transmission ;
- checklist ;
- identifiant commun temporaire ;
- procédure ;

sans dossier logiciel.

---

# 10. C5 — AUTRE PROBLEME

## Objet

Autoriser l'émergence d'un problème réellement inattendu sans transformer cette catégorie en porte ouverte au choix a posteriori.

## Preuve nécessaire

Le problème doit :

1. ne pas être correctement décrit par C1 à C4 ;
2. être apparu spontanément ou par reconstruction, jamais uniquement par suggestion ;
3. être observé dans au moins **3 cas indépendants** ;
4. concerner au moins **2 rôles différents** ou être soutenu par un artefact fort ;
5. produire une conséquence observable ;
6. être distinct d'un simple manque de capacité, financement ou personnel.

## Métrique principale

À ce stade :

`NOMBRE_CAS_INDEPENDANTS_C5`

Aucune nouvelle métrique optimisée après observation ne peut servir rétroactivement à prétendre que C5 était préenregistré.

## Signal de sélection

Tous les six critères ci-dessus doivent être satisfaits.

Avant toute intervention sur C5, un **nouveau préenregistrement spécifique** doit être produit, sans réinterpréter les données historiques.

## Signal d'élimination

- moins de 3 cas au plafond T0 ;
- un seul rôle ;
- problème déjà couvert par C1-C4 ;
- simple opinion ;
- cause disqualifiante dominante.

## Cause disqualifiante

Toutes les causes transversales de section 3.3.

## Taille maximale

Aucune collecte supplémentaire spécifique à C5 pendant T0.

C5 ne peut utiliser que les données produites par le protocole déjà prévu.

## Stop rule

À la fin de T0 :

- critères remplis → `C5_CANDIDAT_NOUVEAU_PREENREGISTRE_REQUIS`
- sinon → `NON_SELECTIONNE`.

## INCONCLUSIVE

C5 n'utilise pas `INCONCLUSIVE` pour justifier une extension exploratoire. Il reste simplement non sélectionné.

---

# 11. C0 — NO_BUILD

## Question

Les données justifient-elles de ne construire aucun nouveau système pour le programme de coordination étudié ?

## Preuve nécessaire

Le terrain doit être suffisamment couvert pour appliquer les critères aux candidats réellement observables.

## Métrique principale

`NOMBRE_CANDIDATS_PASSANT_LES_CRITERES_DE_SELECTION_SANS_CAUSE_DISQUALIFIANTE`

## Signal de sélection de C0

`C0_NO_BUILD` est la décision par défaut si :

1. aucun C1-C4 ne passe son seuil de sélection ;

**OU**

2. tous les candidats passant leur seuil ont une cause disqualifiante dominante ;

**OU**

3. les problèmes observés sont suffisamment résolus par :
   - correction d'information ;
   - simplification de procédure ;
   - standard humain ;
   - outil existant ;
   sans justification d'un nouveau système.

## Cas particulier

`NO_BUILD` ne signifie pas `NO_ACTION`.

La décision peut être :

- corriger une information ;
- documenter une procédure ;
- contribuer à StopErrance ;
- configurer un outil existant ;
- transmettre un protocole aux acteurs ;
- arrêter seulement la branche logicielle.

## Signal d'élimination de C0

C0 est éliminé si au moins un candidat :

- passe tous ses critères de sélection ;
- n'est pas disqualifié ;
- possède un propriétaire du problème ;
- nécessite encore une intervention après test des solutions simples.

Même dans ce cas, le développement logiciel n'est toujours pas autorisé.

## Taille maximale

Identique au plafond global T0.

## Stop rule

C0 ne peut être décidé avant :

- couverture minimale A/B/C requise par le protocole ;

ou

- kill test explicite rendant le cœur du programme inutile / doublonné.

## INCONCLUSIVE

Si la couverture minimale n'est pas atteinte et qu'aucun kill test ne tranche :

`TERRAIN_INSUFFISANT` ou `TERRAIN_BLOCKED`, pas `NO_BUILD`.

---

# 12. Règles de comparaison entre candidats

Si plusieurs candidats passent leur seuil, un seul problème principal peut être retenu.

L'ordre ne dépend pas de l'attrait technique.

Comparer :

1. **attribuabilité** — la conséquence est-elle réellement liée au problème ?
2. **gravité observée** ;
3. **fréquence observée dans T0** ;
4. **mesurabilité d'une amélioration** ;
5. **existence d'un propriétaire du problème** ;
6. **absence de cause disqualifiante** ;
7. **possibilité de tester une intervention sans intégration** ;
8. **solution la plus simple disponible**.

Aucun score composite automatique n'est préenregistré.

La décision doit expliquer séparément chaque dimension.

En cas d'égalité substantielle :

- choisir le problème testable avec le moins de dépendances et de risques ;

ou

- conclure `INCONCLUSIVE`.

Il est interdit de sélectionner plusieurs problèmes pour un premier pilote.

---

# 13. Kill tests prioritaires

Avant d'étendre T0, rechercher à faible coût les éléments pouvant tuer ou réduire fortement un candidat.

## K1 — StopErrance

Question :

> Quelles fonctions couvre réellement StopErrance pour l'orientation et le traitement des signalements ?

Conséquence :

- une fonction couverte devient `EXISTANT_SUFFISANT` si son usage réel est confirmé ;
- seules les fonctions résiduelles restent candidates.

## K2 — Capacité dominante

Question :

> Les issues dégradées observées viennent-elles principalement de l'absence de capacité compatible plutôt que de la circulation de l'information ?

Conséquence :

- disqualification de C2/C3 comme problème informationnel si dominante.

## K3 — Processus F6/F7 déjà efficace

Question :

> Les conventions, appels et pratiques actuelles assurent-ils déjà une proposition/réponse suffisamment fiable ?

Conséquence :

- C2 éliminé si aucun effet significatif n'est observé.

## K4 — Outil existant

Question :

> Un outil déjà utilisé ou configurable couvre-t-il le problème ?

Conséquence :

- `UTILISER_EXISTANT` ou `CONFIGURER_EXISTANT`.

---

# 14. Baseline obligatoire avant tout pilote

Une intervention future ne pourra être déclarée meilleure que l'existant que si une baseline comparable existe.

Pour le problème sélectionné, avant intervention, figer :

- unité de mesure ;
- période / nombre de cas ;
- métrique principale ;
- métriques secondaires ;
- mode de calcul ;
- données manquantes ;
- niveau de preuve.

Un pilote sans baseline comparable donne :

`INCONCLUSIVE`

et ne peut justifier une architecture.

---

# 15. Règle de décision post-T0

Sorties admises :

- `PROBLEME_SELECTIONNE_C1`
- `PROBLEME_SELECTIONNE_C2`
- `PROBLEME_SELECTIONNE_C3`
- `PROBLEME_SELECTIONNE_C4`
- `C5_NOUVEAU_PREENREGISTRE_REQUIS`
- `C0_NO_BUILD`
- `INCONCLUSIVE`
- `TERRAIN_BLOCKED`

Aucune de ces sorties n'autorise directement le code.

Si C1-C4 est sélectionné :

1. appliquer la hiérarchie des solutions simples ;
2. définir une intervention minimale non logicielle ;
3. mesurer cette intervention contre la baseline ;
4. seulement si elle crée de la valeur et que son coût manuel devient limitant, examiner l'outillage.

---

# 16. Interdictions jusqu'à la décision post-T0

- architecture V1 ;
- prototype produit ;
- nouvelle base centrale ;
- inbox territoriale ;
- journal de responsabilité généralisé ;
- API supposée ;
- intégration I-CAD / BNO supposée ;
- moteur d'identification photo ;
- extension générale `VOIR → COMPRENDRE → AGIR` ;
- choix d'un problème par intuition ;
- modification silencieuse des seuils.

---

# 17. Prochaine action après validation de ce préenregistrement

La prochaine action gouvernée redevient :

> **REVUE ADVERSARIALE DES INSTRUMENTS TERRAIN V0.1**

La revue devra désormais vérifier non seulement la neutralité des questions, mais aussi :

> **si les instruments produisent réellement les données nécessaires pour trancher C0 à C5 selon les règles de ce préenregistrement.**

Sorties prévues :

- `PASS_POUR_PRE_TEST_BORNE`
- `CORRECTION_MINIMALE_REQUISE`
- `FAIL_RECONCEPTION_INSTRUMENTS`

Aucun contact terrain n'est autorisé par le présent document.
