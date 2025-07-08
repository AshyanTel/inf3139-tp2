# INF3190 – Introduction à la programmation web
## TP2 – Été 2025

Ce travail peut être fait individuellement ou en équipe de 2 personnes. Aucun retard ne sera toléré.
Un travail remis en retard recevra la note de 0.

### Soumissions d'assurance auto
Vous devez faire une application web qui effectuera une série de soumissions simplifiées d'assurance automobile. Le logiciel demandera quelques questions à l'utilisateur et calculera un montant d'assurance en fonction des réponses fournies par l'utilisateur. Il est possible qu'un utilisateur soit trop risqué pour notre compagnie d'assurance, si le programme détecte un cas similaire, il affiche à l'utilisateur «Désolé, nous n'avons aucun produit à offrir pour ce profil de client.» et l'analyse se termine. À la fin d'une soumission, le logiciel propose de faire une nouvelle soumission.

#### _Voici les questions à poser, exactement dans cet ordre :_

- [ ] Quel est votre genre `var genre` ?
- [ ] Quel est votre date de naissance `var birt_date`?
- [ ] Quelle est la valeur d'achat de votre véhicule `var vehicle_cost` ?
- [ ] Quelle est l'année de fabrication de votre véhicule `var  vehicle_date` ?
- [ ] Combien de kilomètres parcourez-vous par année `var millage`?
- [ ] Est-ce que votre véhicule possède une caméra de recul `var have_back_cam`?
- [ ] Avez-vous fait des réclamations d'assurance auto dans les 6 dernières années? (oui/non) `var have_reclam`
 Si oui, on demande les questions suivantes `var num_reclam` :
   - [ ] Combien de réclamations avez-vous faites?
   Ensuite, pour chaque réclamation, on demande (remplacer x par le numéro) :
      - [ ] Pour la réclamation `#x`, quel montant avez-vous réclamé? `var total_reclam`

#### _Voici les cas qui ne sont pas assurés :_

- [ ]  Les femmes de moins de 16 ans.
- [ ]  Les hommes de moins de 18 ans.
- [ ]  Une personne non-binaire de moins de 18 ans.
- [ ]  Les personnes de 100 ans ou plus.
- [ ]  Un véhicule de plus de 25 ans.
- [ ]  Un véhicule de plus de 100 000$ à l'achat.
- [ ]  Une personne avec plus de 4 réclamations.
- [ ]  Une personne avec plus de 35 000$ de réclamation.
- [ ]  Une personne qui parcourt plus de 50000 km par année.
- [ ]  Un véhicule qui n'a pas de caméra de recul.

#### _Voici un tableau représentant la logique de calcul du montant de base :_

| Règles | Montant de base|
|:------:|:--------------:|
|Pour les hommes et personnes non-binaires <br> de moins de 25 ans|**5%** de la valeur d'achat du véhicule|
| Pour les personnes de 75 ans ou plus | **4%** de la valeur d'achat du véhicule |
| Pour toutes les autres personnes | **1.5%** de la valeur d'achat du véhicule |

#### _La formule pour calculer le montant de l'assurance :_

$$\text{Assurance Annuelle} = \text{Montant de base} + 350 \times \text{Nombre de Réclamations} + 0.02 \times \text{kilométrage annuel}$$

On ajoute à ce montant une pénalité de **700\$** si la personne a plus de **25 000\$** de réclamation.
Une fois les données saisies et les calculs complétés, on affiche à l'utilisateur le prix annuel de la soumission d'assurance, ainsi que le montant d'une prime mensuelle.
### Validations
Une validation doit être faite pour chaque entrée de données. Si la donnée fournie est invalide, le programme doit afficher un message d'erreur indiquant le format attendu. La validation doit être faite en Javascript. La validation d'un champ en particulier doit être déclenchée par le changement de la valeur du champ.
La validation ne doit pas être effectuée une fois à la fin du processus, mais bien au fur et à mesure que l'utilisateur entre des données dans chaque champ.
La date de naissance doit être une date valide du calendrier.
### Divulgation progressive
La divulgation progressive consiste à n'afficher certaines questions que lorsque nécessaire. Les questions sur le nombre de réclamations et le montant des réclamations ne doivent pas s'afficher du tout si les questions n'ont pas à être répondues.
### Code source
#### _Le code source doit respecter les exigences suivantes :_
- [ ] Le projet ne contient que les technologies suivantes : `HTML`, `CSS`, `Javascript`. Aucun *backend* n'est présent.
- [ ]  Le `CSS` doit être dans un (ou plusieurs) fichier séparé;
- [ ]  Aucune librairie ou `framework` n'est permis;
- [ ]  Le code doit être indenté correctement.
- [ ] Les noms d'éléments, classes, identifiants, propriétés `CSS` doivent être en minuscules;
- [ ] Les fichiers sources doivent être encodés en `utf-8`;
- [ ]  il est permis d'utiliser un *template* `CSS` pour la présentation, dans la mesure où vous en respectez la licence.
#### Compatibilité
Le travail doit être utilisable et présentable sur **Chrome et Firefox**. Le design du site web doit être construit de façon à être fonctionnel et esthétique sur un ordinateur de bureau ou sur une tablette en mode paysage.
#### Ce que vous devez me remettre
Le site web doit être compressé dans un fichier `.zip` et remis par ***Moodle***. Le nom du fichier `.zip` doit contenir le code permanent des auteurs.
Vous serez pénalisé si vous ne respectez pas ces exigences.
Une seule remise par équipe.
#### Pondération
Respect des exigences : 60%
Convivialité du site web : 15%
Qualité du code : 15%
Aspect visuel du site : 10%