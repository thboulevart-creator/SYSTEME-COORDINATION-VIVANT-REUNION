# Protection animale à La Réunion : parcours, systèmes et frontières entre structures — Mission V0.3.1

**Date de consultation des sources :** 24 septembre 2026.
**Statut :** recherche documentaire en lecture seule. Aucun contact, aucun compte créé, aucun formulaire soumis, pas de collecte massive, aucune API présumée.
**Ce document n'est ni une architecture ni une V1 produit.**

**Étiquettes de preuve :**

- **O = OBSERVED** : constaté dans une source primaire ou une interface publique consultée.
- **R = REPORTED** : déclaré par un acteur, un éditeur ou un média.
- **I = INFERRED** : déduit de plusieurs éléments.
- **H = HYPOTHESIS** : proposition à tester.
- **U = UNKNOWN** : pas de preuve suffisante.

**Limites de cette passe :**

- La liste DAAF des associations sans refuge n'a pas pu être lue, car le site bloque l'accès automatisé.
- `app.stoperrance.re` est une coquille JavaScript vide sans compte, donc son contenu est U.
- Légifrance a refusé la lecture directe des articles. Les textes cités proviennent des extraits indexés, et deux versions de l'article L211-25 coexistent dans les résultats (voir A5).
- Aucun logiciel n'a été testé.
- Une page commerciale ne vaut jamais test du logiciel.

---

## 0. Réponse synthétique aux 10 questions de la mission

