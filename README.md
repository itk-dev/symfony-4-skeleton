# Symfony 4 skeleton

This is a skeleton for a [Symfony 4](https://symfony.com/doc/current/setup.html)
project.

--- ✂ --------------------------------------------------------------------------

# Skeleton installation (delete this section when done)

```sh
composer create-project itk-dev/symfony-4-skeleton my-itk-dev-project
```

## Post skeleton installation

- [ ] Edit [`.env`](.env) and define the `COMPOSE_PROJECT_NAME` variable.
- [ ] Edit `$header` in [`.php_cs.dist`](.php_cs.dist).
- [ ] Edit [`README.md`](README.md) (Remove optional sections and describe your
      actual project).

## Suggested packages

[Doctrine](https://symfony.com/doc/current/doctrine.html):

```sh
composer require symfony/orm-pack
composer require --dev symfony/maker-bundle
```

Set `DATABASE_URL` in `.env.dev`:

```sh
DATABASE_URL=mysql://db:db@mariadb:3306/db
```

[EasyAdminBundle](https://symfony.com/doc/master/bundles/EasyAdminBundle/index.html):

```sh
composer require admin
```

[EasyAdmin Extension](https://github.com/alterphp/EasyAdminExtensionBundle):

```sh
composer require alterphp/easyadmin-extension-bundle
```

[API Platform](https://api-platform.com/):

```sh
composer require api
```

[Encore](https://symfony.com/doc/current/frontend/encore/installation.html)

```sh
composer require encore
```

Add tools for linting assets:

```sh
yarn add --dev eslint eslint-config-standard eslint-plugin-import eslint-plugin-node eslint-plugin-promise eslint-plugin-standard
yarn add --dev stylelint stylelint-config-recommended-scss stylelint-scss
```

Add these lines to `scripts` in `package.json`:

```json
        "check-coding-standards/stylelint": "stylelint --config=.stylelintrc.js 'assets/**/*.scss'",
        "check-coding-standards/scss": "yarn run check-coding-standards/stylelint",
        "check-coding-standards/eslint": "eslint --config .eslintrc.js 'assets/**/*.js'",
        "check-coding-standards/js": "yarn run check-coding-standards/eslint",
        "check-coding-standards": "yarn run check-coding-standards/scss; yarn run check-coding-standards/js",
        "apply-coding-standards/stylelint": "stylelint --config=.stylelintrc.js 'assets/**/*.scss' --fix",
        "apply-coding-standards/scss": "yarn run apply-coding-standards/stylelint",
        "apply-coding-standards/eslint": "eslint --config .eslintrc.js 'assets/**/*.js' --fix",
        "apply-coding-standards/js": "yarn run apply-coding-standards/eslint",
        "apply-coding-standards": "yarn run apply-coding-standards/scss; yarn run apply-coding-standards/js"
```

See also:

- [Encore with bootstrap](https://symfony.com/doc/current/frontend/encore/bootstrap.html#importing-bootstrap-styles)
- [Boostrap 4 Form Theme](https://symfony.com/doc/current/form/bootstrap4.html)

--- ✂ --------------------------------------------------------------------------

## Starting the show

```sh
docker-compose pull
docker-compose up -d
```

Open the site in your default browser:

```sh
open http://$(docker-compose port nginx 80)
```

## Coding standards

Check Symfony coding standards using [PHP Coding Standards
Fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer) and
[PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer):

```sh
composer check-coding-standards
```

Apply Symfony coding standards:

```sh
composer apply-coding-standards
```

### Twig (experimental)

Check Twig templates using [Twigcs](https://github.com/allocine/twigcs):

```sh
composer check-coding-standards/twigcs
```

--- ✂ --- (remove this section if not using encore) ----------------------------

### Assets (SCSS and JavaScript)

Check coding standards in all assets:

```sh
yarn check-coding-standards
```

Check coding standards in SCSS files:

```sh
yarn check-coding-standards/scss
```

Check coding standards in JavaScript files:

```sh
yarn check-coding-standards/js
```

Apply coding standards to all assets:

```sh
yarn apply-coding-standards
```

Apply coding standards to SCSS files:

```sh
yarn apply-coding-standards/scss
```

Apply coding standards to JavaScript files:

```sh
yarn apply-coding-standards/js
```

--- ✂ --------------------------------------------------------------------------
