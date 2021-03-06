---
title: Utiliser des webhooks pour recevoir des événements de modification de ressource
ms.topic: article
ms.date: 05/08/2020
ms.service: partner-dashboard
ms.subservice: partnercenter-csp
description: Utiliser les API webhook pour déterminer quand des modifications de ressources de références sont effectuées
ms.assetid: c6fca2c0-2e6c-41b1-9be8-b363b139f15b
author: LauraBrenner
ms.author: labrenne
keywords: références, API webhook, événements de modification de ressource
ms.localizationpriority: medium
ms.openlocfilehash: a141776f1b591ebe41bb740051802b4b55cf36f0
ms.sourcegitcommit: 2a980b50cf177753c15ebfd7770e14cf6d486cf7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/22/2020
ms.locfileid: "83796205"
---
# <a name="use-webhook-apis-to-register-for-resource-change-events"></a>Utiliser les API webhook pour s’inscrire aux événements de changement de ressource

### <a name="appropriate-roles"></a>Rôles appropriés

- Administrateur des références
- Administrateur système ou personnalisateur de système pour Dynamics 365 CRM ou Salesforce CRM


Les API de webhook de l’espace partenaires vous permettent de vous inscrire aux événements de changement de ressource. Ces événements de modification sont envoyés à votre URL en tant que messages HTTP.

>[!NOTE]
>Cette rubrique explique les API webhook pour Dynamics 365 CRM et Salesforce CRM.

1. Pour inscrire votre URL, sélectionnez **inscription du webhook de l’espace partenaires (version préliminaire)** alimentation automatiser le Flow.

2. Ajouter des connexions pour (a.) Utilisateur de l’espace partenaires avec des références d’administrateur d’administration (b.) Événements de l’espace partenaires mis en surbrillance ci-dessous

![Déclencheur](images/cosellconnectors/triggerflow.png)

3. Lorsque vous effectuez ces mises à jour, vous verrez

![webhooks](images/cosellconnectors/webhook1.png)

4. Enregistrez vos modifications et sélectionnez **activer**. 

Pour activer les webhooks de l’espace partenaires afin d’écouter les modifications d’événement dans les objets d’adresse IP de covente ou de référence indépendante dans l’espace partenaires et les systèmes CRM, procédez comme suit :

5. Sélectionnez **espace partenaires pour Dynamics 365 (version préliminaire d’Insider)** ou **espace partenaires pour Salesforce (version préliminaire d’Insider)**.

6. Sélectionnez l’icône **modifier** et sélectionnez le **moment où une requête HTTP est reçue**.

7. Sélectionnez l’icône de **copie** pour copier l’URL http postale fournie.

![Copier l’URL](images/cosellconnectors/copyurl.png)

8. Maintenant, sélectionnez l’option inscription à un webhook de l’espace partenaires (version préliminaire d’Insider) et sélectionnez **exécuter**.

9. Vérifiez que la fenêtre « exécuter le workflow » s’affiche dans le volet de droite, puis cliquez sur **Continuer**.

10. Entrez les informations suivantes : 

    a. **Point de terminaison du déclencheur http**: URL copiée à partir de l’étape précédente

    b. **Événements à inscrire**: « création de références » et « référencement-mis à jour »

    c. **Remplacer les points de terminaison déclencheurs existants s'** ils sont présents : Oui (cette valeur remplace tous les points de terminaison existants).

Le webhook peut maintenant écouter les modifications (créer et mettre à jour des événements). 

11. Sélectionnez **exécuter** , puis sélectionnez **terminé.**

 ## <a name="customize-synchronization-steps"></a>Personnaliser les étapes de synchronisation

Lorsque les références de covente sont synchronisées entre l’espace partenaires et votre système CRM, les champs qui sont synchronisés sur le PC de l’espace partenaires sont répertoriés ici.

