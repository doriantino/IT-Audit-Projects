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

# DATA SET
## Context
There is a lack of public available datasets on financial services and specially in the emerging mobile money transactions domain. Financial datasets are important to many researchers and in particular to us performing research in the domain of fraud detection. Part of the problem is the intrinsically private nature of financial transactions, that leads to no publicly available datasets.

We present a synthetic dataset generated using the simulator called PaySim as an approach to such a problem. PaySim uses aggregated data from the private dataset to generate a synthetic dataset that resembles the normal operation of transactions and injects malicious behaviour to later evaluate the performance of fraud detection methods.

## Content
PaySim simulates mobile money transactions based on a sample of real transactions extracted from one month of financial logs from a mobile money service implemented in an African country. The original logs were provided by a multinational company, who is the provider of the mobile financial service which is currently running in more than 14 countries all around the world.

This synthetic dataset is scaled down 1/4 of the original dataset and it is created just for Kaggle.

NOTE: Transactions which are detected as fraud are cancelled, so for fraud detection these columns (oldbalanceOrg, newbalanceOrig, oldbalanceDest, newbalanceDest ) must not be used.
Headers
This is a sample of 1 row with headers explanation:

1,PAYMENT,1060.31,C429214117,1089.0,28.69,M1591654462,0.0,0.0,0,0

- step - maps a unit of time in the real world. In this case 1 step is 1 hour of time. Total steps 744 (30 days simulation).
- type - CASH-IN, CASH-OUT, DEBIT, PAYMENT and TRANSFER.
- amount -
amount of the transaction in local currency.
- nameOrig - customer who started the transaction
- oldbalanceOrg - initial balance before the transaction
- newbalanceOrig - new balance after the transaction.
- nameDest - customer who is the recipient of the transaction
- oldbalanceDest - initial balance recipient before the transaction. Note that there is not information for customers that start with M (Merchants).
- newbalanceDest - new balance recipient after the transaction. Note that there is not information for customers that start with M (Merchants).
- isFraud - This is the transactions made by the fraudulent agents inside the simulation. In this specific dataset the fraudulent behavior of the agents aims to profit by taking control or customers accounts and try to empty the funds by transferring to another account and then cashing out of the system.
- isFlaggedFraud - The business model aims to control massive transfers from one account to another and flags illegal attempts. An illegal attempt in this dataset is an attempt to transfer more than 200.000 in a single transaction.



# I. Observations Générales sur la Qualité des Données

## Problème Majeur de Types de Données (V_String partout) :
- Constat : Toutes les colonnes qui devraient être numériques (step, amount, oldbalanceOrg, newbalanceOrg, oldbalanceDest, newbalanceDest, isFraud, isFlaggedFraud) ont été importées par Alteryx comme des chaînes de caractères (V_String).
- Impact Audit : Cela rendait impossible toute opération numérique directe (calculs, filtrages par valeur, agrégations statistiques). C'est une faiblesse critique d'un point de vue de la qualité des données, qui aurait dû être corrigée en amont si ces données provenaient directement d'un système bancaire.
- Action Corrective : Nécessité absolue de convertir ces colonnes en types numériques appropriés (Double pour les montants/soldes, Byte pour les indicateurs 0/1) via l'outil Select, suivi d'un nettoyage (Data Cleansing) pour gérer les Nulls et les espaces parasites.

## Absence de Valeurs Manquantes Importantes :
- Constat : Pour toutes les colonnes examinées (amount, soldes, isFraud, isFlaggedFraud), aucune valeur Null ou vide n'a été détectée.
- Impact Audit : C'est un point positif. Cela simplifie la phase de nettoyage et suggère une certaine complétude des enregistrements de transactions.

# II. Observations Spécifiques sur les Données Financières

## Présence de Montants et Soldes Extrêmement Élevés :
- Constat : Les colonnes amount, oldbalanceOrg, newbalanceOrg, oldbalanceDest, newbalanceDest contiennent des valeurs qui, une fois converties en numérique, atteignent des dizaines de millions (ex: 1.46E8 pour oldbalanceDest = 146 millions).
- Impact Audit : Dans un contexte bancaire, ces transactions à très gros montants sont des points de risque élevés pour la fraude (notamment le blanchiment d'argent) et nécessitent des - contrôles internes et des validations spécifiques (par exemple, des limites transactionnelles, des validations manuelles pour les montants au-delà d'un certain seuil). L'efficacité des contrôles doit être testée pour ces transactions.

## Fréquence Élevée des Soldes à Zéro :
- Constat : Les valeurs 0.0 sont extrêmement fréquentes dans les colonnes oldbalanceOrg (plus de 1.3 millions) et newbalanceOrg (plus de 2.2 millions), ainsi que dans oldbalanceDest (plus de 1.7 millions) et newbalanceDest (plus de 1.5 million).
- Impact Audit : Un nombre aussi élevé de soldes à zéro (avant ou après transaction) peut être un indicateur de comportements anormaux ou frauduleux :
-- Comptes frauduleusement vidés (cash-out).
-- Comptes "mules" utilisés temporairement pour recevoir/transférer des fonds avant d'être vidés.
-- Tentatives de transactions sur des comptes sans fonds.
C'est une caractéristique des données qu'il faudra corréler avec la présence de fraude (isFraud=1) pour voir si ces transactions sont plus risquées.

