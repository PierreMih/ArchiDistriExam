## db.jsonl

Ce fichier correspond à la base de données principale référençant les informations sur les joueurs.

Les champs sont les suivants:
- 'id': id du joueur (doit être unique)
- 'chat_messages': un tableau contenant les informations sur les messages du joueur
    - 'sentiment': le sentiment global du message (négatif vers 0, positif vers 1)
    - 'date': la date du message
- 'last_matches': un tableau contenant les informations sur les derniers matches du joueur
    - 'date': date du match
    - 'kills': Le nombre d'ennemis éliminés durant le match
    - 'deaths': Le nombre d'élimination durant le match
    - 'friendly_kills': Le nomre d'amis éliminés durant le match
    - 'time_in_movement_ration': Le ratio entre le temps à l'arrêt et en mouvement du joueur
    - 'shots_fired': Le nombre de munition tirées
    - 'flags_captured': Le nombre de drapeaux capturés
- 'level': le niveau actuel du joueur
- 'total_hours_played': le nombre d'heures durant lequel le joueur a été en ligne

## sales.jsonl

Ce fichier contient les informations de transations dans le jeu, c'est-à-dire les objets que le joueur a acheté

Les champs sont les suivants:
- 'user': l'id du joueur
- 'transactions': la liste des transactions
    - 'date': la date de l'opération
    - 'products': la liste des produits achetés
        - 'name': le nom de l'objet
        - 'description': la description de l'objet
        - 'price': le prix
        - 'discout': OPTIONNEL: le discount appliqué sur le prix du produit