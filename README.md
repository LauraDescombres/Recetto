# RECETTO EXPLICATION
petit site pour compiler les recettes de ma famille

# STACK TECHNIQUE

php, vue.js, bootstrap, docker

# SCHEMA BDD

**table recette**
	id_recette *INT* (clé primaire) => id de la recette
	titre *VARCHAR* => titre de la recette
	description *TEXT* => description de la recette
	ingredients *TEXT* => ingrédients utilisés pour la recette
	instructions *TEXT* => etape à realiser pour la recette
	date_creation *DATETIME* => date de poste de la recette
	id_categorie *INT* (clé étrangère) => categorie de la recette
	id_utilisateur *INT* (clé étrangère) => id de l'utilisateur qui a posté la recette

**table categorie**
	id_categorie *INT* (clé primaire) => id de la categorie
	label *VARCHAR* => nom de la catégorie (entrée, dessert, plat)

**table utilisateur**
	id_utilisateur *INT* (clé primaire) => id de l'utilisateur
	nom_utilisateur *VARCHAR* => nom de l'utilisateur
	mot_de_passe *VARCHAR* => mot de passe sécurisée de l'utilisateur (hash et sel)
	email *VARCHAR* => email de l'utilisateur
	date_inscription *DATETIME* => date d'inscription de l'utilisateur