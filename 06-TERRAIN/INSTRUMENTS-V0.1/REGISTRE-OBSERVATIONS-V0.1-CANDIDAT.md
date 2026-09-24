# REGISTRE-OBSERVATIONS-V0.1-CANDIDAT

**Statut :** CANDIDAT — structure de registre avant collecte  
**Usage :** registre maître des observations T0

---

# 1. Principe

Une ligne représente une observation atomique.

Ne jamais combiner dans une seule ligne :

- un fait observé ;
- une interprétation ;
- une hypothèse de cause ;
- une idée de solution.

Si ces quatre éléments existent, créer quatre entrées reliées.

---

# 2. Schéma du registre

| Champ | Définition |
|---|---|
| `OBSERVATION_ID` | Identifiant unique |
| `DATE_OBSERVATION` | Date de collecte |
| `AXE` | A / B / C |
| `UNITE` | U1 / U2 / U3 / U4 |
| `SESSION_ENTRETIEN_CASE_ID` | Référence anonymisée |
| `ROLE_ACTEUR` | Rôle, pas identité personnelle |
| `ORGANISATION` | Si pertinent et non sensible |
| `EPCI` | Territoire concerné |
| `ETAPE` | Étape du parcours |
| `FAIT` | Ce qui a réellement été observé ou déclaré |
| `SOURCE_PREUVE` | Artefact, observation, récit, document |
| `FORCE_PREUVE` | P1 à P6 |
| `STATUT_EPISTEMIQUE` | OBSERVED / REPORTED / INFERRED / HYPOTHESIS / UNKNOWN |
| `ORIGINE_SIGNAL` | SPONTANEE / REVELEE_PAR_RECONSTRUCTION / SUGGEREE / NON_APPLICABLE |
| `CANAL` | Téléphone, e-mail, logiciel, formulaire, etc. |
| `DELAI` | Mesuré, estimé ou inconnu |
| `FRICTION_CANDIDATE_ID` | Lien éventuel vers une friction |
| `CONSEQUENCE_OBSERVEE` | Aucune ou conséquence factuelle |
| `CLASSE_PROBLEME_CANDIDATE` | P-INFO, P-ORIENT, etc. |
| `CONFIDENCE` | FORTE / MOYENNE / FAIBLE |
| `DONNEES_PERSONNELLES` | EXCLUES / REDACTEES / AUCUNES |
| `NOTES` | Limites ou contexte |

---

# 3. Force de preuve

- `P1` — trace opérationnelle anonymisée / procédure réellement utilisée ;
- `P2` — démonstration d'un outil sur données fictives ou anonymisées ;
- `P3` — reconstruction concordante des deux côtés d'une frontière ;
- `P4` — récit d'un acteur appuyé par un artefact ;
- `P5` — récit d'un seul acteur sans artefact ;
- `P6` — opinion générale.

La force de preuve ne transforme pas automatiquement une observation en vérité générale.

---

# 4. Modèle de ligne

| OBSERVATION_ID | AXE | UNITE | CASE_ID | ROLE | ETAPE | FAIT | PREUVE | FORCE | STATUT | ORIGINE | DELAI | CONSEQUENCE | CLASSE | CONFIDENCE |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| OBS-0001 | | | | | | | | | | | | | | |

---

# 5. Registre des contradictions

Lorsqu'une observation contredit une autre :

| CONTRADICTION_ID | OBS_A | OBS_B | Nature | Résolution disponible | Statut |
|---|---|---|---|---|---|
| CTR-0001 | | | | | `OUVERTE` |

Ne jamais écraser l'observation précédente.

---

# 6. Registre des inconnues

| UNKNOWN_ID | Question | Axe | Pourquoi important | Source capable de répondre | Statut |
|---|---|---|---|---|---|
| UNK-0001 | | | | | `OUVERTE` |

Une inconnue ne déclenche une nouvelle recherche documentaire que si elle provient directement du terrain et si sa résolution est nécessaire à une décision.

---

# 7. Registre des non-problèmes

| NONPROBLEME_ID | Parcours / étape | Observation | Preuve | Portée |
|---|---|---|---|---|
| NP-0001 | | | | |

Ce registre est obligatoire.

Il empêche de reconstruire des fonctions déjà satisfaisantes.

---

# 8. Contrôle avant ajout

Avant d'ajouter une observation :

- [ ] elle est atomique ;
- [ ] sa source est identifiable ;
- [ ] son statut épistémique est correct ;
- [ ] sa portée n'est pas généralisée ;
- [ ] aucune donnée personnelle inutile n'est présente ;
- [ ] une opinion n'est pas présentée comme mesure ;
- [ ] une friction éventuelle décrit une conséquence observable.

