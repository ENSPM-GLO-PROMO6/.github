# Directives de Contribution

Ce document présente les règles et bonnes pratiques à suivre pour contribuer aux projets de l'organisation ENSPM-GENIE-LOGICIEL-PROMO6.

## Principes généraux

Tous les membres de l'organisation ENSPM-GENIE-LOGICIEL-PROMO6 sont invités à contribuer aux projets en respectant ces principes :

- **Qualité du code** - Écrivez du code lisible, maintenable et documenté
- **Respect des délais** - Respectez les échéances fixées pour les contributions
- **Communication** - Communiquez clairement sur vos contributions et difficultés
- **Collaboration** - Travaillez avec respect et ouverture d'esprit

## Processus de contribution

### 1. Configuration initiale

1. Clonez le dépôt concerné :
   ```bash
   git clone https://github.com/ENSPM-GENIE-LOGICIEL-PROMO6/[nom-du-depot].git
   ```

2. Configurez votre environnement de développement en suivant les instructions du fichier README du projet

### 2. Workflow de développement

1. **Créez une branche** pour chaque nouvelle fonctionnalité ou correction :
   ```bash
   git checkout -b feature/nom-de-la-fonctionnalite
   # ou
   git checkout -b fix/nom-du-correctif
   ```

2. **Effectuez vos modifications** en respectant les conventions de codage du projet

3. **Testez vos modifications** pour vous assurer qu'elles fonctionnent correctement

4. **Validez vos modifications** avec des messages de commit clairs et descriptifs :
   ```bash
   git commit -m "Type: description concise de la modification"
   ```
   
   Types de commit recommandés :
   - `feat` : nouvelle fonctionnalité
   - `fix` : correction de bug
   - `docs` : modification de la documentation
   - `style` : formatage du code (sans changement fonctionnel)
   - `refactor` : refactorisation du code (sans changement fonctionnel)
   - `test` : ajout ou modification de tests
   - `chore` : modifications des outils de build, configurations, etc.

5. **Poussez votre branche** vers le dépôt distant :
   ```bash
   git push origin feature/nom-de-la-fonctionnalite
   ```

6. **Créez une Pull Request (PR)** sur GitHub :
   - Donnez un titre clair à votre PR
   - Décrivez les modifications apportées
   - Référencez les issues concernées (si applicable)

### 3. Révision de code

- Toutes les contributions doivent être revues par au moins un autre membre de l'équipe
- Répondez aux commentaires et apportez les modifications nécessaires
- Une fois approuvée, la PR peut être fusionnée par les mainteneurs du projet

## Standards de codage

### Général

- Utilisez des noms descriptifs pour les variables, fonctions et classes
- Respectez les principes SOLID et DRY
- Commentez votre code lorsque nécessaire (logique complexe, décisions importantes)
- Évitez les commentaires obsolètes ou redondants

### Langages spécifiques

#### Java
- Suivez les conventions Oracle pour Java
- Utilisez la notation camelCase pour les variables et méthodes
- Utilisez PascalCase pour les noms de classes
- Préfixez les constantes avec `SNAKE_CASE_MAJUSCULE`

#### Python
- Suivez la PEP 8
- Utilisez snake_case pour les variables et fonctions
- Utilisez PascalCase pour les noms de classes
- Utilisez des docstrings pour documenter les fonctions et classes

#### JavaScript
- Suivez les conventions ESLint ou StandardJS
- Utilisez camelCase pour les variables et fonctions
- Utilisez PascalCase pour les composants React et les classes

## Documentation

- Chaque projet doit avoir un fichier README.md à jour
- Les API doivent être documentées selon les standards du langage utilisé
- Les décisions techniques importantes doivent être documentées dans un fichier ARCHITECTURE.md

## Tests

- Les nouvelles fonctionnalités doivent être accompagnées de tests
- Visez une couverture de code d'au moins 80%
- Les tests doivent passer avant de soumettre une PR

## Gestion des versions

Nous suivons la convention [Semantic Versioning](https://semver.org/lang/fr/) :

- **MAJEUR.MINEUR.CORRECTIF**
- Incrémentez la version **MAJEURE** pour des changements incompatibles
- Incrémentez la version **MINEURE** pour des ajouts compatibles
- Incrémentez la version **CORRECTIF** pour des corrections de bugs compatibles

## Questions et assistance

Si vous avez des questions ou besoin d'aide concernant le processus de contribution, n'hésitez pas à :

- Contacter les responsables du projet
- Créer une issue sur GitHub
- Envoyer un e-mail à genie-logiciel-promo6@enspm.ac.ma

---

Ces directives peuvent évoluer au fil du temps. Les contributeurs sont invités à consulter régulièrement ce document pour rester informés des changements.