Souvent, les systèmes CRM sont hautement personnalisés. Vous pouvez personnaliser les flux Power automate. Suivez le Guide de mappage de champs et, si nécessaire, apportez les modifications appropriées dans les étapes des flux d’automate Power.  Les mappages de l’espace partenaires Microsoft aux CRM sont fournis, mais en fonction de votre environnement CRM, vous pouvez choisir de personnaliser davantage les champs.

Plusieurs étapes de chacun des flux d’automate d’alimentation peuvent être personnalisées en fonction de vos besoins. Voici quelques exemples de personnalisations disponibles :

1. Pour personnaliser les champs pour les événements de création ou de mise à jour dans l’espace partenaires pour la synchronisation de références CRM : 

    a. Sélectionnez espace partenaires pour Dynamics 365 (version préliminaire d’Insider) ou espace partenaires pour Salesforce (version préliminaire d’Insider).

    b. Sélectionnez **modifier** pour modifier/personnaliser le Flow automatiser l’alimentation.

    c. Sélectionnez **(étendue) synchroniser le prospect ou l’opportunité**.

2. Pour personnaliser les mappages de champs CRM (en fonction du Guide des mappages de champs) pour créer des événements, sélectionnez **s’il s’agit d’une nouvelle opportunité partagée, puis**. Sélectionnez la sous-étape **si oui** , puis développez **création d’une nouvelle opportunité dans le CRM**. Vous pouvez modifier les mappages dans cette section à l’aide du Guide de mappage de champs.

    d. Pour personnaliser les mappages de champs CRM (en fonction du Guide des mappages de champs) pour les événements de mise à jour, cliquez sur l’étape « (étendue) synchroniser le prospect ou l’opportunité ».

    e. Sélectionnez **s’il s’agit d’une mise à jour d’une opportunité, puis**. Sélectionnez la sous-étape **si oui** , puis développez **si la différence entre les objets d’opportunité dans l’espace partenaires et CRM est déplacée**.  

    f. Sélectionner **si oui** suivi de **mettre à jour l’opportunité existante**
       
3. Pour personnaliser les champs pour la synchronisation des références de CRM à PC pour les événements de mise à jour :

    a. Sélectionnez **modifier** pour modifier/personnaliser le Flow automatiser l’alimentation.

    b. Sélectionnez **(étendue) synchroniser l’opportunité**.

    c. Pour personnaliser les mappages de champs CRM (en fonction du Guide des mappages de champs) pour les événements de mise à jour, sélectionnez **s’il existe une différence entre les objets de Prospect dans l’espace partenaires et CRM, puis**. 

    d. Sélectionnez la sous-étape **si oui** , puis développez l’étape **mettre à jour une référence avec les données d’opportunité**.

Vous pouvez modifier les mappages dans cette section en fonction du Guide de mappage de champs.

4. Pour personnaliser les champs de la synchronisation de référence de CRM à PC pour les événements de création ?

   a. Sélectionnez **modifier** pour modifier/personnaliser le Flow automatiser l’alimentation.

   b. Sélectionnez **(étendue) synchronisation des références.**

   c. Pour personnaliser les mappages de champs CRM (en fonction du Guide des mappages de champs) pour créer des événements, sélectionnez **créer une référence Microsoft**. 

Vous pouvez modifier les mappages dans cette section en fonction du Guide de mappage de champs.

## <a name="end-to-end-bi-directional-co-sell-referral-synchronization"></a>Synchronisation bidirectionnelle de la direction de la co-vente de bout en bout

Une fois que vous avez installé, configuré et personnalisé la solution Power automate, vous pouvez tester la synchronisation des références de covente entre Dynamics 365 ou Salesforce et l’espace partenaires.

### <a name="pre-requisites"></a>Conditions préalables

Pour synchroniser les références entre l’espace partenaires et Dynamics 365 CRM ou entre l’espace partenaires et le CRM Salesforce, la solution Power automate doit clairement délimiter les champs de référence propres à Microsoft. Cela permet à vos équipes de vendeur de décider quelles références elles souhaitent partager avec Microsoft pour la covente.

