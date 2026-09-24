# GUIDE-ENTRETIEN-AXE-B-V0.1-CANDIDAT

**Statut :** CANDIDAT — aucun contact autorisé par ce document  
**Référence :** `PROTOCOLE-CARTOGRAPHIE-TERRAIN-V0.1-CANDIDAT`  
**Axe :** B — Parcours inter-structures

---

## 1. Finalité

Reconstituer les pratiques réelles entre structures à partir de cas concrets.

L'entretien ne sert pas à obtenir un avis sur une application future.

Principe :

> PROCESSUS RÉEL → TRACE → DÉLAI → CONSÉQUENCE → INCONNUE

avant toute discussion de solution.

---

## 2. Métadonnées minimales

- `ENTRETIEN_ID` :
- Date :
- Rôle de l'interlocuteur :
- Type d'organisation :
- Territoire / EPCI :
- Ancienneté dans le rôle, si volontairement communiquée :
- Enregistrement audio autorisé : `OUI` / `NON`
- Artefacts montrés : `OUI` / `NON`
- Conservation autorisée d'une copie anonymisée : `OUI` / `NON`

Ne pas enregistrer dans GitHub les coordonnées personnelles de l'interlocuteur.

---

## 3. Introduction standard

Présenter le travail comme une étude de fonctionnement.

À dire :

> Nous cherchons à comprendre comment les parcours fonctionnent réellement entre les différents acteurs. Nous ne partons pas du principe qu'un nouveau logiciel est nécessaire. L'objectif est de reconstruire des cas concrets, de voir ce qui fonctionne bien et d'identifier seulement les frictions vérifiables.

Ne pas présenter l'architecture candidate avant la reconstruction du processus.

---

## 4. Question d'ouverture obligatoire

> Pouvez-vous me raconter le dernier cas réel correspondant à ce parcours, étape par étape, depuis le moment où vous en avez eu connaissance jusqu'à sa clôture ou son état actuel ?

Relances autorisées :

- Que s'est-il passé juste avant ?
- Qui a fait cette action ?
- À qui l'information a-t-elle été envoyée ?
- Par quel canal ?
- Qu'avez-vous reçu en retour ?
- Combien de temps cela a-t-il pris ?
- Quelle trace reste-t-il ?
- Que se passe-t-il quand cela ne fonctionne pas ?

---

# 5. Module F6/F7 — fourrière ↔ refuge / association

Pour un cas réel récent :

1. Quand l'animal devient-il candidat à une sortie ?
2. Qui prend cette décision ?
3. Quelles informations sont disponibles à ce moment ?
4. Comment les structures susceptibles de le recevoir sont-elles identifiées ?
5. Une ou plusieurs structures sont-elles contactées ?
6. Dans quel ordre ?
7. Par quel canal exact ?
8. Quel contenu est transmis ?
9. Existe-t-il un format standard ?
10. Comment savez-vous que la demande a été reçue ?
11. Comment une association accepte-t-elle ?
12. Comment refuse-t-elle ?
13. Existe-t-il un état intermédiaire du type « en attente », « réservé » ou équivalent ?
14. Y a-t-il un délai explicite pour répondre ?
15. Que se passe-t-il sans réponse ?
16. Que se passe-t-il si plusieurs structures répondent positivement ?
17. Qui tranche ?
18. Comment le transfert physique est-il organisé ?
19. Quel document est signé ?
20. À quel moment la responsabilité change-t-elle ?
21. Qui met à jour I-CAD lorsque nécessaire ?
22. Qui clôture le dossier ?
23. Quelle information manque le plus souvent au moment de décider ?
24. Quelles étapes demandent une relance ?
25. Quelle partie fonctionne déjà particulièrement bien ?

### Artefacts utiles, uniquement si l'acteur peut les montrer ou partager

- fiche animale anonymisée ;
- modèle de demande ;
- modèle de réponse ;
- e-mail type ;
- attestation de prise en charge ;
- écran d'un logiciel sur données fictives ou anonymisées ;
- procédure écrite ;
- registre ou extrait anonymisé.

Aucune copie sans autorisation explicite.

---

