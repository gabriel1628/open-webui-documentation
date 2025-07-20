# Guide de l'utilisateur Open WebUI

## Table des matières

<!-- TOC -->

- [Table des matières](#table-des-matières)
- [Introduction](#introduction)
- [Présentation de l'interface utilisateur](#présentation-de-linterface-utilisateur)
    - [Sections principales de l'interface](#sections-principales-de-linterface)
    - [Composants détaillés](#composants-détaillés)
        - [I. Barre latérale gauche (navigation et historique)](#i-barre-latérale-gauche-navigation-et-historique)
        - [II. Zone de discussion](#ii-zone-de-discussion)
        - [III. Menu utilisateur et paramètres](#iii-menu-utilisateur-et-paramètres)
- [Fonctionnalités du chat](#fonctionnalités-du-chat)
- [Paramètres du chat](#paramètres-du-chat)
- [Liste des modèles](#liste-des-modèles)
    - [Modèles de génération de texte](#modèles-de-génération-de-texte)
    - [Modèle de génération d'image](#modèle-de-génération-dimage)
    - [Modèle de reconnaissance vocale](#modèle-de-reconnaissance-vocale)
    - [Modèle de synthèse vocale](#modèle-de-synthèse-vocale)
- [Espace de travail](#espace-de-travail)
- [Paramètres utilisateur](#paramètres-utilisateur)
    - [Changer la langue](#changer-la-langue)
- [Conseils](#conseils)
    - [Évitez les conversations inutilement longues](#évitez-les-conversations-inutilement-longues)
    - [Choisissez le bon modèle](#choisissez-le-bon-modèle)
    - [Générez plusieurs réponses](#générez-plusieurs-réponses)
    - [Utilisez les prompts système](#utilisez-les-prompts-système)
    - [Ajustez la température](#ajustez-la-température)
    - [Recherche web](#recherche-web)
- [FAQ](#faq)

<!-- /TOC -->

## Introduction

Bienvenu sur notre plateforme d'IA basée sur **Open WebUI** !
<br>
Notre application vous permet de discuter avec les LLM (Large Language Model) les plus puissants du marché.
Considérez-la comme votre **chatbot personnel et privé**, similaire à des outils comme ChatGPT, mais avec des avantages clés tels que l'accès à une variété de modèles d'IA de pointe et le contrôle de leurs paramètres.

**Comment l'utiliser :**
Commencez simplement à taper vos questions ou vos instructions dans la zone de discussion.

> [!NOTE]
> * Bien que puissants, les modèles d'IA restent des outils. Vérifiez toujours les informations critiques fournies par l'IA, en particulier pour les tâches sensibles ou factuelles.
> * La date limite des connaissances de l'IA varie selon les modèles. Pour les informations les plus récentes, il est toujours préférable de consulter des sources actuelles.
> * Nous améliorerons et étendrons continuellement les capacités de cette plateforme. Votre avis est précieux !

Amusez-vous !


## Présentation de l'interface utilisateur

Voici un exemple de à quoi ressemble l'interface utilisateur :

![IU](./images/ui-light.png)

### Sections principales de l'interface

L'interface est divisée verticalement en trois sections principales :
1.  **Navigation et historique :** Sur la gauche, offrant la navigation et l'accès aux conversations passées.
2.  **Zone de discussion :** La grande zone centrale où la conversation avec l'IA a lieu.
3.  **Menu utilisateur et paramètres :** En haut à droite, contenant les actions spécifiques à l'utilisateur et les paramètres généraux de l'application.

### Composants détaillés

#### I. Barre latérale gauche (navigation et historique)

1.  **Menu hamburger (☰) :** Tout en haut à gauche, utilisée pour réduire ou étendre la barre latérale afin de gagner de l'espace sur l'écran.
3.  **Bouton « Nouvelle discussion » :** Un bouton proéminent pour lancer une nouvelle conversation, effaçant le contexte de la précédente.
5.  **Barre de recherche (🔎) :** Permet aux utilisateurs de rechercher dans leur historique de conversation.
6.  **Notes :** Une section pour gérer les notes de l'utilisateur, distinctes des conversations.
7.  **Espace de travail :** offre un environnement complet pour gérer vos interactions et configurations d'IA. Il se compose de trois composants clés : Modèles, Connaissances et Prompts. Consultez la section [Espace de travail](#espace-de-travail) pour plus de détails.
8.  **En-tête de section « Conversation » :** Une section pliable indiquant la liste des conversations enregistrées.
11. **Section profil utilisateur :**
    *   **Avatar/initiales de l'utilisateur (`TU` dans un cercle orange) :** Représente l'utilisateur connecté.
    *   **Nom d'utilisateur (« Test User ») :** Affiche le nom de l'utilisateur connecté.

#### II. Zone de discussion

1.  **Sélection du modèle/Affichage du modèle actuel :**
    *   **Nom du modèle :** Affiche le modèle d'IA actuellement sélectionné pour la conversation.
    *   **Flèche déroulante :** Indique qu'un clic sur celle-ci permet à l'utilisateur de sélectionner un autre modèle d'IA.
    *   **Texte « Définir comme valeur par défaut » :** Une option pour désigner le modèle actuellement sélectionné comme modèle par défaut pour les futures discussions.
4.  **Zone de saisie des messages :**
    *   **Zone de saisie de texte :** La zone où l'utilisateur tape ses messages. Elle contient le message de remplissage « Comment puis-je vous aider aujourd'hui ? » qui disparaîtrait lors de la saisie.
    *   **Bouton Pièces jointes/Options (+) :** En bas à gauche de la zone de saisie, ouvre les options pour joindre des fichiers (comme des images) ou accéder à des fonctionnalités de saisie plus avancées.
    *   **Bouton « Image » (Icône Image) :** Pour générer une image à partir du message de l'utilisateur.
    *   **Bouton « Interpreteur de code » :** Pour exécuter du code.
    *   **Icône Microphone (🎤︎︎) :** Pour la saisie vocale. Un modèle de reconnaissance vocale transcrira le message vocal de l'utilisateur et l'enverra au LLM. 
    *   **Icône Casque (🎧) :** Pour la conversation vocale. Cette option permet à l'utilisateur de converser oralement avec le modèle d'IA.
5.  **Suggestions de prompts :** Exemples de questions fournies par l'interface pour aider les utilisateurs à démarrer (par exemple, « Surmonter la procrastination », « Dites-moi un fait amusant », « Expliquer le trading d'options »).

#### III. Menu utilisateur et paramètres

1.  **Avatar/initiales de l'utilisateur (En haut à droite) :** un clic ouvre un menu déroulant avec les éléments suivants :
    *   **Paramètres (⚙️) :** Ouvre le panneau des paramètres généraux de l'application.
    *   **Conversations archivées :** Pour gérer les conversations qui ont été déplacées hors de la liste principale des discussions.
    *   **Playground :** Une zone dédiée à l'expérimentation avec les modèles d'IA, potentiellement avec des paramètres et des configurations plus avancés.
    <*   **Panneau d'administration :** Pour les contrôles administratifs.>
    *   **Documentation :** Liens vers la documentation officielle d'Open WebUI.
    *   **Releases :** Fournit des informations sur les versions logicielles et les mises à jour.
    *   **Raccourcis clavier :** Affiche une liste de raccourcis pour une navigation et une interaction plus rapides.
    *   **Déconnexion :** Pour se déconnecter de l'application.
2.  **Contrôles du chat :** Permet aux utilisateurs de modifier le prompt système et les paramètres avancés du modèle pour une instance de discussion spécifique. Nécessite un peu de connaissances sur les LLM.
3.  **Paramètres de la discussion (•••) :** N'apparaît qu'après le démarrage d'une conversation. Il permet à l'utilisateur de :
    * **Partager** la conversation.
    * Obtenir un **Aperçu** de la discussion et s'y déplacer facilement.
    * **Télécharger** la discussion dans différents formats.
    * **Copier** le contenu de la discussion.
    * Ajouter des balises (tags) à la discussion. Certaines balises sont automatiquement générées par un LLM lorsque la conversation commence.


## Fonctionnalités du chat

Voici une liste non exhaustive des fonctionnalités offertes dans le chat :
- Sélectionner un ou plusieurs modèles.
- Changer le modèle au sein de la même conversation.
- Cliquer sur le bouton **+** (Plus) en bas du champ de saisie de texte pour importer (**téléverser**) des fichiers et en discuter.
- Cliquer sur le bouton **+** (Plus) en bas du champ de saisie de texte pour prendre une capture (**prise de vue**) de votre écran, onglet ou fenêtre et en discuter.
- Cliquer sur **Image** sous le champ de saisie de texte pour générer une image à partir de votre prompt.
- Cliquer sur **Interpreteur de code** sous le champ de saisie de texte pour demander au modèle de générer et d'exécuter du code dans un environnement "sandbox".
- Cliquer sur l'icône de **microphone** en bas à droite du champ de saisie pour saisir votre prompt oralement. Un modèle de reconnaissance vocale transcrira votre saisie vocale (voir [Modèle de reconnaissance vocale](#modèle-de-reconnaissance-vocale)) et l'enverra au LLM.
- Cliquer sur l'icône de **casque** à droite de l'icône de microphone pour démarrer une conversation orale avec le modèle.
Voici comment cela fonctionne :
    - Un modèle de reconnaissance vocale transcrira votre saisie vocale (voir [Modèle de reconnaissance vocale](#modèle-de-reconnaissance-vocale)) ;
    - Le prompt transcrit est envoyé au LLM ;
    - Le LLM génère sa réponse ;
    - Un modèle de synthèse vocale lit à voix haute la réponse du LLM (voir [Modèle de synthèse vocale](#modèle-de-synthèse-vocale)).
- **Modifier** votre prompt en cliquant sur l'icône de modification sous votre message et générer une nouvelle réponse du LLM.
- **Modifier** la réponse du LLM en cliquant sur l'icône de modification sous le message.
- **Copier** votre prompt ou la réponse du modèle en cliquant sur l'icône de copie sous le message.
- **Lire à voix haute** la réponse du LLM en cliquant sur l'icône de haut-parleur sous le message.
- (Non recommandé) **Générer une image** à partir de la réponse du LLM en cliquant sur l'icône d'image sous son message. Il est recommandé de plutôt générer une image directement à partir de votre prompt.
- **Évaluer** la réponse du LLM en lui attribuant un pouce levé ou un pouce baissé.
- **Noter** la réponse du LLM sur une échelle de 1 à 10 et expliquer votre note par une courte phrase (facultatif).
- Prolonger la réponse du LLM en cliquant sur l'icône **lecture** (**Continuer la réponse**).
- **Regénérer** la réponse du LLM à l'aide de l'icône **recharger**. Vous pouvez changer le modèle avant de regénérer pour obtenir une réponse de ce LLM nouvellement sélectionné.
- Cliquer sur **Contrôles** en haut à droite de votre écran pour configurer le prompt système et les paramètres avancés du LLM (voir [Paramètres du chat](#paramètres-du-chat)).
- Une fois une conversation démarrée, vous pouvez cliquer sur les **trois points (•••)** en haut à droite de l'écran, à côté de Contrôles, pour :
    - **Partager** la conversation via une URL.
    - Obtenir un **aperçu** et naviguer facilement dans la conversation.
    - **Télécharger** la conversation dans différents formats (json, txt ou pdf).
    - **Copier** la conversation entière.
    - Ajouter des **tags** à la conversation ou les modifier.
- Vous pouvez également cliquer sur les **trois points (•••)** dans le panneau de gauche, à côté du titre de la conversation, pour **épingler**, **renommer** ou **archiver** la conversation, ainsi qu'accéder aux options mentionnées juste avant.


## Paramètres du chat


## Liste des modèles

### Modèles de génération de texte

Les modèles de génération de texte sont appelés grands modèles de langage ou plus couramment LLM pour Large Language Model.
Les LLM disponibles dans l'application sont listés dans le tableau ci-dessous.
La colonne **Type en entrée** indique le format accepté par le modèle, qui peut être texte, image, audio, vidéo, ou une combinaison des 4.
Par exemple, certains modèles n'acceptent que du texte en entrée, d'autres du texte et des images.
Donc si essayez de donner une image à un modèle qui n'accepte que du texte, vous recevrez une erreur.
Référez-vous au tableau pour savoir si le modèle que vous utilisez accepte le type de donnée que vous souhaitez lui envoyez.

**Remarque:** Lorsque vous utilisez la saisie ou la conversation vocale (voir [II. Zone de discussion](#ii-zone-de-discussion)), c'est un modèle à part qui se charge de transcrire votre message vocal en message écrit, vous pouvez donc utiliser ces fonctionnalités quel que soit le modèle que vous utilisez. En revanche, vous ne pouvez pas joindre un fichier audio si le modèle n'accepte pas les audios en entrée.

### Modèle de génération d'image

### Modèle de reconnaissance vocale

### Modèle de synthèse vocale


## Espace de travail


## Paramètres utilisateur

Vous pouvez accéder aux paramètres utilisateur en cliquant sur votre avatar/vos initiales en haut à droite ou en bas à gauche de l'écran, puis en sélectionnant **⚙️ Paramètres**.

### Changer la langue

Pour changer la langue, allez dans **Paramètres -> Général -> Langue** et sélectionnez votre langue préférée.


## Conseils

### Évitez les conversations inutilement longues

### Choisissez le bon modèle

### Générez plusieurs réponses

### Utilisez les prompts système

### Ajustez la température

### Recherche web


## FAQ

**Pourquoi ne puis-je pas ouvrir l'application dans mon navigateur?**
<br>
Essayez de supprimez les données de navigation, au moins depuis la dernière fois que vous avez réussi à vous connecter à l'application.