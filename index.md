## [Composer Check](https://github.com/gapple/drush-composercheck)

Prevent execution of certain drush commands when project uses composer for dependency management 

---

| Drupal | Supported |
|-------:|:---------:|
|    7.x |     ✅    |
|    8.x |     ✅    |


## [Filesync](https://github.com/gapple/drush-filesync)

Sync file directories between environments

    drush file-sync @source @destination

---

| Drupal | Supported |
|-------:|:---------:|
|    7.x |     ✅    |
|    8.x |     ✅    |

## [Update Rerun](https://github.com/gapple/drush-update-rerun)

Re-execute a single module update hook

    drush update_rerun foo_module 7001

---

| Drupal | Supported |
|-------:|:---------:|
|    7.x |     ✅    |
|    8.x |     ❌    |

# Installation

## Global
### Using Composer
1. Require `composer/installers`
    ```bash
    composer global require composer/installers
    ```

2. Configure the installer path for drush plugins in `~/.composer/composer.json`
    ```json
    {
      "extra": {
        "installer-paths": {
          "../.drush/plugins/{$name}": ["type:drupal-drush"]
        }
      }
    }
    ```

3. Require the plugin
    ```bash
    composer global require gapple/drush-composercheck
    ```

### Manual Installation
1. Download the release package
2. Unzip the package to `~/.drush/`


## Project
### Using Composer
1. Require `composer/installers` in your project
    ```bash
    composer require composer/installers
    ```

2. Configure the installer path for drush plugins in your project's `composer.json`
    ```json
    {
      "extra": {
        "installer-paths": {
          "drush/contrib/{$name}": ["type:drupal-drush"]
        }
      }
    }
    ```

3. Require the plugin in your project
    ```bash
    composer require gapple/drush-composercheck
    ```

### Manual Installation
1. Download the release package
2. Unzip the package to the `drush` folder within your project
