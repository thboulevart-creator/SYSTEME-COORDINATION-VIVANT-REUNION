# Système de coordination du vivant à La Réunion

## Vision générale

Ce dépôt documente un travail de recherche, de cartographie opérationnelle et d’ingénierie de système consacré à une question simple en apparence, mais complexe dans la réalité :

> Comment permettre à n’importe quelle personne présente à La Réunion, quelle que soit sa connaissance du territoire, des organismes locaux ou des procédures administratives, de comprendre rapidement ce qu’elle a devant elle, de savoir quoi faire et d’être orientée vers la bonne structure lorsque le vivant nécessite une intervention ?

Le projet est né d’un cas concret : lorsqu’une personne trouve un animal perdu, abandonné, blessé ou simplement inconnu, elle peut être confrontée à une multitude d’acteurs, de sites, de procédures et de responsabilités différentes.

Fourrières, intercommunalités, associations, refuges, familles d’accueil, vétérinaires, I-CAD, BNO, Filalapat, StopErrance, plateformes perdu/trouvé, organismes spécialisés dans la faune sauvage et services publics possèdent chacun une partie de la réponse.

Le problème potentiel n’est donc pas nécessairement l’absence de services.

Il peut résider dans leur fragmentation.

L’objectif du projet est de comprendre précisément cet écosystème avant de déterminer si une nouvelle architecture peut améliorer sa cohérence, sa lisibilité et sa fluidité.

---

# 1. Le problème étudié

Une personne qui trouve un animal ne devrait idéalement pas avoir besoin de connaître à l’avance :

* la différence entre une fourrière, un refuge et une association sans refuge ;
* l’intercommunalité compétente pour la commune concernée ;
* le rôle exact d’I-CAD, Filalapat ou de la BNO ;
* les compétences de StopErrance ;
* les associations disponibles ;
* les règles applicables selon l’espèce ;
* les organismes spécialisés pour la faune sauvage ;
* les procédures permettant une restitution, une prise en charge, une cession ou un transfert ;
* les différents sites sur lesquels une information doit éventuellement être déclarée.

Le système étudié vise à réduire cette complexité pour l’utilisateur sans supprimer la spécialisation des organismes existants.

L’ambition n’est donc pas de remplacer les acteurs compétents.

Elle consiste à déterminer s’il est possible de rendre leurs fonctions complémentaires beaucoup plus faciles à comprendre et à utiliser comme un ensemble cohérent.

---

# 2. Hypothèse centrale

L’hypothèse de recherche actuelle est la suivante :

> Plusieurs organismes et logiciels peuvent fonctionner correctement individuellement tout en formant collectivement un système difficile à comprendre ou insuffisamment coordonné si les transitions entre eux sont fragmentées, informelles, redondantes ou mal documentées.

Nous cherchons donc moins à découvrir « le logiciel manquant » qu’à comprendre les **frontières** entre les systèmes.

Exemples :

Fourrière
→ association

Association
→ famille d’accueil

Particulier
→ service compétent

Animal perdu
→ I-CAD / Filalapat / fourrière / plateformes de signalement

Structure émettrice
→ structure receveuse

Demande
→ réponse
→ acceptation
→ transfert effectif

C’est à ces frontières que peuvent apparaître des appels répétés, doubles saisies, informations périmées, demandes sans accusé de réception, responsabilités ambiguës ou parcours difficiles à suivre.

---

# 3. Ce que le projet ne suppose pas

Le projet ne considère pas qu’une nouvelle plateforme est nécessaire par défaut.

Il ne suppose pas non plus que les systèmes existants sont défaillants.

I-CAD, BNO, StopErrance, Filalapat, les logiciels associatifs, les registres de fourrière et les organismes spécialisés possèdent des fonctions et des responsabilités propres.

Une éventuelle architecture future devrait donc chercher à :

**réutiliser ce qui fonctionne ;**

**orienter vers les systèmes compétents ;**

**relier les étapes lorsque cela apporte une valeur démontrable ;**

et seulement développer de nouvelles fonctions lorsque les solutions existantes ou une simple amélioration organisationnelle ne suffisent pas.