# III. Observations Critiques sur la Détection de Fraude (Le "Red Flag" Principal)

## Déséquilibre Extrême des Classes (isFraud) :
Constat : Sur plus de 4 millions de transactions :
- Seulement 3 397 sont des fraudes avérées (isFraud = 1).
- 4 057 077 sont des non-fraudes (isFraud = 0).
- Impact Audit : C'est un dataset très déséquilibré. Cela rend la détection de fraude intrinsèquement difficile. Un système qui ne ferait rien du tout aurait une précision (exactitude) de 99.9% mais serait totalement inefficace pour détecter la fraude.

## Performance Alarmante du Système de Détection Actuel (isFlaggedFraud) :
- Constat : Le système de détection de fraude simulé de la banque (isFlaggedFraud) n'a signalé que 3 transactions comme potentiellement frauduleuses sur l'ensemble du dataset.
- Impact Audit (MAJEUR !) : Étant donné qu'il y a 3 397 fraudes avérées (isFraud=1), cela signifie que le système de détection de la banque a manqué la quasi-totalité des vraies fraudes. C'est un taux de Faux Négatifs (fraudes non détectées) extrêmement élevé.
- Conclusion Initiale : Le système de détection de fraude de BankSecur est largement inefficace tel qu'il est configuré dans cette simulation. C'est l'observation la plus importante de notre analyse exploratoire et le point focal de notre audit.

# IV. Analyse des Cohérences des Soldes (Balance_Diff_Org et Balance_Diff_Dest) :
Les observations sur Balance_Diff_Org ([oldbalanceOrg]-[amount]-[newbalanceOrig]) et Balance_Diff_Dest([newbalanceDest]-([oldbalanceDest] + [amount])) sont extrêmement critiques et doivent figurer en bonne place dans votre rapport d'audit :

## Fiabilité des Données Compromise : 
Une majorité écrasante des transactions (environ 85% pour l'origine et 75% pour la destination) présentent des incohérences majeures dans les mises à jour de soldes. Cela indique des failles profondes dans la logique applicative ou la gestion des données des systèmes bancaires. Les soldes affichés aux clients et utilisés pour les rapports internes pourraient être massivement incorrects.
## Risque Opérationnel et Financier Élevé : 
Ces incohérences peuvent entraîner :
- Des erreurs comptables significatives.
- Des pertes financières non détectées (si l'argent "disparaît" via des soldes inférieurs aux attentes).
- Des problèmes de confiance client (en cas de relevés de compte incorrects).
- Des sanctions réglementaires (si les rapports financiers sont basés sur des données non fiables).
## Indicateur de Fraude Potentiel : 
Il est fortement probable que ces incohérences de solde soient utilisées ou générées par les mécanismes de fraude. Les fraudeurs pourraient exploiter ces failles pour manipuler les soldes, ou la fraude elle-même pourrait laisser ces "cicatrices" dans les calculs de solde. C'est un puissant levier d'investigation pour votre audit.


# V. Performance du Système de Détection de Fraude de BankSecur : Une Évaluation Critique

Basé sur votre analyse, la matrice de confusion pour le système actuel (isFlaggedFraud vs isFraud) est la suivante :

- Vrais Positifs (VP) : 14
C'est le nombre de fois où le système a correctement identifié une transaction comme étant une fraude.
- Faux Négatifs (FN) : 8 197
C'est le nombre de fois où le système a manqué une transaction qui était en réalité une fraude. Ces fraudes sont passées sous le radar.
- Faux Positifs (FP) : 0
C'est le nombre de fois où le système a incorrectement signalé une transaction non frauduleuse comme étant une fraude.
- Vrais Négatifs (VN) : 6 354 407
C'est le nombre de fois où le système a correctement identifié une transaction comme n'étant pas une fraude.

## Interprétation d'Auditeur : Le Verdict
Ces chiffres sont, du point de vue de l'audit, extrêmement préoccupants :

### Efficacité Catastrophique de la Détection (Faux Négatifs) :
Avec seulement 14 fraudes détectées (VP) sur un total de 8 211 vraies fraudes (14 VP + 8197 FN), le système actuel manque 8 197 fraudes. Cela représente un taux de détection de seulement (14 / 8211) * 100 = 0.17%. Autrement dit, le système ne détecte même pas 1% des fraudes réelles !
C'est une faille opérationnelle majeure. Chaque transaction frauduleuse manquée représente une perte financière potentielle pour la banque. Le risque est immense.

### Absence de Faux Positifs :
Le fait qu'il y ait 0 Faux Positif (FP = 0) signifie que le système ne génère aucun "faux signal". Si cela semble positif à première vue, c'est en fait le symptôme du problème : le système est tellement restrictif qu'il ne signale presque rien, et par conséquent, il ne rate presque rien (de non-fraude) mais ne détecte presque rien (de fraude) non plus. C'est un système "silencieux" parce qu'il ne fait pratiquement rien.

### Performance Inacceptable :
Le système de BankSecur, tel que simulé, est largement inefficace pour protéger l'organisation contre la fraude. Il offre une fausse impression de sécurité.
