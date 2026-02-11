Data Base : concepts de sites



**1. MOOCademy (plateforme de cours en ligne)**



table cours :

&nbsp;	id (INTEGER)

&nbsp;	titre (TEXT)

&nbsp;	description (TEXT)



table leçons :

&nbsp;	id (INTEGER)

&nbsp;	titre (TEXT)

&nbsp;	body (TEXT)

&nbsp;	*cours\_id (INTEGER)*





**2. The Hacking Pinterest (Images)**



table utilisateurs :

&nbsp;	id (INTEGER)

&nbsp;	



table pins :

&nbsp;	id (INTEGER)

&nbsp;	image (URL)

&nbsp;	*utilisateurs\_id*



table commentaires :

&nbsp;	id (INTEGER)

&nbsp;	body (TEXT)

&nbsp;	*pins\_id*

&nbsp;	*utilisateurs\_id*





**3. The Hacking News (Liens et débats)**



table utilisateurs :

&nbsp;	id (INTEGER)

&nbsp;	nom (TEXT)



table liens :

&nbsp;	id (INTEGER)

&nbsp;	liens (URL)

&nbsp;	*utilisateurs\_id*



table commentaires :

&nbsp;	id (INTEGER)

&nbsp;	body (TEXT)

&nbsp;	*utilisateurs\_id*

	*liens\_id*

	*commentaire\_parent\_id* (SI c'est une réponse à autre commentaire)





**4. The Hacking Class (Éducation)**



table élèves :

&nbsp;	id (INTEGER)

&nbsp;	nom (TEXT)

&nbsp;	prénom (TEXT)

&nbsp;	age (INTEGER)

&nbsp;	*cours\_id*



table cours :

&nbsp;	id (INTEGER)

&nbsp;	titre (TEXT)

&nbsp;	body (TEXT)