| # | Question | Réponse courte | Niveau |
|---|---|---|---|
| 1 | Qui intervient ? | Voir le livrable B. Les chaînes de responsabilité légale sont : trouveur/propriétaire → maire/intercommunalité → gestionnaire de fourrière (régie ou prestataire) → refuge ou association (après cession) → famille d'accueil ou adoptant. S'y ajoutent des acteurs d'appui : I-CAD/BNO, DAAF, préfecture, vétérinaires, plateformes perdu/trouvé, co-avionneurs et compagnies aériennes. La faune sauvage suit des filières distinctes (SEOR, Kélonia, GLOBICE/Réseau échouage). | O/I |
| 2 | À quel moment ? | Voir le livrable D. Les bascules juridiques sont : capture, fin du délai franc (4 ou 8 jours ouvrés), cession, contrat famille d'accueil, certificat d'engagement suivi d'un délai de 7 jours, adoption. | O |
| 3 | Avec quelle autorité ? | Le maire (police de la divagation). Le gestionnaire de fourrière, propriétaire de l'animal à la fin du délai. Le vétérinaire (avis avant cession, euthanasie). L'association (choix de la famille d'accueil, adoption). La DAAF (réception des déclarations). | O |
| 4 | Avec quelle information ? | Identification (numéro de puce), description, lieu, état, coordonnées. Le reste (état de santé, comportement, compatibilité) relève du jugement humain et n'est centralisé nulle part. | O/I |
| 5 | Dans quel logiciel ou canal ? | Identification et opérateurs : I-CAD, Filalapat, BNO. Mesure : StopErrance. Annonces publiques : Pet Alert et autres sites. Entre structures : téléphone, courriel, formulaires web associatifs, Facebook. Pawer, Pattoune et Hunimalis sont proposés mais leur usage local est U. | O/R/U |
| 6 | Quelle source de vérité ? | Voir le livrable E. I-CAD pour l'identification et le détenteur ; BNO pour l'opérateur déclaré et la capacité maximale de la famille d'accueil ; registres des structures pour la présence physique. **Aucune source de vérité n'existe pour la disponibilité ni pour l'acceptation entre structures.** | O/I |
| 7 | Qui confirme l'étape suivante ? | Le receveur : association, famille d'accueil, adoptant. Le canal de confirmation fourrière → association n'est **pas documenté publiquement**. | U |
| 8 | Où l'information est-elle ressaisie, retardée ou perdue ? | Voir les livrables G et H. Annonces perdu/trouvé sur au moins 5 supports non synchronisés ; aucune liste publique des animaux en fourrière (critique avec 4 jours) ; au moins 3 saisies par cession ; capacité de la famille d'accueil tenue à la fois dans la BNO et chez l'association. | O/I |
| 9 | Quelles fonctions sont bien couvertes ? | Identification et alerte au propriétaire d'un animal identifié (I-CAD/Filalapat). Déclaration et collaboration association ↔ famille d'accueil (BNO). Orientation générale (StopErrance, sites des intercommunalités). Faune sauvage (SEOR, GLOBICE, Kélonia). | O |
| 10 | Quelles frontières pourraient justifier une liaison ? | Candidates seulement : F7/F8 (fourrière → association : proposition, acceptation) et F11 (association → famille d'accueil : proposition, disponibilité). **Aucune n'est démontrée.** Le goulot documenté reste d'abord capacitaire et organisationnel. | H |

---

## LIVRABLE A — Errata V0.2

| # | Affirmation V0.2 | Correction | Niveau | Source |
|---|---|---|---|---|
| A1 | Opérateur de StopErrance « UNKNOWN » | L'éditeur est **la préfecture de La Réunion** ; le directeur de la publication est le préfet. La conception, le développement et la maintenance sont assurés par l'**agence 10positif** (Saint-Denis). L'hébergement est assuré par **Webflow, Inc.** | O | stoperrance.re/mentionslegales |
| A2 | « StopErrance n'est ni un outil de signalement ni un outil de suivi de cas » | **Conclusion insuffisamment établie, retirée.** Les CGU (version du 2 février 2026) disent que le service « permet aux utilisateurs d'effectuer des signalements », consultables et traitables par des « services compétents habilités », sans garantie de prise en charge. Certaines fonctions nécessitent un compte, qui doit correspondre à une « personne physique réelle ». La vitrine publique, elle, ne propose que le questionnaire des acteurs et renvoie les citoyens vers la mairie, la fourrière ou Pet Alert. **Il y a donc une contradiction entre la vitrine et les CGU.** Le contenu réel de l'application (types de signalements, destinataires, statuts, clôture) est U. La présentation d'info.fr (« ouvert au grand public ») n'est plus réfutée : son statut devient U. | O (CGU) / U (app) | stoperrance.re/cgu |
| A3 | Objet de StopErrance limité à la « mesure » | Il faut ajouter : les données collectées doivent alimenter « l'étude scientifique qui sera réalisée ». Le formulaire de participation restreint le choix de structure à 10 catégories (associations, communes/police municipale, fret aérien, DAAF, EPCI/fourrières, gendarmerie/police, ONF, Parc national, rectorat, vétérinaires). Une politique de confidentialité est mentionnée par les CGU, mais aucun lien n'a été trouvé. | O | stoperrance.re/participer ; /cgu |
| A4 | Délai de garde du TCO : « 8 jours » | **Faux.** Le TCO publie 8 jours ouvrables pour un animal identifié et 4 jours seulement pour un animal non identifié. C'est cohérent avec l'article R271-9 : en outre-mer, pour les chiens et chats non identifiés capturés parce que dangereux ou susceptibles de provoquer des accidents, le délai de l'article L211-26 « peut être réduit à quatre jours ouvrés ». La contradiction restante concerne la CIVIS, qui affiche 4 jours sans distinguer identifié et non identifié. L'affirmation de Free Dom selon laquelle un « arrêté préfectoral impose » 4/8 jours reste R, aucun arrêté n'ayant été trouvé. | O | tco.re (fourrière) ; Légifrance R271-9 ; freedom.fr |
| A5 | L211-25 : cession « à une association », rédaction post-2021 U | La version consolidée affichée par Légifrance (section L211-11 à L211-28) et par Lexbase prévoit la cession gratuite, après avis vétérinaire, à des fondations ou associations disposant d'un refuge **« ou à des associations mentionnées à l'article L. 214-6-5 »**, c'est-à-dire les associations sans refuge. L'extrait est tronqué. D'anciennes versions encore indexées (« refuge… seules habilitées ») circulent. **Des acteurs locaux tiennent des propos conformes à l'ancienne version** (TCO : le refuge est « seul habilité à faire adopter » ; un acteur associatif cité par Zinfos en 2023 : « elle peut céder les chiens qu'à une association qui dispose d'un refuge »). Voir la rupture R7. | O (extraits) / I | Légifrance LEGISCTA000006167705 ; lexbase ; tco.re ; zinfos974 (19/02/2023) |
| A6 | CASUD : « fourrière et refuge », gestionnaire du refuge U | Selon Zinfos (19/02/2023), le refuge de Bérive est vide depuis le départ de l'association Les Petits Innocents en mai 2022, l'appel à candidatures de 2022 n'a trouvé aucun preneur, et la SEMRRE est prestataire de la fourrière. Or StopErrance compte en 2026 « 3 refuges (CASUD, CINOR et CIVIS) ». **Contradiction datée : l'état actuel du refuge de la CASUD est U.** | R / O | zinfos974 ; stoperrance.re |
| A7 | Inférence « 40 à 60 rotations par place et par an » | **Erreur de calcul, retirée.** 9 000 captures pour 395 places donnent environ 23 entrées par place et par an. Aucune conclusion sur l'occupation n'est tirable sans durée de séjour, euthanasies immédiates ni chiffres par site. | I (corrigée) | — |
| A8 | Pawer : « abonnement, prix U » | Pawer affiche un accès gratuit « sans limite de durée », un essai Pro de 30 jours et un **« réseau » ouvert aux familles d'accueil**, qui peuvent « mettre leur foyer à disposition des associations ». Ce pool de familles d'accueil entre associations est R. Le 24/09/2026, l'annuaire public des associations partenaires n'en affichait **qu'une** (Bourges), ce qui laisse supposer une adoption faible et aucune présence réunionnaise visible. | R / O | pawer.fr/fr ; pawer.fr/fr/associations |
| A9 | Hunimalis : « version gratuite » | Hunimalis propose une version gratuite côté associations, puis une offre « à partir de 20 € par mois ». Un module « fourrières » annonce une « coordination des transferts et adoptions » avec les refuges partenaires et des registres d'entrée et de sortie. C'est R, non testé. | R | hunimalis.com |
| A10 | BNO : fonctionnement largement U | Le guide I-CAD a été lu, voir la section 6. L'inscription d'un opérateur est transmise à la DDPP (DAAF à La Réunion) pour vérification, puis un récépissé est délivré. | O | Guide BNO associations sans refuge (I-CAD) |
| A11 | Remise directe d'un animal par un particulier à une association « exclue (I) » | L'inférence est maintenue, mais **elle est contredite dans la pratique** : plusieurs associations déclarent récupérer des animaux « dans la rue » (Sauvade, RPA). La qualification juridique de ces « sauvetages » est U. Voir la rupture R6. | I / R | asso-sauvade.fr ; rpa974 |
| A12 | Absence d'autres logiciels | **Refugilys** se déclare utilisé « en France et dans les DOM » (R). Son usage à La Réunion est U. | R | refugilys.org |

---

## LIVRABLE B — Carte des acteurs

### B1. Autorité et décisions

| Acteur | Fonction | Peut décider | Ne peut pas décider | Déclencheur | Fin / successeur |
|---|---|---|---|---|---|
| Particulier trouveur | Signaler, éventuellement retenir temporairement l'animal | Qui il appelle ; déclaration « trouvé » sur Filalapat | Statut juridique de l'animal, adoption, cession | Découverte | Remise à la fourrière ou au propriétaire |
| Propriétaire | Rechercher l'animal, prouver sa détention, payer les frais | Déclarations de perte (I-CAD) ; annonces | Délai de fourrière | Perte | Restitution ; sinon perte de propriété à la fin du délai (L211-25) |
| Maire / commune | Police de la divagation (L211-22) ; peut prendre des arrêtés (R271-10) | Capture, arrêtés, amende de 150 € sur arrêté (R) | Gestion de la fourrière quand elle est transférée à l'intercommunalité | Signalement de divagation, attaque de cheptel | Intercommunalité / fourrière |
| Police municipale | Reçoit les constats de divagation et d'attaques (O StopErrance) | Constat | Capture si non organisée (U) | Signalement | Mairie / fourrière (U) |
| Intercommunalité (CINOR, CIREST, CIVIS, CASUD, TCO) | Exerce la compétence fourrière (L211-24) ; stérilisations aidées | Mode de gestion (régie ou marché), conventions avec des associations, priorisation des captures | Adoption directe (O CIREST) | Numéro vert, courriel | Gestionnaire de fourrière |
| Gestionnaire de fourrière (régie ou prestataire, ex. SEMRRE cité pour la CASUD en 2023) | Capture, garde, recherche du propriétaire, restitution | Restitution après frais ; garde dans la limite de la capacité ; cession après avis vétérinaire ; euthanasie sur avis vétérinaire | Adoption directe par un particulier | Capture | Propriétaire, refuge ou association (cession), ou euthanasie |
| Refuge (SPA Réunion, SPA du Sud ; CASUD U) | Accueil et adoption | Accepter ou refuser un animal ; sélection selon le « potentiel d'adoption » (R, Zinfos 2023) ; adoption | Obliger une fourrière à céder | Proposition de la fourrière, abandon par un propriétaire | Adoptant, famille d'accueil, transfert |
| Association sans refuge | Placement en famille d'accueil, adoption | Choix de la famille d'accueil (représentant compétent), adoption | Recevoir des animaux hors des provenances de L214-6-5 (I) | Cession, don d'un propriétaire, réquisition administrative ou judiciaire | Famille d'accueil, adoptant, association en métropole |
| Famille d'accueil | Héberger sans transfert de propriété (L214-6 V) | Accepter ou refuser un animal ; demander la fin de collaboration (BNO) | Céder ou faire adopter | Proposition de l'association | Retour à l'association, adoption |
| Vétérinaire | Lecture de puce, identification ; vétérinaire sanitaire en fourrière ; avis avant cession ; certificat pour la famille d'accueil ; stérilisations | Diagnostic, euthanasie médicale, avis de cession | Propriété de l'animal | Présentation de l'animal | Retour vers le détenteur |
| I-CAD | Fichier national d'identification | Aucune décision sur l'animal | — | Identification, déclarations | — |
| BNO (gérée par I-CAD) | Registre des opérateurs, établissements et familles d'accueil | Enregistrement ; transmission à la DDPP | Validation (faite par la DDPP/DAAF) | Inscription | Récépissé |
| Préfecture, sous-préfet de Saint-Pierre (mission errance) | Pilotage, cages de capture, lecteurs de puce, StopErrance, facilitation des transferts vers l'Hexagone | Orientations, financements | La compétence fourrière (communale ou intercommunale) | — | — |
| DAAF | Reçoit les déclarations des associations sans refuge ; publie la liste ; contrôles | Validation des déclarations BNO (rôle de DDPP, I) | — | Déclaration | Liste publiée |
| StopErrance | Base départementale, questionnaire, signalements (selon les CGU) | U | — | U | U |
| Plateformes perdu/trouvé (Pet Alert, chien-perdu.org, SOS chien perdu, 30 Millions d'Amis…) | Diffusion d'annonces | Modération de leurs annonces | Aucune décision juridique | Annonce | U |
| Gendarmerie / police nationale | Contrôle de l'identification (lecteurs fournis par l'État), plaintes d'éleveurs, mains courantes | Procès-verbaux | — | Plainte, contrôle | Justice |
| Compagnies aériennes, co-avionneurs, associations receveuses en métropole | Transferts d'animaux vers l'Hexagone | Accepter un animal en soute | — | Adoption ou famille d'accueil en métropole | Association receveuse, adoptant |
| SEOR / Kélonia / GLOBICE (Réseau échouage) | Faune sauvage protégée | Prise en charge, soins, relâcher ; manipulation réservée aux porteurs de la carte verte (cétacés) | — | Signalement | Relâcher, données nationales |
| Éleveurs | Victimes d'attaques | Plainte, signalement | — | Attaque | Mairie, forces de l'ordre |
| ONF, Parc national, rectorat | Listés comme acteurs mobilisés par StopErrance | U | U | U | U |

### B2. Informations, outils et traces

| Acteur | Reçoit | Produit | Outils / canaux | Source de vérité pour lui | Traces conservées |
|---|---|---|---|---|---|
| Trouveur | Consignes (StopErrance, sites des intercommunalités) | Signalement, photo, lieu | Téléphone, Filalapat, Pet Alert, Facebook | — | Annonces (U) |
| Propriétaire | Alerte I-CAD/Filalapat, appels | Déclaration de perte, annonces | I-CAD, Filalapat, Pet Alert, affiches, radio, main courante (R APPAR) | Carte I-CAD | Déclaration I-CAD |
| Fourrière | Signalement, animal, numéro de puce | Entrée/sortie, restitution, cession, euthanasie | I-CAD ; logiciel interne **U** | Registre interne (U) | Registre (U) ; entrée en fourrière connue d'I-CAD (voir F4) |
| Refuge / association | Animal cédé ou abandonné | Cession, contrat de famille d'accueil, certificat d'engagement, adoption | Formulaires web, téléphone, Facebook, BNO ; Pawer/Pattoune/Hunimalis/Refugilys **U** | Registres légaux | Registre des familles d'accueil, registre des entrées et sorties (R pour les refuges) |
| Famille d'accueil | Contrat, document d'information, certificat vétérinaire (7 jours) | Nouvelles, disponibilité | BNO, téléphone, logiciel éventuel de l'association | Contrat | Contrat |
| I-CAD | Identifications, changements de détenteur, pertes, « trouvé » | Alertes au détenteur | Fichier + Filalapat | Lui-même | Fichier national |
| BNO | Opérateurs, établissements, familles d'accueil, capacités maximales | Récépissé, notifications | Plateforme BNO | Elle-même (déclaratif) | Historique des collaborations (début, fin) |
| StopErrance | Questionnaires ; signalements (CGU) | Chiffres agrégés publics | Webflow + application | U | U |
| SEOR | Appel téléphonique | Prise en charge, relâcher | Téléphone, postes-relais, bénévoles | Centre de soins | U (registre de centre de soins probable, I) |

---

## LIVRABLE C — Carte des systèmes

| Système | Identité (opérateur / utilisateurs / finalité) | Entrées | Workflow / états | Sorties | Interopérabilité documentée | Permissions | Niveau |
|---|---|---|---|---|---|---|---|
| **Fichier I-CAD** | Gestionnaire du fichier national (délégation du ministère) ; identification des chiens, chats et furets | Numéro, détenteur, coordonnées, changements de détenteur, perte | Identifié → perdu → retrouvé ; changement de détenteur (cession) | Alertes au détenteur ; consultation par les professionnels (R) | Aucune API tierce documentée ; fiches de procédure « acquérir », « céder », « mettre à jour les coordonnées » republiées par StopErrance | Détenteur (numéro + mot de passe) ; professionnels habilités | O/R |
| **Filalapat** (I-CAD) | Grand public | Annonce perdu/vu/trouvé, photo, lieu | Déclaration « trouvé » → alerte au détenteur. Notification au propriétaire **« lorsque votre animal entre en fourrière »**. Le propriétaire confirme « retrouvé » : l'annonce est supprimée et les coordonnées du trouveur ne sont plus accessibles. | Notifications, annonces, carte « Autour de moi » (vétérinaires, fourrières, animaux trouvés) | Aucune API documentée | Application publique ; espace détenteur | O (FAQ) |
| **BNO** (I-CAD) | Opérateurs : éleveurs, refuges, fourrières, pensions, animaleries, associations sans refuge et leurs familles d'accueil | SIRET ou RNA, responsable légal, contact opérationnel, établissements, espèces, personnel qualifié, vétérinaire sanitaire (Cerfa 15983), familles d'accueil (identité, adresse, téléphone, courriel, date de naissance, date de collaboration, **capacité par espèce**) | Inscription → validation DDPP → récépissé. Collaboration famille d'accueil : en attente → acceptée / refusée → active → fin (avec date). Détection des doublons. | Notifications par courriel à tous les établissements liés en cas de modification ; courriel servant à vérifier les annonces de cession en ligne | Aucune API ni export documentés | Seul le contact opérationnel se connecte ; la famille d'accueil a son propre compte | O (guide) |
| **StopErrance – vitrine** | Préfecture ; public et acteurs | Formulaire de demande de participation | — | Chiffres clés, contacts, guides PDF | Aucune | Public | O |
| **StopErrance – application** (app.stoperrance.re) | Préfecture / 10positif | Questionnaire des acteurs ; **signalements** (CGU) | U | U | U | Compte obligatoire pour certaines fonctions | U |
| **Pet Alert** (plusieurs sites : petalert.fr, pet-alert-974.fr, petalertglobal.com ; page Facebook Pet Alert Réunion 974, environ 40 800 mentions « j'aime ») | Réseau de bénévoles | Formulaire d'alerte « Découverte » ou « Disparition » | Validation par l'équipe → diffusion sur les réseaux sociaux, aux bénévoles (« watchers ») et aux vétérinaires partenaires du périmètre (R Pet Alert France) | Affiches, publications | Aucune avec I-CAD ni les fourrières | Public | R/O. Plusieurs opérateurs possibles derrière la marque (I) |
| **Autres annonces** (chien-perdu.org : 97 annonces « Réunion » affichées ; SOS chien perdu ; 30 Millions d'Amis ; CPasPerdu) | Divers | Annonces | Clôture U | Annonces | Aucune | Public | O |
| **Pawer** | Éditeur privé ; associations et familles d'accueil | Fiches animaux, familles d'accueil, disponibilités, préférences | Statuts d'animal, attribution à une famille d'accueil, rendez-vous ; catalogue public et candidatures | Catalogue d'adoption | Aucune API ni export documentés | Association, famille d'accueil, équipe | R ; usage réunionnais non observé |
| **Pattoune** | Éditeur privé | Dossiers, suivi vétérinaire, familles d'accueil | **Annuaire des familles d'accueil « disponibles et recherchant une association »** | Site d'adoption | U | Démonstration sur rendez-vous | R |
| **Hunimalis** | Éditeur privé (depuis 2016, « plus de 2 000 professionnels » R) | Fiches animaux, registres | Registres d'entrée et de sortie (Cerfa, R214-30-3/4 cités) ; module fourrière avec « coordination des transferts » ; placements en famille d'accueil | Rapports « exportables » (R) | Export mentionné, pas d'API documentée | Compte | R |
| **Refugilys** | Éditeur (30 ans annoncés) | U | U | U | U | U | R (« France et DOM ») |
| **Logiciels des 5 fourrières** | — | — | — | — | — | — | **U** |
| **Trombinoscope CIREST** | Intercommunalité | Liste d'animaux adoptables | — | Liste | — | Public | O : affichait « Impossible de charger la liste des animaux » |
| **Canaux informels** | Associations, particuliers | — | — | — | — | — | Voir ci-dessous |

**Canaux informels et flux parallèles documentés (sans deviner les autres) :**

- **Téléphone :**
  - numéros verts des intercommunalités, avec messagerie et astreinte le week-end au TCO (O) ;
  - SEOR, Kélonia et GLOBICE (O).
- **Formulaires web et téléphone :**
  - recrutement des familles d'accueil par formulaire en ligne via la page TCO, qui renvoie vers l'APEBA et sa page Facebook (O) ;
  - formulaire de RPA étudié par un « Pôle Famille d'Accueil », puis rappel téléphonique (O).
- **Facebook et groupes :**
  - page Pet Alert 974 ;
  - groupe « Co avionnage Réunion métropole » et pages d'associations (O, liste Zinfos 2018).
- **Radio et presse :**
  - annonces de perte sur radio Freedom et dans les journaux (R) ;
  - affiches et main courante (R, APPAR).
- **Non trouvés publiquement :** WhatsApp, SMS, tableurs, Google Sheets et listes de diffusion (**U, non inventés**). Pawer décrit précisément les « tableurs et e-mails qui s'accumulent » comme la situation qu'il remplace, mais c'est un discours commercial, pas une observation locale (R).

---

## LIVRABLE D — Parcours P1 à P7

Colonnes : événement → acteur | information / décision | système / trace | responsabilité → suivant (condition) | rupture potentielle | preuve.

### P1 — Chien trouvé par un particulier

| # | Événement → acteur | Information / décision | Système / trace | Responsabilité → suivant | Rupture | Preuve |
|---|---|---|---|---|---|---|
| 1 | Découverte → trouveur | Détresse ? Dangerosité ? Puce ? | Consignes StopErrance (fiche réflexe) | Aucune responsabilité légale formalisée | Statut du trouveur qui garde l'animal : U | O / U |
| 2a | Trouveur → vétérinaire (lecture de puce) → I-CAD | Numéro de puce | I-CAD | — | Coordonnées du détenteur périmées | O (StopErrance renvoie aux vétérinaires) / R |
| 2b | Trouveur → Filalapat « trouvé » | Photo, lieu, puce | Alerte automatique au détenteur | Détenteur → restitution directe, hors fourrière | Animal non identifié : aucune correspondance possible | O (FAQ) |
| 2c | Trouveur → Pet Alert / Facebook | Photo, lieu | Diffusion ; vétérinaires partenaires avertis (R) | — | Aucun lien avec I-CAD ni la fourrière | O / R |
| 3 | Trouveur → numéro vert de l'intercommunalité | Lieu, description | Téléphone ; trace U | Intercommunalité → capture (priorisée selon la capacité, TCO) | Capture différée ou non réalisée faute de places (TCO) | O |
| 4 | Capture → fourrière | Examen par le vétérinaire sanitaire (R271-9) ; lecture de puce | Registre (U) ; entrée en fourrière visible par le propriétaire via Filalapat (O) — le mécanisme de saisie de la fourrière est U | Gestionnaire de fourrière | Euthanasie immédiate possible si dangereux, gravement atteint ou en misère | O |
| 5 | Garde | Délai de 8 jours ouvrés (identifié) ou 4 (non identifié, R271-9 ; TCO) | — | — | Délai de 4 jours très court pour un propriétaire d'animal non identifié | O |
| 6a | Propriétaire → fourrière | Preuve de détention, paiement (TCO : 30 € de capture, 20 € par jour au-delà de 24 h après information) | Restitution | Propriétaire | — | O |
| 6b | Fin du délai | Voir P4 | — | Propriété transférée au gestionnaire (L211-25) | — | O |
| Alternative | Trouveur → association directement | « Sauvetage » | U | U | **Cadre légal ambigu (R6)** | R / I |

### P2 — Chat trouvé (différences avec P1)

- Divagation définie différemment pour le chat : non identifié à plus de 200 m des habitations, ou à plus de 1 000 m du domicile de son maître (O, V0.2).
- Capacités minimes : 99 places sur l'île, dont 14 au TCO (O).
- Filière « chats libres » : capture, stérilisation, identification et relâcher (L211-27). Son usage réel à La Réunion est U.
- Filalapat couvre les chats (O).
- **Particularité opérationnelle (I) :** vu la faiblesse des capacités, un chat trouvé a moins de chances d'entrer en fourrière. La branche « trouveur → association / famille d'accueil » pèse donc probablement davantage, et c'est précisément la branche la moins encadrée juridiquement (R6). C'est une hypothèse à vérifier.

### P3 — Animal perdu par son propriétaire

| # | Action du propriétaire | Système | Ce qui redescend ailleurs | Preuve |
|---|---|---|---|---|
| 1 | Déclarer la perte dans l'espace détenteur I-CAD | I-CAD | « Informe les vétérinaires, fourrières, associations… » (service-public). Le mécanisme de diffusion est U | O / R |
| 2 | Annonce Filalapat, alertes par critères | Filalapat (I-CAD) | Notification si l'animal est trouvé par un utilisateur ou s'il entre en fourrière | O |
| 3 | Alerte « Disparition » Pet Alert | Pet Alert | Diffusion sur les réseaux sociaux et aux bénévoles ; aucune remontée vers I-CAD | R |
| 4 | Autres sites, Facebook, affiches, radio, journaux | Multiples | Aucune | O / R |
| 5 | Appels à la fourrière, dépôt de photo, rappels réguliers ; main courante ; appels à « toutes les associations » et vétérinaires | Téléphone | Aucune | R (APPAR) |
| 6 | Restitution | Fourrière ou trouveur | Filalapat : « retrouvé » supprime l'annonce. Les autres supports : clôture manuelle ou absente (I) | O / I |

**Double saisie minimale (I) :** pour un animal non identifié, les informations sont saisies sur au moins 4 supports, sans réconciliation possible.

### P4 — Animal en fin de délai de fourrière

| # | Étape | Acteur / décision | Trace | Preuve |
|---|---|---|---|---|
| 1 | Fin du délai | Le gestionnaire de fourrière devient propriétaire | Registre (U) | O |
| 2 | Qualification | Avis vétérinaire obligatoire avant cession ; sélection selon le « potentiel d'adoption » par les bénévoles du refuge (R) | U | O / R |
| 3 | Proposition fourrière → structure | **Canal : U.** Indices : CIREST (7 associations conventionnées), CIVIS (la SPA du Sud a pour « rôle premier » de sortir des animaux de la fourrière du même centre, R HelloAsso), CINOR (refuge SPA adjacent, avec quota), TCO (sans refuge, renvoie à une liste d'associations constituée par l'association ZOOM, O) | U | O / R / U |
| 4 | Acceptation / refus | Structure receveuse | U | U |
| 5 | Cession | Gratuite, après avis vétérinaire, à un refuge ou à une association L214-6-5 | Document de cession + changement de détenteur I-CAD (procédure I-CAD, O) | O / I |
| 6 | Pas de preneur | Garde dans la limite de la capacité, ou euthanasie. CASUD 2023 sans refuge : « euthanasie quatre jours après capture » (R) | U | O / R |
| 7 | Après cession | Refuge, famille d'accueil (P5), ou transfert vers l'Hexagone (P6) | Registre de la structure | O |

### P5 — Association → famille d'accueil

Voir le livrable I pour le détail. Chaîne :

- recrutement ;
- contrôle (U) ;
- enregistrement BNO et collaboration acceptée ;
- disponibilité (**hors BNO**) ;
- sélection (représentant de l'association) ;
- proposition (téléphone ou Facebook, R/O) ;
- acceptation (U) ;
- contrat, document d'information et certificat vétérinaire sous 7 jours ;
- transfert ;
- suivi (U) ;
- adoption ou retour ;
- fin de collaboration BNO datée.

### P6 — Transferts entre structures

| Transfert | Décision | Documentation | Classe | Preuve |
|---|---|---|---|---|
| Fourrière → refuge / association | Voir P4 | Cession + I-CAD | Non documentée (canal) | U |
| Association → association (île) | U | U | Non documentée | U |
| Association réunionnaise → famille d'accueil ou adoptant en métropole, par co-avionnage | Association ; voyageur volontaire. Sauvade : environ 70 vols par an, une dizaine de familles d'accueil à La Réunion, une quinzaine en métropole, adoption en Île-de-France (R). RPA : familles d'accueil sur place puis en région parisienne (O) | Enregistrement auprès de la compagnie aérienne, organisé par l'association (R). Changement de détenteur I-CAD à l'adoption (I) | Informelle et structurée par association | O / R |
| Vulnérabilité | Chaîne suspendue quand les vols se raréfient (confinement 2020 : chiens « bloqués sur l'île ») | — | Capacitaire / logistique | R |
| Rôle de l'État | « Facilitation des transferts vers l'hexagone » ; compagnies aériennes membres du réseau StopErrance | U | — | O |

### P7 — Faune sauvage

| Branche | Premier contact | Procédure | Responsable final | Preuve |
|---|---|---|---|---|
| Oiseaux (pétrels, puffins, papangues, pailles-en-queue) et chauves-souris | SEOR, 0262 20 46 65 | Accord téléphonique → dépôt dans l'un des postes-relais (environ une centaine selon la LPO : SDIS, cliniques vétérinaires, police, gendarmerie) → collecte par des bénévoles et premier diagnostic → centre de Saint-André → relâcher | SEOR | O / R |
| Tortues marines | Kélonia, 0692 65 37 98 (urgence) | Centre de soins | Kélonia | R (CEDTM) |
| Cétacés | GLOBICE, 0692 65 14 71, 7 j/7 : « numéro unique » du Réseau échouage | Seuls les membres porteurs de la carte verte manipulent l'animal ; partenaires : Muséum, DEAL, BNOI, OFB, Réserve naturelle marine, Kélonia, vétérinaires | Réseau échouage ; données vers le Réseau national échouages / Pelagis (I) | O |

---

## LIVRABLE E — Matrice information × source de vérité

| Information | Source de vérité légitime | Nature | Remarques / corrections |
|---|---|---|---|
| Identification (numéro) | Fichier I-CAD | Réglementaire | O |
| Détenteur enregistré | I-CAD | **Présomption, pas une preuve de propriété** | Dépend des mises à jour du détenteur (I) |
| Coordonnées du détenteur | I-CAD, déclaratif | Peut être périmé | O (I-CAD insiste sur l'actualisation) |
| Animal perdu (déclaré) | Déclaration du propriétaire dans I-CAD / Filalapat | Déclaratif | Les annonces Pet Alert ou Facebook ne font pas autorité |
| Animal trouvé | Déclarant | **Pas une preuve** (espèce, identité, statut) | — |
| Entrée en fourrière | Registre de la fourrière | Réglementaire (U sur le support) | Se reflète dans l'alerte Filalapat (O) |
| Statut « abandonné » / propriété | Gestionnaire de fourrière, à l'expiration du délai | Légal (L211-25) | Aucun registre public |
| Restitution / cession | Gestionnaire de fourrière (émetteur) et receveur, puis I-CAD (changement de détenteur) | Légal + fichier | Au moins 3 écritures (I) |
| Opérateur déclaré | BNO, après validation DDPP/DAAF (récépissé) | Réglementaire | — |
| Association sans refuge déclarée | Liste DAAF **et** BNO | Deux registres | Divergence possible entre les deux (I), non vérifiable ici |
| Capacité réglementaire d'un refuge ou d'une fourrière | Arrêté / déclaration (ex. CIVIS : arrêté 2010-1418) | Réglementaire | O |
| Capacité maximale d'une famille d'accueil | BNO, déclaratif | Non vérifiée | O |
| Présence physique | Registre d'entrées et de sorties de la structure | Réglementaire (R pour les refuges) | Non public |
| Disponibilité | Famille d'accueil (volonté) + association (décision) | **Aucun registre qui fasse autorité** | Pawer ou Pattoune possibles, mais internes ou commerciaux (R) |
| Compatibilité avec un animal | Jugement humain de l'association | Non centralisable raisonnablement (I) | — |
| Acceptation d'une demande | Destinataire | **Aucun support documenté** | Rupture R1 |
| Transfert effectif | Émetteur + receveur (document) + I-CAD | Mixte | — |
| Adoptabilité | Refuge ou association devenus propriétaires | Légal | — |
| Signalement de divagation ou d'attaque | Mairie / police municipale ; plainte : forces de l'ordre | Administratif | — |
| Données agrégées sur l'errance | StopErrance (préfecture) | **Dérivé, pas une source primaire** | Dépend des questionnaires |
| Échouage d'un cétacé | Réseau échouage (GLOBICE) → base nationale | Scientifique / réglementaire | I |
| Oiseau pris en charge | SEOR | Interne | U |

**Principe (I) :** si une couche de liaison devait exister un jour, elle ne pourrait être source de vérité que pour ce qu'elle crée elle-même, c'est-à-dire des demandes et des réponses horodatées. Elle ne le serait ni pour l'identité, ni pour la propriété, ni pour la capacité, ni pour la présence physique.

---

## LIVRABLE F — Matrice des frontières

**Classes :**

- **AUTO** : automatisée ;
- **HS** : humaine mais structurée ;
- **INF** : informelle ;
- **ND** : non documentée ;
- **ROMPUE** : aucun lien.

| # | A → B | Événement / information | Canal | Accusé / acceptation | Transfert de responsabilité / trace | Clôture | Classe |
|---|---|---|---|---|---|---|---|
| F1 | Trouveur → intercommunalité | Signalement | Numéro vert (messagerie et astreinte le week-end au TCO) | U | Aucun avant la capture ; trace U | U | HS / ND |
| F2 | Trouveur → I-CAD → détenteur | « Trouvé » | Filalapat | Alerte | — | « Retrouvé » supprime l'annonce | AUTO |
| F3 | Trouveur ou propriétaire → Pet Alert | Annonce | Formulaire → validation par l'équipe → réseaux | Validation | — | U | HS |
| F3b | Pet Alert ↔ I-CAD / fourrières | — | — | — | — | — | ROMPUE (aucun lien documenté) |
| F4 | Fourrière → I-CAD | Entrée, lecture de puce | U | — | — | — | ND (effet aval AUTO vers Filalapat) |
| F5 | Propriétaire → fourrière | Réclamation | Téléphone, sur place | Restitution | Propriétaire ; quittance (I) | Restitution | HS |
| **F6** | **Fourrière → refuge ou association** | **Animal cessible** | **U** | **U** | — | — | **ND** |
| **F7** | **Refuge ou association → fourrière** | **Acceptation** | **U** | **U** | Cession + I-CAD (I) | U | **ND** |
| F8 | Structure → I-CAD | Changement de détenteur | Procédure I-CAD | Oui (I) | Détenteur mis à jour | — | HS |
| F9 | Famille d'accueil ↔ BNO ↔ association | Collaboration | BNO | Acceptation ou refus, courriels | Relation active | Fin datée | AUTO / HS |
| **F10** | **Association → famille d'accueil** | **Proposition d'un animal** | Téléphone, Facebook (R/O) ; logiciel U | **U** | Contrat L214-6-6 | Retour ou adoption | **INF / ND** |
| F11 | Association → famille d'accueil | Contrat, document d'information, certificat vétérinaire | Papier ou numérique (U) | Signature | Garde sans transfert de propriété | — | HS |
| F12 | Association (île) → association ou famille d'accueil (métropole) + voyageur + compagnie | Transfert | Facebook, téléphone, réservation aérienne | U | U | U | INF |
| F13 | Acteurs → StopErrance | Données | Questionnaire (application) | U | — | — | HS (sens retour U) |
| F14 | Citoyen → StopErrance → services habilités | Signalement (CGU) | Application | « Aucune garantie de prise en charge » (CGU) | U | U | ND |
| F15 | Citoyen ou éleveur → mairie / police municipale | Divagation, attaque | Téléphone, guichet | U | U | U | HS / ND |
| F16 | Trouveur → SEOR → poste-relais → bénévole → centre | Oiseau | Téléphone + réseau physique | Accord téléphonique | SEOR | Relâcher | HS |
| F17 | Trouveur → GLOBICE → Réseau échouage → national | Cétacé | Numéro unique | U | Porteurs de la carte verte | Examen | HS |
| F18 | Trouveur → Kélonia | Tortue | Téléphone | U | Kélonia | U | HS |
| F19 | Association → DAAF / BNO → DDPP | Déclaration | Courriel DAAF + BNO | Récépissé | — | — | HS (double canal, I) |
| F20 | Association ou refuge → adoptant | Cession | Certificat d'engagement, délai de 7 jours, I-CAD | Signature | Adoptant | — | HS |
| F21 | Structure → toute autre structure | Capacité, occupation | — | — | — | — | ROMPUE / inexistante |

---

## LIVRABLE G — Registre des doublons

### G1. Matrice information × système (perdu / trouvé / fourrière)

**Légende :** ● saisi (documenté) ; ◐ possible ou déclaré par l'éditeur ; ○ absent ; ? inconnu.

| Information | I-CAD | Filalapat | Pet Alert | Facebook / autres sites | Fourrière | Vétérinaire | StopErrance |
|---|---|---|---|---|---|---|---|
| Photo | ? | ● | ● | ● | ? | ? | ? |
| Espèce / sexe / description | ● | ● | ● | ● | ● (I) | ● | ? |
| Identification (puce) | ● | ● | ◐ | ◐ | ● (lecture) | ● (lecture) | ? |
| Date / lieu | ◐ (perte) | ● | ● | ● | ● (capture, I) | ○ | ? |
| Coordonnées | ● | ● (masquées ensuite) | ● (publication anonyme, R) | ● | ? | ? | ? |
| Statut perdu / trouvé | ● | ● | ● | ● | ○ | ○ | ? |
| Entrée en fourrière | ● (déclenche l'alerte) | ● (notification) | ○ | ○ | ● | ○ | ◐ (agrégé) |
| Restitution | ◐ | ● (« retrouvé ») | ? | ? | ● | ○ | ◐ (agrégé) |
| Clôture de l'annonce | ● | ● (suppression) | ? | ○ / manuelle | — | — | — |

### G2. Doublons identifiés

| # | Doublon | Systèmes | Synchronisation | Niveau |
|---|---|---|---|---|
| D1 | Annonce de perte ou de découverte | Filalapat, Pet Alert, Facebook, chien-perdu.org, SOS chien perdu, 30 Millions d'Amis | Aucune documentée | O / I |
| D2 | Clôture après résolution | Automatique seulement sur Filalapat | Annonces non closes ailleurs | O / I |
| D3 | Description de l'animal par le propriétaire | Déposée à la fourrière (photo), sur les plateformes, auprès des associations et vétérinaires | Aucune | R (APPAR) |
| D4 | Cession | Registre de la fourrière, document de cession, I-CAD, registre de l'association, logiciel éventuel | Aucune | I |
| D5 | Famille d'accueil | BNO (identité, capacité), registre et contrat de l'association, logiciel éventuel (Pawer : disponibilités) | Aucune | O / I |
| D6 | Association sans refuge | Déclaration DAAF + BNO | Inconnue ; la BNO devait remplacer la déclaration (R Solidarité Peuple Animal) | R / I |
| D7 | Données d'activité | Registres des fourrières → questionnaire StopErrance | Ressaisie probable (I) | I |
| D8 | Numéros de contact | Sites des 5 intercommunalités, StopErrance, APPAR, Filalapat « Autour de moi » | Divergences possibles (déjà vu : CIVIS 0262 35 25 58 selon le site intercommunal, 0262 352 558 sur StopErrance, même numéro) | O |

---

## LIVRABLE H — Registre des ruptures

**Règle appliquée :** l'absence d'API n'est pas une rupture en soi. Les fréquences non publiées sont marquées U.

| # | Rupture | Information nécessaire vs disponible | Canal actuel | Conséquence | Fréquence | Plus simple possible | Liaison logicielle nécessaire ? | Importance potentielle | Preuve |
|---|---|---|---|---|---|---|---|---|---|
| R1 | Proposition d'un animal cessible fourrière → structures ; acceptation | Liste datée des animaux cessibles, profil, date limite, réponse | **U** | Euthanasie si aucun preneur dans le délai | U | Protocole de diffusion et réponse horodatée (courriel ou liste) | **Non démontrée** | Haute | U |
| R2 | Pas de liste publique des animaux présents en fourrière | Photo et date d'entrée par animal ; propriétaire d'animal non identifié limité à 4 jours | Appels, dépôt de photo (R APPAR) ; trombinoscope CIREST en panne (O) | Restitutions manquées (H) | U | Page publique de photos mise à jour par la fourrière | Non | Haute pour les animaux non identifiés | O / R |
| R3 | Perdu/trouvé fragmenté, sans clôture | — | Au moins 5 supports | Recherches redondantes ; annonces périmées | U | Orientation unique (I-CAD + fourrière + Pet Alert) | Non | Moyenne | O / I |
| R4 | Coordonnées I-CAD périmées | Coordonnées à jour | Responsabilité du détenteur | Alerte inopérante | U | Sensibilisation | Non | Moyenne | R |
| R5 | Disponibilité des familles d'accueil invisible hors de chaque association | Disponibilité réelle et compatibilité | BNO (capacité maximale seulement) ; Pawer/Pattoune (R) | Places non mobilisées (**H2**) | U | Tableau partagé volontaire entre 2 à 3 associations | Non démontrée | Dépend de H2 | O / R |
| R6 | « Sauvetages » directs d'animaux de rue par des associations sans refuge vs provenances autorisées par L214-6-5 | Qualification juridique | — | Risque juridique pour les associations et pour tout système qui formaliserait ce flux | U | Clarification DAAF | **Non** (préalable juridique) | Haute | R / I |
| R7 | Discours publics locaux conformes au droit antérieur à 2021 (cession réservée aux refuges) | Droit en vigueur | Sites institutionnels, presse | Sous-utilisation possible des associations sans refuge comme débouché (**H**) | U | Information juridique | Non | Moyenne à haute | O |
| R8 | Refuge de la CASUD vacant (2022-2023) | Structure preneuse | Appel à candidatures | Aucun débouché : euthanasie à J+4 (R) | — | Organisationnel ou financier | Non | Haute, mais non informationnelle | R |
| R9 | Transferts vers l'Hexagone dépendants des voyageurs et des vols | Voyageurs disponibles | Facebook, réseaux | Blocage des sorties, donc saturation locale | Saisonnière (R) | Existant | Non démontrée | Moyenne | R |
| R10 | StopErrance : flux à sens unique vers la préfecture ; contenu des signalements U | Retour vers les acteurs | Application | Doublon possible avec toute nouvelle couche | — | Lire l'application ou interroger la préfecture | U | **Critique pour la décision** | O / U |
| R11 | Aucune circulation de la capacité ou de l'occupation | Places réelles | Aucun | Appels répétés (H) | U | Aucun | Non démontrée | U | I |
| R12 | Hors heures ouvrées (animal accidenté) | Service de garde | TCO : messagerie et astreinte ; autres U | Retard de prise en charge | U | Affichage de l'astreinte | Non | Moyenne | O / U |

**Lecture critique :**

- Sur 12 ruptures, **aucune** n'exige démontrablement une liaison logicielle.
- R1, R5 et R10 sont les seules où une solution d'information pourrait avoir un effet. R1 et R5 restent U quant à leur existence réelle, et R10 est un risque de doublon.
- R6, R7 et R8 sont juridiques ou organisationnelles, et doivent être traitées avant toute conception.

---

## LIVRABLE I — Cartographie des familles d'accueil

| Étape | Obligation légale | Pratique observée à La Réunion | Couvert par | Lacune |
|---|---|---|---|---|
| Recrutement | — | StopErrance renvoie vers la liste DAAF (O) ; page TCO vers le formulaire de l'APEBA et sa page Facebook (O) ; formulaire RPA puis « Pôle Famille d'Accueil » (O) ; sites nationaux type AnimauxFA (R) | Pawer (réseau de familles d'accueil, R) ; Pattoune (annuaire, R) | Aucune plateforme locale commune observée |
| Validation | Choix par un représentant compétent de l'association | Critères non publiés (U) ; rappel téléphonique (RPA, O) | Pawer : formulaires (R) | U |
| Enregistrement | Coordonnées obligatoires dans la BNO (L214-6-6 4° selon la FAQ SPA) ; amende possible sinon (R) | Obligation rappelée par StopErrance (O) | **BNO** : création par l'association ou auto-inscription avec le SIRET → demande de collaboration → acceptée / refusée (O) | — |
| Capacité | Capacité maximale par espèce | Déclarative (O) | BNO | Non vérifiée |
| Disponibilité | Aucune | U | **Pas la BNO** (flux non enregistrés, R) ; Pawer (R) | **Aucune source commune** |
| Matching | Association | Téléphone (RPA, O) ; annonces Facebook (APEBA, O) | Pawer : préférences et propositions (R) | U |
| Acceptation | Implicite dans le contrat | U | — | U |
| Transfert | Contrat d'accueil, document d'information, certificat vétérinaire sous 7 jours (O, guide StopErrance) | Support U | Hunimalis / Pawer : documents (R) | — |
| Suivi | Frais pris en charge par l'association (O guide) | U | Pawer : espace famille d'accueil, rendez-vous (R) | U |
| Fin | Adoption par un tiers ou retour ; fin de collaboration BNO datée (O) | U | BNO (fin de relation), pas la libération de place | La « place libérée » n'existe dans aucun système commun |

**Constat (I) :** la BNO couvre l'identité, la relation et la capacité maximale, avec de vraies transitions d'états et des notifications. La seule couche absente, **disponibilité puis proposition puis acceptation**, est justement ce que Pawer et Pattoune revendiquent (R). Avant tout développement, le test pertinent est donc la configuration d'un outil existant par 2 ou 3 associations, et non un nouveau système.

---

## LIVRABLE J — Hors chiens et chats : tronc commun et branches

| Famille | Premier contact | Relais / transport | Prise en charge | Issue | Systèmes | Intégrable dans une couche commune ? |
|---|---|---|---|---|---|---|
| Oiseaux marins et terrestres, chauves-souris | SEOR | Postes-relais et bénévoles | Centre de Saint-André | Relâcher (85 % en moyenne selon Wikipédia, R) | Téléphone ; registre U | **Orientation seulement** |
| Tortues marines | Kélonia | U | Centre de soins | U | Téléphone | Orientation seulement |
| Cétacés | GLOBICE (numéro unique du Réseau échouage) | Porteurs de la carte verte | Examen | Données nationales | Base Pelagis (I) | Orientation seulement (espèces protégées, habilitation exclusive) |
| NAC | I-CAD gère aussi un fichier NAC (R) ; Pet Alert annonce couvrir poules, oiseaux et tortues (R) | U | U | U | U | U |
| Animaux d'élevage divagants | Maire (L211-20 : lieu de dépôt désigné) | U à La Réunion | U | U | U | U |
| Attaques de cheptel | Mairie / police municipale + plainte (O StopErrance) ; aides du Département (O) | — | — | — | — | Hors champ du prototype |

**Tronc commun réel (I) :** seules les étapes **signal → qualification de l'espèce et de la situation → orientation vers le bon premier interlocuteur** sont communes. À partir de la « responsabilité », chaque branche a son propre détenteur d'autorité, et la faune sauvage fonctionne déjà sans lien avec les fourrières. Unifier les workflows au-delà de l'orientation n'est **pas justifié** par les éléments publics.

---

## ANNEXE 1 — Modèle conceptuel de la boucle (pas une architecture)

| Transition | Acteur autorisé | Source de vérité | Système actuel | Preuve produite | Rupture |
|---|---|---|---|---|---|
| Signal | Quiconque | Déclarant (non probant) | Téléphone, Filalapat, Pet Alert, StopErrance (CGU) | Annonce, appel | Fragmentation (R3) |
| Qualification | Vétérinaire, fourrière, spécialiste | Examen | — | Lecture de puce, examen | — |
| Orientation | Service public, spécialiste | Consignes officielles | StopErrance, sites des intercommunalités | Consignes | Faible |
| Responsabilité | Fourrière (chiens, chats), SEOR, Kélonia, GLOBICE | Loi / habilitation | Registres | Entrée | — |
| Demande | Fourrière → structure ; association → famille d'accueil | — | **U** | **U** | R1, R5 |
| Acceptation | Receveur | Receveur | **U** | **U** | R1 |
| Transfert | Émetteur + receveur | Document + I-CAD | I-CAD | Cession, contrat | Ressaisie (D4) |
| Prise en charge / suivi | Structure receveuse | Registre | Interne | Registre | U |
| Issue | Structure (adoption), fourrière (restitution ou euthanasie) | I-CAD, registre | I-CAD | Certificat, cession | — |
| Capacité libérée | Structure / famille d'accueil | Structure | **Aucun** | Aucune | R11 |
| Nouvelle demande | — | — | — | — | — |

**Test d'applicabilité :**

- La boucle complète ne s'applique qu'aux chiens et chats après leur entrée en fourrière ou leur prise en charge par une association.
- Elle ne s'applique **pas** aux cas suivants :
  - perdu/trouvé : pas de demande ni d'acceptation, c'est un rapprochement ;
  - faune sauvage : responsabilité unique du spécialiste, pas de « capacité libérée » partagée ;
  - animaux d'élevage : procédure de lieu de dépôt.
- Les transitions « demande », « acceptation » et « capacité libérée » sont précisément les seules dont le système actuel est U. Cela ne prouve pas un manque : c'est une absence de documentation publique.

---

## ANNEXE 2 — Carte des besoins de liaison (sans choix de solution)

| Besoin potentiel | Classement |
|---|---|
| Identification, alerte au propriétaire d'un animal identifié | **EXISTANT SUFFISANT** (I-CAD / Filalapat) |
| Déclaration des opérateurs, relation association ↔ famille d'accueil | **EXISTANT SUFFISANT** (BNO) |
| Orientation générale du public | **EXISTANT SUFFISANT** (StopErrance, sites des intercommunalités) ; au mieux **À REDIRIGER** |
| Orientation faune sauvage | **EXISTANT SUFFISANT** ; **À REDIRIGER** |
| Perdu/trouvé multi-plateformes | **À REDIRIGER** ; synchronisation **NON JUSTIFIÉE** (aucune API, Pet Alert pluri-opérateurs) |
| Liste publique des animaux en fourrière | **PROCESSUS HUMAIN SUFFISANT** (publication par la fourrière) ; besoin plausible, non démontré |
| Proposition et acceptation fourrière → structure | **BESOIN NON DÉMONTRÉ** ; à qualifier sur le terrain ; ensuite éventuellement **À COMPLÉTER** |
| Disponibilité et proposition association → famille d'accueil | **À COMPLÉTER** par un outil existant si H2 est vraie ; sinon **BESOIN NON DÉMONTRÉ** |
| Données vers StopErrance | **À RELIER SI AUTORISÉ** (U ; dépend de la préfecture) |
| Changement de détenteur I-CAD | **EXISTANT SUFFISANT** ; synchronisation **IMPOSSIBLE sans autorisation** |
| Capacité des structures en temps réel | **NON JUSTIFIÉ** en l'état (aucune source ; fraîcheur non garantissable) |
| Unification des workflows des espèces spécialisées | **NON JUSTIFIÉ** |

**Conséquence sur la forme d'un éventuel système (sans choisir) :**

- Les seules fonctions non couvertes publiquement relèvent d'une **couche de workflow minimale** : demande, réponse, horodatage, pour deux frontières (F6/F7 et F10).
- Elles relèvent aussi, éventuellement, d'un **portail d'orientation**, qui existe déjà en grande partie (StopErrance).
- Rien ne soutient à ce stade un orchestrateur, une couche d'intégration ou une couche événementielle.
- **« Rien du tout » reste une option ouverte**, si le terrain montre que F6/F7 fonctionnent déjà correctement par téléphone ou courriel au sein de conventions stables.

---

## LIVRABLE K — Questions de terrain (impossibles à trancher publiquement)

| # | Question | Acteur capable de répondre | Pourquoi | Décision permise | Hypothèse testée |
|---|---|---|---|---|---|
| K1 | Par quel canal, à quelle fréquence et sous quel format chaque fourrière propose-t-elle un animal cessible ? Comment la réponse est-elle reçue et tracée ? | Responsable de fourrière (régie / SEMRRE), associations conventionnées | Frontière F6/F7 inconnue | Liaison F6/F7 : utile, ou existant suffisant | H1, H4 |
| K2 | Sur un mois, combien d'animaux jugés adoptables ont été euthanasiés faute de preneur, contre faute de place ? | Fourrière + vétérinaire sanitaire | Sépare le défaut d'information du défaut de capacité | Continuer ou arrêter | **H1** |
| K3 | Que contient l'application StopErrance une fois connecté (signalements, destinataires, statuts, clôture, feuille de route) ? | Préfecture (stoperrance974@reunion.gouv.fr), 10positif | Risque de doublon critique | Doublon, donc arrêt ou articulation | **H5** |
| K4 | Quel logiciel ou registre chaque fourrière et chaque refuge utilise-t-il ? Avec quel export ? | Intercommunalités, SPA | Frontières F4/F8, doublons D4 | Faisabilité d'une liaison | H6 |
| K5 | Les associations sans refuge reçoivent-elles des cessions de fourrière depuis 2021 ? Sinon, pourquoi ? | Intercommunalités, DAAF, associations | Rupture R7 | Levier juridique vs logiciel | H (R7) |
| K6 | Comment sont qualifiés juridiquement les « sauvetages » de rue par les associations sans refuge ? | DAAF | Rupture R6 | Périmètre légal de tout flux formalisé | — |
| K7 | Combien de familles d'accueil déclarées dans la BNO sont réellement disponibles chaque mois ? Qui les suit, et comment ? | 3 à 5 associations | Rupture R5 | Configurer un outil existant (A3) ou rien | **H2, H3** |
| K8 | Une association utilise-t-elle déjà Pawer, Pattoune, Hunimalis ou Refugilys à La Réunion ? Avec quelles fonctions réellement utilisées ? | Associations | L'existant couvre peut-être déjà le besoin | Solution A3 | **H6** |
| K9 | Temps moyen entre la fin du délai et la cession ; nombre d'appels ou messages par cession | Fourrière + association | Mesure de la friction de base | Faut-il agir ? | H4, H7 |
| K10 | État actuel du refuge de la CASUD et débouchés des animaux capturés dans le Sud rural | CASUD | Contradiction A6 | Carte des débouchés | — |
| K11 | Délai réellement appliqué par la CIVIS aux animaux identifiés (4 ou 8 jours) | CIVIS | Contradiction résiduelle A4 | Exactitude juridique de l'orientation | — |
| K12 | Qui paierait une réduction mesurée de la friction sur F6/F7 : intercommunalité, État, associations ? | Intercommunalités, sous-préfet pilote | Payeur | Poursuite économique | **H8** |

---

## GATE FINAL

**DOCUMENTAIRE_INSUFFISANT, avec une borne stricte.**

Ce qui justifie ce verdict :

- Les frontières centrales (F6/F7) n'ont aucune documentation publique trouvée.
- Des sources publiques à forte valeur d'information restent identifiables et **n'ont pas été lues** :
  1. les **délibérations et conventions** entre les intercommunalités et les associations, notamment les 7 conventions CIREST, qui peuvent décrire le circuit de proposition et d'acceptation ;
  2. les **cahiers des charges (CCTP)** des marchés de fourrière CINOR, CIVIS et CASUD (registres imposés, logiciels, obligations d'information des associations) ;
  3. la **liste DAAF** du 23/04/2026, à lire manuellement car le site bloque l'accès automatisé, et le **recueil des actes administratifs** de la préfecture (arrêté sur le délai de garde, s'il existe).

Borne :

- Ce lot unique suffit.
- Si ces trois lectures ne documentent pas F6/F7, la conclusion passe automatiquement à **DOCUMENTAIRE_SUFFISANT_POUR_CARTOGRAPHIE_TERRAIN**, sans nouvelle passe documentaire. Continuer à chercher au-delà deviendrait un coût de gouvernance supérieur à l'information attendue.

Cette décision ne signifie ni PLATEFORME NÉCESSAIRE, ni PRODUIT VIABLE, ni INTERCONNEXION NÉCESSAIRE, ni PROJET À ABANDONNER.

---

## Registre des sources (consultées le 24/09/2026)

| Source | URL | Niveau | Ce qu'elle appuie |
|---|---|---|---|
| StopErrance, accueil | https://www.stoperrance.re/ | Primaire | Chiffres, acteurs, participation, contacts, guides, orientation des citoyens et des éleveurs |
| StopErrance, mentions légales | https://www.stoperrance.re/mentionslegales | Primaire | Éditeur : préfecture ; 10positif ; Webflow (A1) |
| StopErrance, CGU (v. 02/02/2026) | https://www.stoperrance.re/cgu | Primaire | Signalements, comptes (A2) |
| StopErrance, participer | https://www.stoperrance.re/participer | Primaire | Étude scientifique ; 10 catégories (A3) |
| StopErrance, guide « Être famille d'accueil » | https://cdn.prod.website-files.com/676cf3bc0408f5baeba10a62/6811be8f808822593c7fc52c_Etre_famille_d%27accueil.pdf | Primaire | Obligations des familles d'accueil, BNO |
| Imaz Press (15/06/2026) ; info.fr (10/06/2026) | imazpress.com/toute-l-actu/stop-errance-animale ; info.fr/... | Secondaire | Lancement ; « grand public » |
| I-CAD, guide BNO associations sans refuge | https://www.i-cad.fr/uploads/NEW_BNO_GUIDE_ASSOCIATIONS_SANS_REFUGE.pdf | Primaire | Workflow BNO (section 6, livrable I) |
| Solidarité Peuple Animal (BNO, FAQ) ; fiches SPA BNO | solidarite-peuple-animal.com ; la-spa.fr | Secondaire | Flux non enregistrés, obligations, finalités |
| Filalapat, FAQ | https://www.filalapat.fr/faq/... | Primaire (opérateur) | Alertes, entrée en fourrière, clôture |
| Service-public F24029 | https://www.service-public.gouv.fr/particuliers/vosdroits/F24029 | Primaire | Déclaration de perte I-CAD |
| Légifrance R271-9 ; section L211-11 à L211-28 ; Lexbase L211-25 | legifrance.gouv.fr ; lexbase.fr | Primaire (extraits) | Délais, cession aux associations L214-6-5 |
| TCO : fourrière ; famille d'accueil | tco.re | Primaire | 8 / 4 jours, tarifs, capacités, APEBA, liste ZOOM |
| CIREST : adoptez votre animal | https://www.cirest.fr/adoptez-votre-animal/ | Primaire | Conventions, trombinoscope en panne |
| Zinfos974 (19/02/2023) | zinfos974.com/errance-animale-derriere-les-effets-d-annonce-de-la-casud... | Secondaire | Refuge CASUD vacant, SEMRRE, tri des animaux |
| HelloAsso, annuaire Réunion | helloasso.com | Secondaire | Rôle de la SPA du Sud |
| Sauvade ; RPA ; APPAR | asso-sauvade.fr ; rpa974.wordpress.com ; appar.re | Acteurs | Familles d'accueil, co-avionnage, conseils en cas de perte |
| Imaz Press (2020) ; La 1ère (2021) ; Free Dom (2025) ; Zinfos (2018) | — | Secondaire | Co-avionnage, groupes Facebook |
| Pawer ; Pattoune ; Hunimalis ; Refugilys | pawer.fr ; pattoune-adoption.fr ; hunimalis.com ; refugilys.org | Commercial | Fonctions annoncées (R uniquement) |
| Pet Alert France ; Pet Alert 974 | petalert.fr ; pet-alert-974.fr ; facebook.com/Pet.Alert.Reunion.974 | Opérateur / secondaire | Workflow des annonces |
| GLOBICE, signaler un échouage | https://www.globice.org/sengager/signaler-un-echouage/ | Primaire | Réseau échouage, numéro unique |
| SEOR ; Fondation Koesio ; LPO | seor.fr ; fondation.koesio.com ; lpo.fr | Primaire / secondaire | Postes-relais |
| CEDTM | https://cedtm-asso.org/ | Secondaire | Numéro de Kélonia |
| DAAF, compte rendu de réunion du 11/12/2015 | daaf.reunion.agriculture.gouv.fr/IMG/pdf/CR_reunion_PA_11_12_15_cle054ef1.pdf | Primaire | Difficultés à trouver des familles d'accueil (2015) |
| DAAF, liste des associations sans refuge | daaf.reunion.agriculture.gouv.fr/...a3888.html | Primaire | **Non lue (robots)** |

**Indépendance des sources :** plusieurs articles (Imaz Press, info.fr, Parallèle Sud) reprennent les chiffres de StopErrance ou de la préfecture. Leur accord ne constitue pas une corroboration indépendante. Les fonctions de Pawer, Pattoune et Hunimalis reposent sur une seule source chacune, l'éditeur.