# MATRICE-QUALIFICATION-FRICTIONS-V0.1-CANDIDAT

**Statut :** CANDIDAT — utilisée uniquement après collecte suffisante  
**Référence :** sections 15 à 18 du protocole terrain V0.1

---

# 1. Règle

Une idée de fonctionnalité n'est jamais une friction.

Une friction doit être formulée comme :

> Dans telle étape, tel acteur rencontre tel obstacle vérifiable, produisant telle conséquence observable.

---

# 2. Fiche de friction

- `FRICTION_ID` :
- Titre descriptif :
- Axe : `A` / `B` / `C`
- Frontière / étape :
- Acteurs touchés :
- Première observation :
- Nombre de cas indépendants :
- Nombre de rôles concordants :
- Origine : `SPONTANEE` / `REVELEE_PAR_RECONSTRUCTION` / `SUGGEREE`

### Formulation factuelle

### Ce qui est observé

### Ce qui est seulement inféré

### Ce qui reste inconnu

---

# 3. Preuves

| OBSERVATION_ID | Cas indépendant | Rôle | Force preuve | Conséquence | Concordance |
|---|---|---|---|---|---|
| | | | | | |

---

# 4. Qualification

## Q1 — Réplication

- [ ] au moins deux cas indépendants ;
- [ ] ou deux rôles différents concordent ;
- [ ] conséquence observable.

Si oui : candidat `FRICTION_QUALIFIEE`.

## Q2 — Gravité forte

- [ ] risque vérifiable pour l'animal ;
- [ ] erreur juridique ;
- [ ] transfert de responsabilité non maîtrisé ;
- [ ] impossibilité d'atteindre le service compétent ;
- [ ] perte définitive d'information critique.

Si un seul cas : `FRICTION_GRAVE_NON_REPLIQUEE`.

## Sinon

`SIGNAL_A_CONFIRMER`.

### Statut final

- `FRICTION_QUALIFIEE`
- `FRICTION_GRAVE_NON_REPLIQUEE`
- `SIGNAL_A_CONFIRMER`
- `NON_PROBLEME`
- `REFUTEE`

---

# 5. Classe de cause dominante

Choisir une cause dominante et, si nécessaire, des causes secondaires.

- `P-INFO` — information absente, obsolète, contradictoire ou inaccessible ;
- `P-ORIENT` — information disponible mais mauvaise orientation ;
- `P-COORD` — circulation lente, répétitive ou non structurée ;
- `P-TRACE` — état, action ou responsabilité difficile à reconstruire ;
- `P-CAP` — absence de capacité compatible ;
- `P-LEGAL` — règle, habilitation ou responsabilité bloquante ;
- `P-INCENT` — moyens, mandat ou incitation insuffisants ;
- `P-NONE` — aucune difficulté significative.

### Cause dominante :

### Causes secondaires :

### Niveau de confiance :

- `FORT`
- `MOYEN`
- `FAIBLE`

---

# 6. Mesure de conséquence

Renseigner seulement ce qui est étayé.

- temps supplémentaire :
- nombre de relances :
- ressaisies :
- systèmes supplémentaires :
- délai ajouté :
- erreur observée :
- responsabilité ambiguë :
- séjour prolongé :
- sortie manquée :
- autre conséquence :

Lorsque la valeur est une estimation, l'indiquer explicitement.

---

# 7. Fréquence

- nombre de cas observés :
- nombre total de cas comparables :
- fréquence calculable : `OUI` / `NON`
- fréquence observée :
- limite de représentativité :

Ne pas extrapoler à La Réunion entière à partir du lot T0.

---

# 8. Solution actuelle

- Comment la friction est-elle gérée aujourd'hui ?
- Existe-t-il un contournement ?
- Ce contournement fonctionne-t-il ?
- Quel coût ou limite produit-il ?
- Existe-t-il déjà un outil couvrant la fonction ?

---

# 9. Test des interventions dans l'ordre obligatoire

Évaluer dans cet ordre.

| Niveau | Intervention | Résout suffisamment ? | Preuve / justification |
|---|---|---|---|
| 1 | `NE_RIEN_FAIRE` | | |
| 2 | `CORRIGER_INFORMATION` | | |
| 3 | `SIMPLIFIER_PROCEDURE` | | |
| 4 | `STANDARDISER_UN_FORMULAIRE` | | |
| 5 | `STANDARDISER_UN_PROTOCOLE_HUMAIN` | | |
| 6 | `UTILISER_UN_OUTIL_EXISTANT` | | |
| 7 | `CONFIGURER_UN_OUTIL_EXISTANT` | | |
| 8 | `AJOUTER_UNE_LIAISON_MINIMALE` | | |
| 9 | `DEVELOPPER_UNE_NOUVELLE_FONCTION` | | |

Dès qu'un niveau simple résout suffisamment la friction, les niveaux plus complexes ne sont pas présumés nécessaires.

---

# 10. Valeur potentielle — sans score prématuré

Décrire séparément :

- réduction potentielle de temps ;
- réduction de ressaisie ;
- réduction de délai ;
- réduction d'ambiguïté ;
- amélioration de traçabilité ;
- impact possible sur l'animal ;
- acteurs bénéficiaires ;
- acteur susceptible de supporter le coût ;
- risques nouveaux introduits.

Aucun « score global » n'est utilisé avant données suffisantes.

---

# 11. Décision

- `NE_RIEN_FAIRE`
- `MESURER_DAVANTAGE`
- `CORRIGER_INFORMATION`
- `TESTER_PROCEDURE_SIMPLE`
- `TESTER_OUTIL_EXISTANT`
- `FORMULER_LIAISON_CANDIDATE`
- `FORMULER_FONCTION_CANDIDATE`
- `ABANDONNER_HYPOTHESE`

### Justification

### Preuves nécessaires avant étape suivante

---

# 12. Contrôle adversarial

Avant de retenir une friction :

1. Existe-t-il une explication plus simple ?
2. Le problème est-il seulement local à un acteur ?
3. Un biais de sélection peut-il l'expliquer ?
4. Avons-nous suggéré le problème ?
5. Une meilleure information suffit-elle ?
6. La capacité physique, le droit ou le financement sont-ils la vraie cause ?
7. Un outil existant couvre-t-il déjà la fonction ?
8. La solution envisagée créerait-elle une double saisie supplémentaire ?
9. Une absence d'intégration est-elle réellement un problème ?
10. Que se passe-t-il si nous ne faisons rien ?

### Verdict adversarial

- `RESISTE`
- `PARTIELLEMENT`
- `NE_RESISTE_PAS`

