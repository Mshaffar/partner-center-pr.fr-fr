---
title: Acheter des offres de la place de marché commercial
ms.topic: article
ms.date: 05/05/2020
ms.service: partner-dashboard
ms.subservice: partnercenter-csp
description: Découvrez comment les partenaires du programme CSP peuvent utiliser le Marketplace de l’espace partenaires pour permettre aux clients d’acheter des offres SaaS auprès d’éditeurs de logiciels indépendants.
author: LauraBrenner
ms.author: labrenne
keywords: abonnements, Marketplace, Marketplace commerciale, tiers, ISV, offres SaaS, programme de fournisseur de solutions Cloud, acheter une offre, acheter un abonnement
ms.localizationpriority: medium
ms.custom: SEOMAY.20
ms.openlocfilehash: c740ae823670644cb1f81c0a667d1fb48fc873ae
ms.sourcegitcommit: e9b627159745bcce53a8c2b1676f63f5249bba76
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2020
ms.locfileid: "82908080"
---
# <a name="purchase-commercial-marketplace-products-for-your-customers-in-partner-center"></a>Acheter des produits de la place de marché commercial pour vos clients dans l’espace partenaires

**S’applique à**

- Espace partenaires
- Partenaires du programme Fournisseur de solutions Microsoft Cloud

**Rôles appropriés**

- Administrateur général
- Agent d’administration

En tant que partenaire dans le programme du fournisseur de solutions Cloud (CSP), vous pouvez utiliser le Marketplace commercial pour acheter des abonnements pour vos clients à certains produits SaaS (Software as a service) proposés par des éditeurs de logiciels indépendants (ISV). 

En proposant des abonnements SaaS ISV à vos clients, vous pouvez contribuer à la différenciation de votre entreprise. Vous pouvez également permettre aux clients d’accéder aux offres logicielles qui répondent à leurs besoins professionnels spécifiques. Vous gérez les licences et les abonnements pour ces produits SaaS de la place de marché à partir d’éditeurs ISV, tout comme vous gérez les licences et les abonnements pour les produits Microsoft.

Vous pouvez acheter des abonnements Saas **basés sur une licence** ou des abonnements **basés sur l’utilisation** . Pour en savoir plus sur la différence entre la facturation basée sur une licence et la facturation basée sur l’utilisation, consultez [principes de base](billing-basics.md)de la facturation.

## <a name="purchase-license-based-saas-subscriptions-in-partner-center"></a>Acheter des abonnements SaaS basés sur une licence dans l’espace partenaires

Vous achetez des abonnements pour les produits SaaS basés sur des licences proposés par les éditeurs ISV en utilisant le même processus que celui utilisé pour acheter des abonnements pour les produits Microsoft.

Pour acheter un abonnement SaaS basé sur une licence dans l’espace partenaires, consultez [créer, suspendre ou annuler des abonnements clients](create-a-new-subscription.md#create-a-new-subscription).

Vous pouvez également utiliser les [API de l’Espace partenaires](https://docs.microsoft.com/partner-center/develop/) pour créer des abonnements de la place de marché commerciale pour vos clients. (Pour plus d’informations sur l’utilisation des API de l’espace partenaires, consultez [créer un abonnement pour les produits de la place de marché commercial](https://docs.microsoft.com/partner-center/develop/create-subscription-azure-marketplace-products).)

>[!IMPORTANT]
> En tant que partenaire dans le programme CSP, vous pouvez uniquement acheter des abonnements Saas **basés sur une licence** auprès d’éditeurs ISV au sein de l’espace partenaires. Cela signifie que vous pouvez acheter une offre SaaS basée sur une **licence** que l’éditeur ISV met à votre disposition, y compris les [offres exclusives](csp-commercial-marketplace-discover.md#learn-about-marketplace-exclusive-offers) auxquelles vous avez accès. Pour acheter ou gérer d’autres offres de la place de marché commercial auprès d’éditeurs de logiciels (ISV) (telles que des offres basées sur l’utilisation, limitées ou basées sur **l’utilisation**impliquant des applications, des conteneurs ou des machines virtuelles Azure), vous devez accéder au [portail Azure](https://portal.azure.com/). Pour plus d’informations, consultez la rubrique suivante.

## <a name="purchase-usage-based-subscriptions-in-the-azure-portal"></a>Achetez des abonnements basés sur l’utilisation dans le Portail Azure

Contrairement aux abonnements SaaS basés sur des licences provenant d’éditeurs ISV tiers, les abonnements basés sur l’utilisation requièrent d’abord qu’un client dispose d’un abonnement Azure. Facturation de la place de marché commercial, les ressources basées sur l’utilisation s’inscrivent dans le cadre de l’abonnement Azure du client. Une fois que votre client dispose d’un abonnement Azure, un partenaire dans le programme CSP peut effectuer les étapes suivantes pour acheter un abonnement au marché commercial pour eux :

1. Connectez-vous au [tableau de bord](https://partner.microsoft.com/dashboard)de l’espace partenaires, puis sélectionnez **clients** dans le menu de gauche.

2. Sélectionnez le client spécifique, puis sélectionnez **abonnements**.  

3. Sous les **abonnements basés sur l’utilisation**, sélectionnez **toutes les ressources**. Vous accédez au portail de gestion Azure.

4. Dans le portail de gestion Azure, sélectionnez **créer une ressource** dans le menu de gauche.

5. Sélectionnez **Afficher tout** en haut de la liste de la place de marché Azure.

6. Pour affiner votre liste, utilisez des filtres en haut de la liste de la place de marché. Par exemple, vous pouvez sélectionner **Microsoft** ou **partenaire** dans la liste déroulante **éditeur** pour afficher uniquement les offres de Microsoft ou celles d’un éditeur ISV.

7. Choisissez une offre spécifique, puis sélectionnez **créer**.

## <a name="next-steps"></a>Étapes suivantes

- [Gérer les offres de la place de marché commercial](csp-commercial-marketplace-purchase.md)