La solution finale peut donc être une plateforme, une couche de workflow, un portail, un système d’orchestration minimal, un protocole organisationnel ou même l’absence de nouveau logiciel.

---

# 4. Principe de source de vérité

Un principe fondamental du projet consiste à ne pas transformer une future interface centrale en propriétaire artificiel de toutes les informations.

Chaque information doit rester rattachée à son autorité légitime.

Exemples conceptuels :

I-CAD
→ identification et détenteur enregistré.

BNO
→ opérateurs déclarés, établissements, familles d’accueil et capacité maximale déclarée.

Fourrière
→ présence physique, entrée, sortie et actes relevant de son registre.

Association
→ décisions concernant ses familles d’accueil, ses prises en charge et ses dossiers.

Organismes spécialisés
→ qualification et prise en charge relevant de leur compétence.

Une éventuelle couche commune pourrait devenir source de vérité uniquement pour les événements qu’elle crée elle-même, par exemple :

demande envoyée ;

demande reçue ;

acceptation ;

refus ;

transfert attendu ;

transfert confirmé ;

dossier clôturé.

---

# 5. Trois axes de recherche terrain

Une fois la cartographie documentaire terminée, le projet sera étudié selon trois axes indépendants.

## Axe A — Accessibilité universelle à l’action

La question n’est pas de savoir si une personne connaît aujourd’hui les procédures.

L’objectif est justement qu’elle n’ait pas à les connaître.

La question devient :

> Peut-on permettre à une personne, quelle que soit sa nationalité, sa langue ou sa connaissance de La Réunion, de partir uniquement de ce qu’elle observe et d’être conduite rapidement vers la compréhension et l’action appropriées ?

Nous devons mesurer la charge réelle imposée aujourd’hui :

nombre de sites visités ;

recherches nécessaires ;

informations difficiles à comprendre ;

nombre d’appels ;

doubles saisies ;

décisions que l’utilisateur doit reconstruire seul ;

moment où il ne sait plus quelle action réaliser.

## Axe B — Parcours inter-structures

La question est :

> Une fois qu’un dossier entre dans l’écosystème, comment l’information et la responsabilité passent-elles réellement d’une organisation à l’autre ?

Nous étudierons notamment :

fourrière → association ;

association → famille d’accueil ;

association → association ;

organisme → I-CAD ;

structures → StopErrance ;

transferts vers l’Hexagone lorsque pertinents.

Le but est de déterminer si les transitions sont déjà efficaces ou si elles reposent sur des appels, courriels, messages privés ou ressaisies susceptibles de produire de la friction.

## Axe C — Parcours de l’animal

La question devient :

> Peut-on savoir sans ambiguïté qui prend actuellement en charge l’animal, quel est son état administratif et quelle est la prochaine action attendue ?

Il faut distinguer :

signalement ;

responsabilité juridique ;

responsabilité opérationnelle ;

présence physique ;

demande de prise en charge ;

acceptation ;

transfert ;

suivi ;

issue finale.

---

# 6. Scénario de référence

Un scénario sert de fil directeur pour tester la valeur d’une future architecture.

## Un chien est trouvé à La Réunion

Une expérience cible pourrait un jour être :

**Chien trouvé**

→ interface unique

→ commune automatiquement reliée à l’EPCI compétent

→ procédure correcte affichée

→ orientation de la déclaration perdu/trouvé vers le système approprié

→ informations utiles réunies dans un parcours compréhensible

→ suivi de la situation

→ si juridiquement admissible, demande de prise en charge

→ réponse d’une structure

→ éventuelle proposition à une famille d’accueil

→ acceptation

→ transfert confirmé

→ suivi jusqu’à l’issue.

L’utilisateur ne devrait idéalement pas avoir besoin de comprendre lui-même l’ensemble des systèmes sous-jacents.

Il devrait seulement savoir :

**ce qu’il doit faire maintenant ;**

**pourquoi ;**

**qui devient responsable ensuite ;**

**et ce qui doit normalement se passer après.**

Ce scénario reste une hypothèse de conception à tester, et non une architecture validée.

---

# 7. Voir → Comprendre → Agir

Le projet possède également une extension de vision plus large concernant le vivant réunionnais.

