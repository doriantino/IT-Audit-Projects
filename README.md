# IT-Audit-Projects

Entend q'auditeur IT nous allons évaluee si les systèmes d'information des organisation (ordinateurs, réseaux, logiciels, données) sont :

- Sécurisés : Protégés contre les accès non autorisés, les modifications ou destructions.
- Fiables : Fonctionnent correctement et produisent des informations exactes.
- Disponibles : Accessibles quand les utilisateurs en ont besoin.
- Conformes : Respectent les lois, les réglementations (comme le RGPD en Europe, ou d'autres régulations bancaires) et les politiques internes de l'entreprise.
- Efficaces et efficient : Utilisés de manière optimale pour atteindre les objectifs de l'organisation.

Nous ne réparns pas les systèmes, nous identifions les faiblesses, les risques et proposns des recommandations pour les améliorer. Nous avons les rôles de contrôle et de conseil.

# Pourquoi un Audit IT dans une Banque est-il Crucial ?
Le secteur bancaire est l'un des plus réglementés et des plus critiques en termes de sécurité de l'information. Voici pourquoi l'audit IT y est indispensable :

- Confiance des clients : Les clients confient leur argent et leurs données personnelles. Toute faille peut détruire cette confiance.
- Risque financier : La fraude ou des erreurs systèmes peuvent entraîner des pertes financières massives pour la banque et ses clients.
- Conformité réglementaire : Les banques doivent se conformer à une multitude de lois et de régulations strictes (anti-blanchiment d'argent, protection des données, stabilité financière, etc.). Les amendes en cas de non-conformité sont astronomiques.
- Réputation : Une cyberattaque ou une faille de sécurité majeure peut gravement nuire à la réputation d'une banque.
- Complexité des systèmes : Les banques utilisent des systèmes IT extrêmement complexes et interdépendants, ce qui augmente la surface d'attaque et la difficulté à gérer les risques.

# Notre contexte est celui d'une Mission Fictive chez "BankSecur"
Nous sommes en mission chez BankSecur, une banque de taille moyenne axée sur le digital. Nos objectifs sont très concrets :

## Audit de la Détection de Fraude sur les Transactions en Ligne :

Concept : La fraude est une préoccupation majeure. Il s'agit de s'assurer que les systèmes de la banque sont capables d'identifier et de bloquer les transactions illégitimes (par exemple, quelqu'un qui utilise une carte volée ou accède à un compte sans autorisation).
Pourquoi l'auditer ? Si les systèmes de détection ne sont pas efficaces, la banque subira des pertes financières, ses clients seront impactés, et elle pourrait être sanctionnée par les régulateurs pour n'avoir pas protégé ses clients.
Ce que nous cherchons : Nous allons vérifier si les alertes de fraude sont bien générées, si les transactions frauduleuses sont effectivement détectées et si les mécanismes de prévention fonctionnent.
Audit des Contrôles d'Accès aux Systèmes Critiques :

Concept : Les "contrôles d'accès" sont les mécanismes (mots de passe, biométrie, droits d'utilisateur) qui garantissent que seules les personnes autorisées peuvent accéder à certaines informations ou fonctionnalités.
Pourquoi l'auditer ? C'est la première ligne de défense. Si n'importe qui peut accéder aux bases de données des clients ou aux systèmes de virement, c'est une catastrophe assurée. Nous voulons s'assurer que seuls les employés qui doivent accéder à certaines données ou systèmes y ont accès, et que cet accès est tracé et surveillé.
Ce que nous cherchons : Nous allons vérifier qui accède à quoi, quand, et si cela correspond aux droits qui leur sont attribués. Nous chercherons des accès non autorisés, des échecs de connexion suspects (tentatives d'intrusion), ou des comptes d'utilisateurs avec des droits excessifs.
Les Données : Notre Matière Première d'Auditeur
En tant qu'auditeur IT, les données sont vos yeux et vos oreilles. Elles contiennent la vérité sur ce qui se passe réellement dans les systèmes.

## Types de données ?
- Transactions (pour la fraude) : Chaque transaction est un événement traçable. En l'analysant, nous pouvons identifier des motifs suspects qui indiqueraient une fraude. Le Flag_Fraude_Banque est crucial : il nous dit ce que la banque pense être une fraude, que nous allons confronter à nos propres analyses.
- Logs d'Accès (pour les contrôles d'accès) : Un "log" est un enregistrement automatique d'événements. Chaque fois que quelqu'un se connecte, tente d'accéder à un fichier, ou échoue à se connecter, c'est enregistré. Ces logs sont une mine d'informations pour voir si les règles d'accès sont respectées.
- Référentiel Utilisateurs/Droits : C'est le "qui devrait avoir accès à quoi". Sans ce référentiel, les logs d'accès sont difficiles à interpréter car on ne sait pas si un accès était légitime ou non.


## OUTIL : Alteryx - Notre Outil Puissant pour l'Analyse de Données

# Pourquoi Alteryx ?
Alteryx est un outil de préparation des données, de mélange de données et d'analyse avancée qui permet aux utilisateurs de créer des workflows visuels.

- Pas de code (ou très peu) : C'est un atout majeur si vous n'êtes pas un développeur. Vous glissez-déposez des outils sur une toile, vous les connectez et configurez. C'est intuitif et puissant.
Rapidité : Il peut traiter d'énormes volumes de données très rapidement.
- Transparence : Chaque étape de votre analyse est visible dans le workflow, ce qui est parfait pour un audit où la traçabilité est essentielle. Un autre auditeur ou un contrôlé peut facilement comprendre votre logique.
- Diversité des connecteurs : Il peut se connecter à presque n'importe quelle source de données (fichiers Excel, CSV, bases de données, applications cloud, etc.).
- Capacités d'analyse : Il permet non seulement de nettoyer et transformer les données, mais aussi d'effectuer des analyses statistiques, géospatiales, prédictives, et même d'intégrer des modèles de Machine Learning.

Rôle clé que jouera Alteryx pour ce projet : 
- Importation : Importer nos données (CSV, Excel) de Kaggle.
- Nettoyage : Gérer les données manquantes, corriger les erreurs, uniformiser les formats.
- Transformation : Créer de nouvelles colonnes (par exemple, "Heure du jour" à partir de "Date_Heure"), agréger les données.
- Analyse : Appliquer des règles pour identifier les fraudes, détecter des anomalies dans les logs d'accès, joindre différentes sources de données.
- Reporting : Générer des résumés, des tableaux, et potentiellement des visualisations.
