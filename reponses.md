
## Partie 03

**Q3.2.** 
- (1) Si j'écris DatabaseHelper() deux fois, seul un objet est créé grâce au constructeur privé _interne(), à static final _instance et au actory qui retourne toujours la même instance. C'est le pattern singleton.
- (2) L'opérateur ??= assigne une valeur à _db seulement s'il est 
ull. Une fois la base ouverte, il n'est plus appelé.
- (3) PRAGMA foreign_keys = ON doit être dans onConfigure, car il doit être réactivé à chaque ouverture de la base et non uniquement à sa création.
- (4) onCreate n'est appelé qu'une seule fois, au moment où le fichier .db n'existe pas encore.

**Q3.5.** Non, onCreate ne s'affiche plus au second lancement. Le fichier existe déjà, donc openDatabase ouvre directement la base sans appeler onCreate.

**Q3.7.** (à vérifier sur mon écran) Les deux tables existent avec les mêmes colonnes que rouillon.db. La table categories contient les 4 catégories de départ, la table produits est vide. La valeur *User Version* est 1, ce qui correspond à ersionBase: 1.
