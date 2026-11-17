# Renforcement du pare-feu dans une démarche PCR/PCA

## Objectif

Dans le cadre d'un Plan de Continuité des activités (PCA) ou d'un Plan de Reprise des activités (PRA/PCR), le pare-feu doit protéger les flux indispensables tout en permettant une reprise contrôlée des services.

## 1. Préparer le pare-feu

1. Inventorier les règles actuelles, les interfaces, les objets réseau et les applications autorisées.
2. Identifier les flux indispensables au fonctionnement critique : administration, messagerie, accès aux données, sauvegardes, DNS, authentification et téléphonie.
3. Sauvegarder la configuration courante avant toute modification.
4. Mettre à jour le logiciel et le micrologiciel à partir de sources officielles.
5. Vérifier les licences, les réserves de capacité et les droits d'accès administrateur.

## 2. Appliquer une politique stricte

- Commencer avec une posture « tout refuser » pour les flux entrants et indésirables.
- Autoriser uniquement les sources, destinations, protocoles et plages horaires nécessaires.
- Séparer les flux de chaque zone : utilisateurs, administration, serveurs, objets connectés et invités.
- Éviter les règles « tout autoriser » et les règles temporaires sans date d'expiration.
- Supprimer les règles obsolètes, dupliquées ou trop larges.
- Limiter les accès d'administration aux adresses ou réseaux approuvés.
- Désactiver les interfaces, services, fonctions cloud et connexions VPN inutilisés.

## 3. Sécuriser l'administration

- Utiliser des comptes nominatifs avec privilèges limités.
- Désactiver les comptes par défaut et appliquer l'authentification multifacteur si elle est disponible.
- Ne jamais exposer l'interface d'administration directement sur Internet.
- Préférer une administration depuis un réseau dédié ou via un VPN sécurisé.
- Autoriser les modifications selon un processus approuvé et consigner les changements.
- Conserver les journaux hors du pare-feu avec horodatage et synchronisation NTP.

## 4. Mettre en place les protections réseau

- Activer le filtrage d'État pour les connexions établies.
- Activer l'anti-spoofing sur les interfaces externes.
- Restreindre les flux ICMP aux seules fonctions nécessaires.
- Bloquer les adresses et pays uniquement si cela est justifié ; cette méthode ne remplace pas une politique précise.
- Activer les protections contre les scans, les déni de service et les connexions anormales disponibles sur l'équipement.
- Utiliser TLS, IPS/IDS et filtres applicatifs lorsque le matériel et les exigences le permettent.

## 5. Déployer progressivement

1. Documenter l'état initial et définir les critères d'acceptation.
2. Tester les règles dans un environnement de préproduction ou en mode simulation.
3. Planifier un créneau de maintenance et informer les équipes concernées.
4. Appliquer les règles par groupes limités, puis vérifier les journaux et les usages.
5. Conserver une procédure de restauration rapide de la sauvegarde.
6. Prévoir une solution de repli si un changement bloque un service critique.
7. Vérifier les applications depuis plusieurs postes, réseaux et profils utilisateurs.

## 6. Préserver la continuité

- Recenser les règles nécessaires à chaque service essentiel du PCA.
- Préconfigurer les règles de reprise sur un équipement secondaire.
- Tester régulièrement le basculement vers le pare-feu de secours.
- Documenter les adresses, identifiants, dépendances, procédures et responsables.
- Protéger les sauvegardes contre les accès non autorisés et les stocker séparément.
- Prévoir des scénarios pour une panne Internet, une panne matérielle ou une cyberattaque.

## 7. Surveiller et auditer

- Consulter les journaux de connexion, les refus répétés et les modifications de configuration.
- Centraliser les journaux dans un système surveillé et définir des alertes pertinentes.
- Effectuer des revues périodiques des règles avec les équipes réseau, sécurité et métiers.
- Réaliser un test de configuration après chaque changement majeur.
- Mesurer la disponibilité des services critiques pendant les tests de continuité.
- Supprimer ou corriger immédiatement toute règle ou règle temporaire devenue inutile.

## 8. Exemple de vérification après modification

- Le pare-feu est joignable depuis le réseau d'administration autorisé.
- Aucun service administratif n'est exposé depuis Internet.
- Les flux non autorisés sont rejetés et enregistrés.
- Les utilisateurs accèdent aux applications nécessaires depuis leur zone.
- Les objets connectés ne peuvent pas atteindre les serveurs sensibles sans nécessité.
- Les sauvegardes et flux de reprise fonctionnent.
- Les tests de reprise sont documentés avec les résultats et les écarts.

Ces mesures doivent être adaptées à la taille du réseau, aux contraintes d'exploitation et aux risques identifiés. Pour un système exposé ou sensible, faire valider la configuration par un administrateur réseau qualifié.
