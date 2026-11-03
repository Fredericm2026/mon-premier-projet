# FreddyNova Studio — mon-premier-projet

Ce dépôt contient un site vitrine en français présentant FreddyNova Studio, ses services et une sélection de réalisations. Il comprend cinq pages HTML reliées par une navigation commune et une mise en forme CSS.

## Technologies utilisées

- **HTML5** : contenu des pages, liens de navigation et formulaire de contact.
- **CSS** : mise en page avec Flexbox et Grid, couleurs, dégradés, transitions et effets de flou.
- **Polices système** : aucune police externe à télécharger.

Le dépôt ne contient aucun JavaScript, framework, serveur applicatif ou accès à une base de données. React, Tailwind CSS et Supabase sont cités dans la présentation des services, mais ne sont pas intégrés au code de ce site.

## Structure des fichiers

```text
mon-premier-projet/
├── index.html       # Accueil et liens vers le portfolio et le contact
├── a-propos.html    # Présentation du studio
├── services.html    # Présentation des services
├── portfolio.html   # Présentation de trois réalisations
├── contact.html     # Formulaire de contact, sans traitement d'envoi
├── style.css        # Feuille de styles chargée par index.html
└── README.md        # Documentation du projet
```

Les quatre pages secondaires définissent leurs styles dans des blocs `<style>` intégrés au HTML. Elles ne chargent pas `style.css` : une modification de ce fichier ne change donc que la page d'accueil dans l'état actuel du projet.

## Ouvrir le site localement

Un navigateur web suffit pour consulter les pages statiques. Aucune installation de dépendances, compilation ou configuration de base de données n'est nécessaire.

1. Ouvrir le dossier du dépôt dans l'explorateur de fichiers.
2. Ouvrir `index.html` dans un navigateur, par double-clic si les fichiers HTML lui sont associés, ou avec **Ouvrir avec**.
3. Utiliser les liens du menu pour accéder aux quatre autres pages.

Conserver les fichiers dans le même dossier : les liens vers les pages et la feuille CSS sont relatifs. Cette ouverture locale permet de consulter le site ; elle n'ajoute aucun traitement au formulaire de contact.

Le dépôt ne fournit pas de script d'installation, de démarrage, de test ou de compilation, ni de manifeste `package.json`. Node.js et npm ne sont pas requis pour cette consultation locale.

## Fonctionnalités présentes dans le code

- Navigation entre Accueil, À propos, Services, Portfolio et Contact, avec un lien marqué comme actif sur chaque page.
- Présentation du studio et de trois catégories de services : développement Web et applications, UI/UX et design, branding et stratégie.
- Présentation de trois réalisations dans le portfolio. Les liens « Demander une démo » conduisent à la page Contact.
- Liens « Demander un devis » depuis les services vers la page Contact.
- Formulaire comportant les champs nom ou entreprise, adresse e-mail et message, avec des libellés associés. Les attributs `required` et le type `email` déclarent une validation native côté navigateur.
- Titres, descriptions, langue française, encodage UTF-8 et balise viewport déclarés dans les cinq pages.

Les applications décrites dans le portfolio ne sont pas incluses dans ce dépôt : celui-ci contient leurs présentations textuelles.

## Fonctionnalités incomplètes et points non vérifiés

| Élément | État actuel |
| --- | --- |
| Envoi du formulaire | Non implémenté. Le formulaire n'a pas d'attribut `action` ni de méthode explicite, les champs n'ont pas d'attribut `name`, et aucun gestionnaire JavaScript ou traitement serveur n'est présent. Aucune réception de message n'est assurée. |
| Affichage mobile | La balise viewport et des grilles adaptatives sont présentes, mais aucune media query ni adaptation spécifique du menu n'est définie. Le comportement aux petites largeurs reste à vérifier. |
| Accessibilité et compatibilité | Aucun contrôle en navigateur du parcours clavier, du contraste ou de la compatibilité entre navigateurs n'a été effectué lors de cette mise à jour documentaire. |
| Tests et qualité | Aucun test automatisé, validateur HTML/CSS ou outil de lint n'est configuré dans le dépôt. |
| Publication | Aucune configuration de déploiement n'est versionnée. L'existence et le fonctionnement d'un éventuel site publié n'ont pas été vérifiés. |

## Vérifications manuelles conseillées

Ces vérifications sont proposées pour une prochaine validation du site ; elles ne constituent pas des résultats de tests déjà exécutés.

1. Ouvrir chacune des cinq pages et vérifier la navigation ainsi que le chargement des styles.
2. Réduire la largeur de la fenêtre pour repérer les débordements du menu, des cartes et des boutons.
3. Parcourir les liens et les champs avec la touche Tab pour contrôler l'ordre de navigation et la visibilité du focus.
4. Vérifier la validation native des champs avec des valeurs fictives, en gardant à l'esprit que l'envoi de message n'est pas implémenté.

## Recommandations techniques

- Centraliser progressivement les styles communs dans `style.css`, puis vérifier chaque page pour préserver sa présentation.
- Adapter la navigation et les espacements aux petits écrans après vérification du rendu réel.
- Définir le traitement du formulaire avant de proposer un envoi opérationnel : destination, méthode de soumission, noms des champs, validation côté serveur et messages de succès ou d'erreur.
- Vérifier la structure HTML, la navigation au clavier et les contrastes avant publication.
- Documenter la procédure de publication lorsqu'un hébergement aura été choisi et vérifié.

Ces recommandations décrivent des travaux possibles ; elles ne sont pas implémentées par cette mise à jour du README.