Une personne peut rencontrer un organisme sans même savoir ce qu’elle observe.

Il peut s’agir :

d’un animal domestique ;

d’un animal sauvage ;

d’un oiseau marin ;

d’un reptile ;

d’un insecte ;

d’une plante ;

d’une espèce protégée ;

d’une espèce invasive ;

d’un organisme blessé ou en détresse.

L’expérience à long terme envisagée pourrait suivre trois étapes :

## VOIR

L’utilisateur photographie ce qu’il rencontre.

## COMPRENDRE

Le système propose une identification prudente, accompagnée d’un niveau de confiance, d’alternatives éventuelles et d’une fiche pédagogique issue de référentiels fiables.

Il peut apprendre :

le nom de l’espèce ;

ses caractéristiques ;

sa présence à La Réunion ;

son habitat ;

son statut ;

les précautions éventuelles ;

sa place dans l’écosystème local.

## AGIR

Lorsque la situation nécessite une intervention, le système ne s’arrête pas à l’identification.

Il explique précisément la conduite appropriée :

ne pas toucher ;

mettre en sécurité selon une procédure déterminée ;

contacter une structure ;

utiliser un poste-relais ;

signaler l’observation ;

faire vérifier une identification ;

ou simplement laisser l’organisme tranquille.

L’identification automatique ne doit jamais être confondue avec une certitude.

Une photographie peut permettre de produire des candidats, pas nécessairement une identification définitive.

Les situations sensibles devront conserver une validation ou une orientation humaine.

---

# 8. Une interface universelle, des parcours spécialisés

Le projet ne cherche pas à imposer un workflow unique à tout le vivant.

Un chien trouvé, un pétrel échoué, une tortue marine, un cétacé, un chat errant et un animal d’élevage ne relèvent pas des mêmes autorités ni des mêmes procédures.

Le tronc commun pourrait être :

**OBSERVATION**

→ **QUALIFICATION**

→ **ORIENTATION**

Puis chaque situation bascule vers son parcours spécialisé.

Cette séparation permettrait de proposer une expérience simple au public tout en respectant les compétences des acteurs spécialisés.

---

# 9. Architecture de liaison candidate

Aucune architecture technique n’est encore adoptée.

Une direction de recherche apparaît néanmoins :

> construire éventuellement une couche fédérée de coordination plutôt qu’une base centralisée remplaçant les systèmes existants.

Conceptuellement :

**PORTE D’ENTRÉE UNIVERSELLE**

→ **COMPRÉHENSION DE LA SITUATION**

→ **ORIENTATION**

→ **DEMANDE**

→ **RÉPONSE**

→ **ACCEPTATION**

→ **TRANSFERT**

→ **SUIVI**

→ **CLÔTURE**

Pendant que les systèmes existants continuent d’exercer leurs propres responsabilités.

L’innovation recherchée se situe donc potentiellement dans l’**orchestration des transitions**, plutôt que dans la duplication des fonctions déjà existantes.

---

# 10. Recherche de frictions

Une phase importante du projet consistera à rechercher systématiquement tout ce qui oblige aujourd’hui un humain à :

chercher ;

comprendre plusieurs sites ;

ressaisir une information ;

téléphoner à plusieurs organismes ;

attendre une réponse sans accusé de réception ;

répéter une demande ;

vérifier manuellement qu’un organisme a accepté ;

chercher une famille d’accueil ;

mettre à jour plusieurs annonces ;

reconstituer l’historique d’un dossier ;

ou déterminer qui est désormais responsable.

Chaque friction sera étudiée selon une chaîne commune :

**ACTION**

→ **FRICTION**

→ **CAUSE**

→ **CONSÉQUENCE**

→ **SOLUTION ACTUELLE**

→ **ALTERNATIVE PLUS SIMPLE**

→ **ÉVENTUELLE SOLUTION DE LIAISON**

→ **VALEUR MESURABLE.**

Le développement ne sera justifié que lorsqu’un problème est suffisamment démontré.

---

# 11. État actuel des recherches

Les travaux documentaires ont déjà permis de cartographier une partie importante de l’écosystème réunionnais.

Ils couvrent notamment :

les principales autorités ;

les intercommunalités ;

