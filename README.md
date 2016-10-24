A basic container image with Apache2, mod_php and drush for running Drupal CMS.

Mount Drupal installation to the `/var/www/html`.

```console
docker volume add drupal-data
docker run -v drupal-data:/var/www/html --name drupal selim13/drupal-generic
```

To exec drush:

```console
docker exec --user www-data drupal drush
```

No environment variables configuration.