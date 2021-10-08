#td sql q1)
#select titre from livre
#q2)
#select nom from usager
#q3)
#select DISTINCT nom from usager
#q4)
#select titre from livre where annee < 1980
#q5)
#select titre from livre where titre like "%A%"
#q6)
#select isbn FROM emprunt where retour = "2020-01-01"
#q7)
#select nom from auteur order by nom asc
#q8)
#select nom from usager where cp = "75012" or cp = "75013"
#q9)
Select nom, adresse from usager where adresse Not "rue"
#q10)
Select titre from livre where annee / 4 or annee / 400
