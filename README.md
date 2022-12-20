# TP_Spring_Batch

Le paiement par carte bancaire n’induit pas le débit immédiat du compte.
La transaction ne sera validée qu’au début du mois suivant. Ainsi le
compte sera debité au debut de mois suivant.
Au moment du paiement par carte, la transaction est journalisée dans un
fichier csv.
Le fichier de journalisation csv contient les informations suivantes :
idTransaction,idCompte,montant,dateTransaction
1,1,2000,02/01/2015 23:15
2,2,1800,02/01/2015 13:15
3,3,1000,05/01/2015 09:35
4,4,3100,02/10/2015 00:15
dateTransaction est la date de transaction et non pas la date de débit
du compte.
Soit le diagramme de classes suivant :
Ecrire un batch qui permet, au debut de chaque mois, de lire à partir
du fichier csv des transactions, puis enregistrer les transactions dans
la base de données et débiter les comptes.
DateDebit est la date où le compte a été débité.