# 6. Module association ↔ famille d'accueil

Reconstituer un cas réel :

`BESOIN_ACCUEIL → RECHERCHE_FA → PROPOSITION → REPONSE → CONTRAT → TRANSFERT → SUIVI → SORTIE → DISPONIBILITE`

Questions :

1. Où sont enregistrées les familles d'accueil ?
2. Quelles informations viennent de la BNO ?
3. Où est tenue la disponibilité réelle ?
4. Qui la met à jour ?
5. Comment connaît-on les contraintes de compatibilité ?
6. Comment recherche-t-on une FA pour un animal précis ?
7. Combien de personnes sont généralement contactées ?
8. Par quels canaux ?
9. Comment une proposition est-elle formulée ?
10. Comment l'acceptation est-elle tracée ?
11. Un refus est-il conservé ?
12. Comment le contrat est-il généré et conservé ?
13. Comment le suivi se fait-il pendant l'accueil ?
14. Comment sait-on que la FA est de nouveau disponible ?
15. Quelles données sont saisies plusieurs fois ?
16. Quels outils actuels évitent déjà du travail ?

---

# 7. Mesures à reconstruire

Pour le cas étudié :

- `NOMBRE_HANDOFFS`
- `NOMBRE_ACTEURS`
- `NOMBRE_CANAUX`
- `NOMBRE_MESSAGES_APPELS`
- `NOMBRE_RESSAISIES`
- `NOMBRE_SYSTEMES`
- `DELAI_PROPOSITION_REPONSE`
- `DELAI_ACCEPTATION_TRANSFERT`
- `NOMBRE_RELANCES`
- `DEMANDES_SANS_REPONSE`
- `REPONSES_SANS_TRACE`
- `STATUTS_AMBIGUS`
- `DONNEES_MANQUANTES`
- `TEMPS_HUMAIN_ESTIME`

Ne pas transformer une approximation en mesure exacte. Marquer `ESTIMATION_ACTEUR` lorsque nécessaire.

---

# 8. Recherche des conséquences

Pour chaque friction évoquée :

> Quel effet concret cela a-t-il eu sur ce cas précis ?

Catégories :

- `AUCUNE`
- `RETARD`
- `RELANCE`
- `RESSAISIE`
- `ERREUR`
- `INFORMATION_PERDUE`
- `RESPONSABILITE_AMBIGUE`
- `SEJOUR_PROLONGE`
- `SORTIE_MANQUEE`
- `AUTRE`

Demander une preuve ou un exemple lorsque possible.

---

# 9. Question de contrefactuel

Après reconstruction complète seulement :

> Si vous supprimiez une seule difficulté de ce parcours, laquelle réduirait réellement le travail ou le délai ?

Puis :

> Existe-t-il déjà une procédure, un outil ou une simple règle qui pourrait résoudre cela sans nouveau logiciel ?

Cette question sert à tester les solutions simples, pas à vendre une architecture.

---

# 10. Non-problèmes

Demander explicitement :

> Quelles étapes fonctionnent bien aujourd'hui et ne devraient surtout pas être modifiées ?

Les réponses alimentent le registre des non-problèmes.

---

# 11. Clôture

Questions finales :

1. Y a-t-il une étape importante que nous avons oubliée ?
2. Existe-t-il une procédure écrite que nous devrions connaître ?
3. Sur ce cas précis, quelle information serait indispensable pour qu'une autre personne puisse reprendre le dossier sans vous appeler ?

Ne pas demander d'engagement commercial.

---

# 12. Contrôle qualité post-entretien

- [ ] cas réel reconstruit ;
- [ ] processus avant opinions ;
- [ ] canaux identifiés ;
- [ ] délais documentés ou marqués inconnus ;
- [ ] traces identifiées ;
- [ ] conséquences séparées des préférences ;
- [ ] éléments spontanés séparés des éléments suggérés ;
- [ ] ce qui fonctionne bien consigné ;
- [ ] aucune architecture future imposée ;
- [ ] données personnelles exclues ou anonymisées.

**Qualité de preuve :** `FORTE` / `MOYENNE` / `FAIBLE`

**Motif :**