Un ensemble de champs personnalisés est disponible dans le cadre de la synchronisation des références de l’espace partenaires pour l’entité **opportunité** de solution Dynamics 365. Un utilisateur administrateur CRM devra créer une section CRM distincte avec les champs personnalisés d' **opportunité** .

Les champs personnalisés suivants doivent faire partie de la section CRM :

- **Synchroniser avec l’espace partenaires**: s’il faut synchroniser l’opportunité avec l’espace partenaires Microsoft

- **Identificateur de référence**: champ d’identificateur en lecture seule pour la référence de l’espace partenaires Microsoft

- **Lien de référence**: lien en lecture seule vers la référence dans l’espace partenaires Microsoft

- **Comment Microsoft peut**-il vous aider ?: aide requise de Microsoft pour la référence

- **Produits**: liste des produits associés à cette opportunité

- **Audit**: piste d’audit en lecture seule pour la synchronisation avec les références de l’espace partenaires

### <a name="scenarios"></a>SCÉNARIO

1. Synchronisation de la référence lorsque la référence est créée ou mise à jour dans CRM et synchronisée dans l’espace partenaires :

    a. Connectez-vous à votre environnement CRM Dynamics 365 ou à l’environnement CRM Salesforce avec un utilisateur qui dispose de la visibilité dans la section **opportunité** de CRM.

    b. Assurez-vous que la section suivante est présente lorsque vous créez une « nouvelle opportunité » dans l’environnement Dynamics 365

   ![Opportunité](images/cosellconnectors/opportunity.png)

    c. Pour synchroniser cette opportunité avec l’espace partenaires Microsoft, veillez à définir les champs suivants dans la vue de la carte :

    - « Synchroniser avec l’espace partenaires » : Oui

    - « Comment Microsoft peut-il m’aider ? » : sélectionnez l’une des options suivantes :

    ![Sélections d’aide](images/cosellconnectors/help.png)

    - Produits : ID de solution du produit

    d. Une fois que l’opportunité est créée dans Dynamics 365 avec l’option **sync with Partner Center** définie sur **Oui**, patientez 10 minutes, connectez-vous à votre compte espace partenaires. Vos références seront synchronisées avec Dynamics 365.

    e. Par conséquent, pour une opportunité avec l’option « synchroniser avec l’espace partenaires » définie sur « Oui », si vous mettez à jour l’opportunité dans Dynamics 365 CRM, les modifications sont synchronisées dans votre compte espace partenaires.

    f. Les opportunités qui sont synchronisées avec succès avec l’espace partenaires sont identifiées avec l’icône ✔ dans Dynamics 365.

2. Synchronisation de la référence lorsque la référence est créée ou mise à jour dans l’espace partenaires Microsoft et synchronisée dans l’environnement Dynamics 365 : 

    a. Connectez-vous à votre [tableau de bord](https://partner.microsoft.com/dashboard/home)de l’espace partenaires.

    b. Dans le menu de gauche, sélectionnez **références** .

    c. Pour créer une nouvelle référence de covente à partir de l’espace partenaires, cliquez sur l’option « nouvelle offre ».

    d. Connectez-vous à votre environnement Dynamics 365 CRM. 

    e. Accédez à **opportunités ouvertes**. La référence créée dans l’espace partenaires Microsoft est maintenant synchronisée dans Dynamics 365 CRM.

    f. Lorsque vous sélectionnez une référence synchronisée, les détails de l’affichage de la carte sont remplis.

 ### <a name="next-steps"></a>Étapes suivantes

- [En savoir plus sur la plateforme Microsoft Power Automated ?](https://docs.microsoft.com/power-automate/)

- [Événements du webhook de l’espace partenaires](https://docs.microsoft.com/partner-center/develop/partner-center-webhook-events)

- [Gérer les prospects](manage-leads.md)

- [Gérer les opportunités de covente](manage-co-sell-opportunities.md)