les fourrières ;

les refuges ;

les associations ;

les familles d’accueil ;

les vétérinaires ;

I-CAD ;

BNO ;

Filalapat ;

StopErrance ;

Pet Alert ;

plusieurs logiciels associatifs ;

les organismes spécialisés pour certaines espèces ;

les parcours perdu/trouvé ;

les transferts ;

les doublons d’information ;

les sources de vérité ;

et les frontières entre acteurs.

Certaines transitions essentielles restent toutefois insuffisamment documentées publiquement.

C’est notamment le cas de la proposition d’un animal cessible par une fourrière à une association et de la manière dont l’acceptation est reçue, enregistrée et suivie.

Le projet se trouve donc encore en phase de recherche.

---

# 12. Discipline épistémique

Chaque information importante doit être classée selon son niveau de preuve.

**OBSERVED**

Directement constaté dans une source primaire ou une interface publique.

**REPORTED**

Déclaré par un organisme, un éditeur ou une source secondaire.

**INFERRED**

Déduit de plusieurs éléments disponibles.

**HYPOTHESIS**

Proposition qui doit être testée.

**UNKNOWN**

Information insuffisamment établie.

Une absence de documentation publique n’est jamais considérée comme une preuve d’absence.

Une fonctionnalité commerciale annoncée n’est jamais considérée comme testée.

Une architecture techniquement possible n’est jamais considérée comme utile avant démonstration du besoin.

---

# 13. Séquence actuelle du projet

Le travail suit une progression volontairement gouvernée.

La phase actuelle consiste à terminer un dernier lot documentaire borné :

conventions et délibérations entre collectivités et associations ;

cahiers des charges et documents publics concernant les fourrières ;

liste DAAF des associations sans refuge ;

actes préfectoraux pertinents.

Une fois ce lot terminé, aucune campagne documentaire générale supplémentaire ne doit être ajoutée sans justification nouvelle.

Le projet passera ensuite à la cartographie terrain selon les axes :

**A — accessibilité universelle à l’action ;**

**B — coordination inter-structures ;**

**C — continuité du parcours de l’animal.**

Puis viendra la recherche structurée des frictions.

Ce n’est qu’après ces étapes qu’une architecture logicielle pourra être comparée à des solutions plus simples.

---

# 14. Mémoire expérimentale

Ce dépôt doit conserver l’intégralité du raisonnement ayant conduit aux décisions.

Il doit notamment préserver :

les hypothèses ;

les sources ;

les contradictions ;

les erreurs corrigées ;

les expériences ;

les résultats ;

les solutions rejetées ;

les limitations ;

les décisions ;

et les raisons ayant conduit à poursuivre, simplifier ou abandonner certaines directions.

L’objectif n’est pas seulement de conserver le résultat final.

Il est de conserver **le chemin de preuve permettant de comprendre pourquoi le système évolue dans une direction donnée.**

---

# 15. Finalité

La vision générale peut être résumée ainsi :

> Rendre le monde vivant réunionnais plus compréhensible et les parcours de protection plus accessibles, en transformant un ensemble d’acteurs et de systèmes spécialisés en une expérience cohérente, sans supprimer leur autonomie ni leurs responsabilités.

À terme, une personne pourrait simplement partir d’une situation :

> « J’ai trouvé cet animal. »

ou même :

> « Qu’est-ce que je viens de trouver ? »

Et recevoir progressivement :

**ce que cela pourrait être ;**

**ce qu’il faut comprendre ;**

**ce qu’il faut faire ;**

**qui peut aider ;**

**comment transmettre la situation ;**

**et ce qui doit se passer ensuite.**

Le projet cherche à déterminer si cette continuité peut être créée de manière fiable, juridiquement correcte, techniquement réaliste et réellement utile aux humains, aux organismes et au vivant qu’ils cherchent à protéger.

---

## Statut du dépôt

**RECHERCHE ET CONCEPTION — AUCUN PRODUIT VALIDÉ**

Ce dépôt constitue une base de recherche, de gouvernance et d’expérimentation.

Il ne représente actuellement ni un service public, ni une plateforme opérationnelle, ni un dispositif officiel de secours, ni un substitut aux organismes compétents.
