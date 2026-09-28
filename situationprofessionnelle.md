# Situation professionnelle n°1 : Travaille à distance.

## Contexte
En octobre, dans la PME de métallurgie où je suis en alternance, il y a 45 poste. Deux des commerciaux font du télétravail 2 jours par semaines.

## Problématique
Les deux commerciaux ont besoins des devis pour travailler, mais comme il est impossible d'avoir accès aux données depuis l'extérieur de l'entreprise. La solution actuelle c'est qu'ils
s'envoyaient sur leurs propres boites mail les fichiers. L'inconvenant c'est que personne ne savaient quelle versions du fichier devis ils avaient, que les devis donné pouvaient étre éronné 
et un manque de sécurité en cas de piratage de leurs propre boites mail personnelles. Donc le responsable SI m'a donné un mois pour trouver une solution et dans un budget limité.

## Démarche
J'ai du réfléchir à une solution: trois possibilités sont apparu:
- Ouverture du bureau à distance sur internet en redirigent le port sur la box.
  avantage: c'est gratuit.
  inconvénient: après avoir reçu une alerte de CERT-FR, J'ai découvert qu'il y avait de grand probabilité de piratage de donner et qu'il a comme conséquence les voles de donnée sensible et
  importante. 
  Conclusion: cette solution a été mise de coter.

- Mettre tout les fichiers commerciaux sur un espace en ligne sur un espace chez un hébergeur.
  Il n'y a pas d'avantage à utilisé cette solution.
  Inconvénient: deux fois plus de charge de travail car il faut synchroniser les fichiers sur les deux systèmes et qu'il faudrait un abonnement par utilisateur donc à long termes le budget
   donner sera depassé.
  Conclusion: cette solution a été mise de coter.

- Mettre ne place un VPN sur le pare-feu de l'entreprise, sur les deux ordinateurs de l'entreprise qui pourront ce connecter au réseaux internet et travailler sur les fichiers d'orrigines.
  Avantages : Le prix de l'abonnement VPN est plus abordable et peu avoir plusieurs utilisateur sur une session, les fichiers mise à jours directement donc moins de risque sur des erreurs
  de devis et une meilleur sécurisation des données.
  Inconvénient: aucune.
  Conclusion: c'est cette solution que j'ai appliqué pour résoudre le probleme.

## Outils mobilisé
J'ai du utiliser le VPN pour créé un compte par utilisateurs sur leur ordinateur et les deux téléphones des commerciaux pour une doubles vérifications pour renforcer la securité.

## Résultat
Les deux commerciaux travailles directement sur les fichiers des devis d'origine, donc plus aucune copie n'est envoyer sur des adresses mail personnel donc il y a une meilleur sécurisation 
des fichiers. Comme je peux avoir accès aux paramètres du VPN j'ai pu voir les connections qui a eut: il y a eut 17 connections enregistré et aucune qui vient d'une adresse inconnu. Un 
temps d'ouverture des fichiers acceptable, 4 secondes depuis chez eux à 1 seconde en entreprise, et vu que on a utiliser le pare-feu car il gère le VPN, cela n'a rien couter à 
l'entreprise. 

## Bilan personnel
La première idée avait été pensé car c'était une solution que je connaissais déjà, et qui était la plus rapide à mettre en place. Mais par acquis de conscience j'ai été vérifier si il y avait des risques, et il en avait. Grace à cette situation j'ai compris l'importance de vérifié l'efficacité de la solutions pensée et pas seulement mettre directement en place la première solutions qui vient et de voir par la suite les éventuelle problèmes. Il me reste une limite que j'assume, je n'ai pas mis en place de sauvegarde de journaux du pare-feu, qui
s'écrase au bout de 30 jours, cela sera la prochaine étape des choses à traiter. 

