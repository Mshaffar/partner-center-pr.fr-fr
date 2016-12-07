---
title: "Créer plusieurs utilisateurs pour un compte client | Espace partenaires"
description: "Vous pouvez ajouter plusieurs utilisateurs en même temps au compte d’un client, en téléchargeant un fichier de données&nbsp;CSV dans l’Espace partenaires."
ms.assetid: c6fca2c0-2e6c-41b1-9be8-b363b139f15b
author: MaggiePucciEvans
translationtype: Human Translation
ms.sourcegitcommit: 14ba85c868e59dd1c77063f5b1b0e9ab8db7f82f
ms.openlocfilehash: d8aa280363bc654170c10ea0497a77bcd1e09e11

---

# Créer plusieurs utilisateurs pour un compte client


Vous pouvez ajouter plusieurs utilisateurs en même temps au compte d’un client, en téléchargeant un fichier de données&nbsp;CSV dans l’Espace partenaires. Vous pouvez télécharger un exemple de fichier de données à partir de l’Espace partenaires, puis l’adapter à votre utilisation, ou créer un fichier de données à l’aide du modèle de données défini ci-dessous.

## <a href="" id="creatingtheimportcsvfile"></a>Conditions requises pour les fichiers de données


Pour ajouter plusieurs utilisateurs au compte d’un client par chargement groupé, vous devez respecter les conditions suivantes&nbsp;:

-   Vous devez posséder des autorisations d’administrateur global sur le compte client.
-   Chaque utilisateur doit avoir une adresse de messagerie unique, ajoutée à un ou plusieurs domaines de messagerie du client.
-   Vous pouvez charger jusqu’à 100&nbsp;enregistrements à la fois. Si vous avez besoin d’ajouter plus de 100&nbsp;utilisateurs, créez et chargez des fichiers de données supplémentaires.
-   Tous les utilisateurs doivent se trouver dans le même **emplacement** géographique.
-   N’entrez que les données décrites ci-dessous. Les autres données bloqueront le chargement.

Entrez les données suivantes dans le fichier de données&nbsp;:

|                 |                                                                              |                                            |
|-----------------|------------------------------------------------------------------------------|--------------------------------------------|
| **Nom de la colonne** | **Description**                                                              | **Limitation**                             |
| Prénom      | Prénom de l’utilisateur (champ facultatif)                                           | 50&nbsp;caractères maximum                         |
| Nom       | Nom de l’utilisateur (champ facultatif)                                            | 50&nbsp;caractères maximum                         |
| Nom d’affichage    | Nom affiché dans l’Espace partenaires (champ obligatoire)                            | 50&nbsp;caractères maximum                         |
| Email           | Adresse de messagerie professionnelle de l’utilisateur chez le client (champ obligatoire)           | Chaque utilisateur doit avoir une adresse de messagerie unique. |
| Mise à jour de l’état   | Permet d’indiquer si le nouvel enregistrement d’utilisateur a été créé. | \*\*Laisser vide\* \ *                        |

 

### <a href="" id="createmultipleuseraccounts"></a>Pour créer plusieurs comptes d’utilisateur&nbsp;:

<a href="" id="creatingtheaccounts"></a>
1.  Créez un fichier de données&nbsp;CSV avec les données décrites ci-dessus. Enregistrez le fichier pour pouvoir le retrouver ultérieurement.
2.  Dans le menu **Tableau de bord**, sélectionnez **Clients**, puis choisissez un client dans la liste.
3.  Sélectionnez **Charger des utilisateurs**.
4.  Sous **Charger des informations d’utilisateur**, sélectionnez **Parcourir**.
5.  Dans le sélecteur de fichiers, sélectionnez votre fichier de données, puis **Ouvrir**.
6.  Sélectionnez **Valider**.

    **Remarque** La plupart des erreurs de création de compte sont provoquées par des problèmes de fichier de données, comme des informations manquantes, des adresses de messagerie incorrectes ou dupliquées, un trop grand nombre d’enregistrements dans le fichier.

     

7.  Lorsque l’Espace partenaires a validé le fichier, sélectionnez l’**emplacement** géographique des nouveaux utilisateurs.
8.  Sélectionnez **Enregistrer**.
9.  Téléchargez le mot de passe temporaire des utilisateurs.

**IMPORTANT&nbsp;:** n’oubliez pas de télécharger le fichier avec les mots de passe temporaires maintenant, car cette opération ne sera plus possible après. Les nouveaux utilisateurs doivent se connecter à leur nouveau compte à l’aide du mot de passe temporaire correspondant.

L’Espace partenaires attribue automatiquement les autorisations **Peut utiliser les licences et services** aux nouveaux utilisateurs.

 

 






<!--HONumber=Nov16_HO4-->

