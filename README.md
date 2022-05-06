# Notice d'utilisation
"Donnez-nous une balance et nous vous fournirons les paramétrages minimaux pour fonctionner sur Evoliz"

## Introduction

Ce fichier Excel « EvolizBalance » intègre une macro pour automatiser les paramétrages "Comptabilité" et "Gestion"  lors de la création du dossier dans Evoliz.

Comptabilité : 
- Comptes comptables

Gestion : 
- Classification de ventes
- Classification d'achats 
- Affectations d'entrées
- Affectations diverses de sorties

![image](https://user-images.githubusercontent.com/100150647/167120167-ac85a91b-d69d-48ef-b680-65789373eda9.png)

Cette macro génère automatiquement des fichiers sous format Excel (au gabarit Evoliz) qui seront ensuite à importer dans Evoliz. 

Une fois ces imports réalisés, le client et le cabinet disposeront dans Evoliz de classifications de ventes, achats et affectations de sorties et d’entrées correctement mappées (affectées) avec le compte comptable de l’outil de production.

## Informations techniques

Ce fichier comporte plusieurs onglets.

| Onglet    | Description |
| --------- | ------------- |
| Note      | Paramétrage des données : Code, Répertoires de sortie, Intégration du compte de tva sur les achats, Détermination des comptes de tva (Compte de tva sur les immobilisations, Compte de tva sur les ABS) |
| PCClient  | Intégration de la balance du client issue de l’outil de production  |
| Param     | Plan comptable et paramétrage "type" permettant de proposer les paramétrages spécifiques au client par comparaison avec sa balance (PC Client)  |


## Descriptif des onglets

### 1 – Notes

Cet onglet reprend par ordre chronologique les étapes à suivre pour utiliser la matrice. 

**Etape 1**

Intégration de la balance n-1 du client afin de reprendre les comptes comptables utilisés pour cette société. Il est fortement déconseillé d’utiliser le plan comptable du dossier. La multitude des comptes comptables engendre la confusion pour l’utilisateur final. Celui-ci aura un choix important de comptes qui ne seront pas mouvementés et inutilisés dans l’outil de production.  

**Etape 2**

Possibilité de faire les choix suivant :













































