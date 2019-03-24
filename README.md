# Symfony 4 skeleton

This is a skeleton for a [Symfony 4](https://symfony.com/doc/current/setup.html)
project.

--- ✂ --------------------------------------------------------------------------

# Skeleton installation (delete this section when done)

```sh
composer create-project itk-dev/symfony-4-skeleton:dev-master my-project
```

## Post skeleton installation

- [ ] Edit [`.env`](.env) and define the `COMPOSE_PROJECT_NAME` variable.
- [ ] Edit `$header` in [`.php_cs.dist`](.php_cs.dist).
- [ ] Edit [`README.md`](README.md) (remove this section and describe your
      actual project).

## Suggested packages

[Doctrine](https://symfony.com/doc/current/doctrine.html):

```sh
composer require symfony/orm-pack
composer require --dev symfony/maker-bundle
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
