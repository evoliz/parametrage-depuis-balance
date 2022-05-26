# Notice d'utilisation v0.10

**"Donnez-nous une balance et nous vous fournirons les paramétrages minimaux pour fonctionner sur Evoliz"**

## Introduction

Ce fichier Excel « EvolizBalance » intègre une macro pour automatiser les paramétrages "Comptabilité" et "Gestion" **lors de la création du dossier** dans Evoliz.

Comptabilité : 
- Comptes comptables

Gestion : 
- Classification de ventes
- Classification d'achats 
- Affectations d'entrées
- Affectations diverses de sorties

![image (1)](https://user-images.githubusercontent.com/100150647/167125348-4e454ece-4cad-454f-accd-09689ab93277.png)

Cette macro génère automatiquement des fichiers sous format Excel (au gabarit Evoliz) qui seront ensuite à importer dans Evoliz. 

Une fois ces imports réalisés, le client et le cabinet disposeront dans Evoliz de classifications de ventes, achats et affectations de sorties et d'entrées correctement mappées (affectées) avec le compte comptable de l'outil de production.

## Informations techniques

Ce fichier comporte plusieurs onglets.

| Onglet    | Description |
| --------- | ------------- |
| Info      | Paramétrage des données : Code, Répertoires de sortie, Intégration du compte de tva sur les achats, Détermination des comptes de tva (Compte de tva sur les immobilisations, Compte de tva sur les ABS) |
| PCClient  | Intégration de la balance du client issue de l'outil de production  |
| Param     | Plan comptable et paramétrage "type" permettant de proposer les paramétrages spécifiques au client par comparaison avec sa balance (PC Client)  |


## Descriptif des onglets

### 1 – Info

Cet onglet reprend par ordre chronologique les étapes à suivre pour utiliser la matrice. 

#### Etape 1

Intégration de la balance n-1 du client afin de reprendre les comptes comptables utilisés pour cette société. Il est fortement déconseillé d'utiliser le plan comptable du dossier. La multitude des comptes comptables engendre la confusion pour l'utilisateur final. Celui-ci aura un choix important de comptes qui ne seront pas mouvementés et inutilisés dans l'outil de production.  

#### Etape 2

Possibilité de faire les choix suivant :


a. Le nommage dans Evoliz des classifications et d'affectations


| Choix    | Libellé dans Evoliz | Exemple de libellé dans Evoliz |
| --------- | ------------- | ------------- |
| 1  | Libellé+Code | Ventes de marchandises-707000 |
| 2  | Code+Libellé | 707000-Ventes de marchandises |
| 3  | Code | 707000 |

Exemple de restitution dans Evoliz

![Image1](https://user-images.githubusercontent.com/100150647/167127352-e3645d36-84e4-42da-8c64-091814f2b53b.png)

b. Choix de l'emplacement où vous souhaitez que les fichiers soient disponibles

Pensez à indiquer "\\" à la fin (Exemple : C:\Users\nom\Documents\EXPORT MACRO\\)

c. Choix d'indiquer un compte comptable de TVA sur les achats : "Oui" ou "Non"

d. Longueur des comptes de TVA : indiquer le nombre de chiffre par défaut des comptes comptables du client

e. Paramétrage des comptes de TVA applicable aux catégories d'achats

![Image2](https://user-images.githubusercontent.com/100150647/167127921-2d638ffd-3fcd-46d0-bd5e-751d730f2cdb.png)

Ce tableau fait une correspondance entre le plan comptable type (onglet Param) et des comptes comptables de TVA sur les achats. 

Il est possible d'enrichir le plan comptable type en saisissant dans l'onglet "Param" le type de TVA souhaité dans la colonne C compte TVA. 

Exemple : 

![Image3](https://user-images.githubusercontent.com/100150647/167128049-882c0993-0eaa-484e-b6f0-f3d01b2a6a6b.png)

Dans le journal d'achat, le compte de TVA pour les comptes 62. sera le 445661. 

Sauf si une ligne est ajoutée, par exemple pour les comptes 621., et indiquant un autre type/compte de TVA. Dans ce cas de figure tous les comptes 62 sauf les 621 auront un compte de tva 445661.

#### Etape 3

Cliquer sur le bouton : "C'est parti !"

Les fichiers sont générés dans le répertoire indiqué à l'étape 2) b). Ils peuvent être intégrés dans Evoliz.


## 2 – PCClient

Dans cet onglet PCClient vous devez intégrer dans la colonne A et B les comptes comptables et les libellés de la balance du dernier exercice clos. 

Cela permet de prendre en compte uniquement les comptes mouvementés et d'éviter d'intégrer des comptes inutilement. 


## 3 – Param

Cet onglet est généralement non modifié par l'utilisateur car il regroupe l'ensemble des informations permettant le fonctionnement de la macro. 

A la marge, certaines informations peuvent y être modifiées par les utilisateurs chevronnés.


# Utilisation de la macro

## Etape 1

Exporter depuis votre outil de production la dernière balance du dernier exercice clos sous Excel. Sélectionner les deux colonnes où figurent le numéro du compte comptable et le libellé. 

Copier et coller les valeurs de ces deux colonnes dans le fichier EvolizBalance dans l'onglet PCClient colonne A et B


## Etape 2

Onglet Info dans les cases bleues : 

a. Sélectionner dans la liste déroulante le code 1, 2 ou 3

b. Indiquer le répertoire de sorties des fichiers et mettre \ à la fin 

c. Sélectionner dans la liste déroulante : Oui (si les achats comportent de la TVA) ou Non (si les achats ne comportent pas de TVA)

d. Indiquer la longueur des comptes exemple : (6 à 11)

e. Valider ou indiquer les comptes de tva sur Achats souhaités pour chaque type d'achat


## Etape 3

Cliquez sur le bouton suivant


Les fichiers sont générés dans le répertoire indiqué à l'étape 2) b).

![Image4](https://user-images.githubusercontent.com/100150647/167128438-c4027ad9-c620-4d38-b4d7-6a1e04d8d3e7.png)


# Import dans Evoliz

## Etape 1 (optionnel)

Remise à zéro préalablement des catégories à importer. 

Paramètres > Remise à Zéro >  cocher les cases suivantes Comptes comptables, Classifications de ventes,  Classifications d'achats,  Affectations d'entrées et Affectations diverses sorties, taux de TVA

Renseigner le motif de la réinitialisation du compte dans la liste déroulante >  les donnés proposées par défaut ne correspondant pas à mon activité > Indiquer un commentaire "ok" et cliquer sur Réinitialiser le compte > cliquer sur ok 


## Etape 2

Les fichiers peuvent être importés.

### Si vous avez opté pour la remise à zéro

- Paramètres > Comptabilité > Comptes comptables > Sélectionner le fichier à importer > **PCG** > charger les données > Vérifier les données > Importer les données 
- Paramètres > Gestion > Taux de TVA > cliquer sur +Nouveau > Sélectionnez dans la liste déroulante le taux de TVA utilisé par le client sur **les ventes** et affecté le compte comptable de TVA > Enregistrer (renouveler l'opération si plusieurs taux de TVA) 
- Paramètres > Gestion > Classifications de ventes > Sélectionner le fichier à importer > **vente** > charger les données > Vérifier les données > Importer les données 
- Paramètres > Gestion > Classification d'achats > Sélectionner le fichier à importer > **achat** > charger les données > Vérifier les données > Importer les données 
- Paramètres > Gestion > Affectations d'entrées > Sélectionner le fichier à importer > **entrée** > charger les données > Vérifier les données > Importer les données 
- Paramètres > Gestion > Affectations diverses sorties > Sélectionner le fichier à importer > **sortie** > charger les données > Vérifier les données > Importer les données 


### Si vous n'avez pas opté pour la remise à zéro

Avant de réaliser l'import, il est nécessaire de remettre à zéro les listes par défaut. Sélectionner tous les codes (sélection multiple en cochant la case dans la ligne en tête) cliquer sur supprimer.

Ensuite réaliser les imports comme indiqué ci-dessus sauf pour les taux de TVA. 

- Pour les taux de TVA **utilisé** sur les ventes dans le cadre de l'activité de votre client : Paramètres > Gestion > Taux de TVA > cliquer sur taux de TVA > Affecté le compte comptable de tva > Enregistrer (renouveler l'opération si plusieurs taux de TVA)
- Pour les taux de tva **non utilisé** sur les ventes dans le cadre de l'activité de votre client : Paramètres > Gestion > Taux de TVA > supprimer les taux non utilisés par l'activité du client > Sélectionner le taux et cliquer sur supprimer
