# Normes de Codage

Ce document définit les normes et conventions de codage à respecter dans tous les projets de l'organisation ENSPM-GENIE-LOGICIEL-PROMO6.

## Table des matières

1. [Principes généraux](#principes-généraux)
2. [Conventions de nommage](#conventions-de-nommage)
3. [Normes par langage](#normes-par-langage)
   - [Java](#java)
   - [Python](#python)
   - [JavaScript/TypeScript](#javascripttypescript)
   - [C/C++](#cc)
   - [SQL](#sql)
4. [Documentation](#documentation)
5. [Tests](#tests)
6. [Revue de code](#revue-de-code)

## Principes généraux

- **Lisibilité** : Le code doit être facile à lire et à comprendre
- **Maintenabilité** : Privilégier des solutions simples et faciles à maintenir
- **Consistance** : Appliquer les mêmes conventions dans tout le projet
- **Tests** : Tout code doit être testé de manière appropriée
- **Documentation** : Documenter le code de manière adéquate

## Conventions de nommage

### Général

- Utilisez des noms descriptifs qui expliquent clairement le rôle ou la fonction
- Évitez les abréviations sauf si elles sont universellement comprises
- Préférez la précision à la brièveté
- Respectez les conventions spécifiques à chaque langage

### Exemples par convention

| Type | Convention | Exemple |
|------|------------|---------|
| Variable | camelCase ou snake_case selon le langage | `userName` ou `user_name` |
| Constante | SNAKE_CASE_MAJUSCULE | `MAX_CONNECTIONS` |
| Fonction/Méthode | camelCase ou snake_case selon le langage | `calculateTotal()` ou `calculate_total()` |
| Classe | PascalCase | `UserAccount` |
| Interface | PascalCase (parfois avec préfixe I) | `Comparable` ou `IComparable` |
| Fichier | Selon les conventions du langage | `userService.js` ou `user_service.py` |
| Package/Module | Tout en minuscules, sans underscore | `com.enspm.utils` |

## Normes par langage

### Java

#### Style général
- Suivez les [conventions de codage Java d'Oracle](https://www.oracle.com/java/technologies/javase/codeconventions-contents.html)
- Indentation : 4 espaces (pas de tabulations)
- Longueur maximale de ligne : 100 caractères

#### Conventions de nommage
- Variables et méthodes : `camelCase`
- Classes et interfaces : `PascalCase`
- Constantes : `SNAKE_CASE_MAJUSCULE`
- Packages : `toutminuscule` (ex: `fr.enspm.projetx.utils`)

#### Bonnes pratiques
- Privilégiez l'immutabilité quand c'est possible
- Utilisez les annotations appropriées (`@Override`, `@Deprecated`, etc.)
- Évitez les exceptions génériques (`Exception`, `RuntimeException`)
- Utilisez les interfaces de collections plutôt que les implémentations spécifiques

### Python

#### Style général
- Suivez la [PEP 8](https://www.python.org/dev/peps/pep-0008/)
- Indentation : 4 espaces (pas de tabulations)
- Longueur maximale de ligne : 79 caractères

#### Conventions de nommage
- Variables et fonctions : `snake_case`
- Classes : `PascalCase`
- Constantes : `SNAKE_CASE_MAJUSCULE`
- Modules : `snake_case`

#### Bonnes pratiques
- Utilisez des docstrings pour documenter les modules, classes et fonctions
- Utilisez les type hints (pour Python 3.5+)
- Évitez l'utilisation de variables globales
- Utilisez les gestionnaires de contexte (`with`) pour les ressources

### JavaScript/TypeScript

#### Style général
- Suivez les règles [ESLint](https://eslint.org/) ou [StandardJS](https://standardjs.com/)
- Indentation : 2 espaces (pas de tabulations)
- Longueur maximale de ligne : 80 caractères
- Point-virgule à la fin des instructions

#### Conventions de nommage
- Variables et fonctions : `camelCase`
- Classes et composants React : `PascalCase`
- Constantes : `SNAKE_CASE_MAJUSCULE`
- Fichiers : `camelCase.js` ou `PascalCase.tsx` pour les composants React

#### Bonnes pratiques
- Préférez `const` et `let` à `var`
- Utilisez les fonctions fléchées pour préserver le contexte `this`
- Utilisez la déstructuration pour accéder aux propriétés des objets
- Documentez avec JSDoc pour les projets JavaScript

### C/C++

#### Style général
- Suivez le [Google C++ Style Guide](https://google.github.io/styleguide/cppguide.html)
- Indentation : 2 espaces (pas de tabulations)
- Longueur maximale de ligne : 80 caractères

#### Conventions de nommage
- Variables : `snake_case`
- Fonctions : `PascalCase` ou `camelCase` (être cohérent)
- Classes : `PascalCase`
- Constantes et macros : `SNAKE_CASE_MAJUSCULE`
- Fichiers : `.h` pour les en-têtes, `.c`/`.cpp` pour l'implémentation

#### Bonnes pratiques
- Préférez les références aux pointeurs quand c'est possible
- Utilisez les smart pointers plutôt que les pointeurs bruts
- Évitez l'allocation dynamique sauf si nécessaire
- Commentez les sections complexes du code

### SQL

#### Style général
- Mots-clés SQL en MAJUSCULES
- Indentation cohérente pour les clauses
- Une clause par ligne pour les requêtes complexes

#### Conventions de nommage
- Tables : singulier, `snake_case` (ex: `user`, `product_category`)
- Colonnes : `snake_case` (ex: `first_name`, `creation_date`)
- Clés primaires : `id` ou `table_id`
- Clés étrangères : `reference_table_id` (ex: `user_id`)

#### Bonnes pratiques
- Utilisez des contraintes pour garantir l'intégrité des données
- Indexez les colonnes fréquemment utilisées dans les requêtes
- Évitez les requêtes imbriquées si possible
- Commentez les requêtes complexes

## Documentation

### Exigences minimales
- Chaque fichier doit avoir un en-tête qui décrit son contenu et son objectif
- Les fonctions et méthodes publiques doivent être documentées
- Les algorithmes complexes doivent être expliqués
- Le code doit être auto-documenté avec des noms significatifs

### Format de documentation
- Java : JavaDoc
- Python : Docstrings (format Google, NumPy ou reStructuredText)
- JavaScript : JSDoc
- C/C++ : Doxygen

### Exemple (Java)
```java
/**
 * Calcule le montant total de la commande incluant les taxes.
 *
 * @param items Liste des articles dans la commande
 * @param taxRate Taux de taxe applicable (ex: 0.20 pour 20%)
 * @return Montant total avec taxes
 * @throws IllegalArgumentException si le taux de taxe est négatif
 */
public double calculateOrderTotal(List<OrderItem> items, double taxRate) {
    // Implémentation
}
```

## Tests

### Types de tests
- **Tests unitaires** : Testent des composants individuels
- **Tests d'intégration** : Testent l'interaction entre composants
- **Tests fonctionnels** : Testent les fonctionnalités complètes
- **Tests de performance** : Évaluent les performances du système

### Bonnes pratiques
- Suivez le principe AAA (Arrange, Act, Assert)
- Testez les cas limites et les cas d'erreur
- Un test doit être indépendant des autres tests
- Évitez les dépendances externes dans les tests unitaires
- Utilisez des mocks et des stubs quand approprié

### Couverture de code
- Visez une couverture de code d'au moins 80%
- Tous les chemins d'exécution critiques doivent être testés
- Les tests doivent être maintenus et mis à jour avec le code

## Revue de code

### Processus
1. Le développeur crée une Pull Request (PR)
2. Au moins un autre développeur examine le code
3. Les commentaires sont discutés et traités
4. Une fois approuvé, le code peut être fusionné

### Critères d'évaluation
- Le code respecte-t-il les normes définies ?
- Le code est-il fonctionnel et sans bugs évidents ?
- Le code est-il bien testé ?
- La documentation est-elle adéquate ?
- Le code est-il efficace et bien conçu ?

---

Ces normes sont destinées à évoluer. Si vous avez des suggestions d'amélioration, veuillez créer une issue ou une pull request.
