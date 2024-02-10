
<p align="right">
<a href="https://platform.sh">
<img src="https://platform.sh/logos/redesign/Platformsh_logo_black.svg" width="150px">
</a>
</p>

<p align="center">
<a href="https://www.drupal.org/">
<img src="header.svg">
</a>
</p>

<h1 align="center">Deploy Drupal 10 on Platform.sh</h1>

<p align="center">
<strong>Contribute, request a feature, or check out our resources</strong>
<br />
<br />
<a href="https://community.platform.sh"><strong>Join our community</strong></a>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
<a href="https://docs.platform.sh"><strong>Documentation</strong></a>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
<a href="https://platform.sh/blog"><strong>Blog</strong></a>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
<a href="https://github.com/platformsh-templates/drupal10/issues/new?assignees=&labels=bug&template=bug_report.yml"><strong>Report a bug</strong></a>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
<a href="https://github.com/platformsh-templates/drupal10/issues/new?assignees=&labels=feature+request&template=improvements.yml"><strong>Request a feature</strong></a>
<br /><br />
</p>

<p align="center">
<a href="https://github.com/platformsh-templates/drupal10/issues">
<img src="https://img.shields.io/github/issues/platformsh-templates/drupal10.svg?style=for-the-badge&labelColor=f4f2f3&color=ffd9d9&label=Issues" alt="Open issues" />
</a>&nbsp&nbsp
<a href="https://github.com/platformsh-templates/drupal10/pulls">
<img src="https://img.shields.io/github/issues-pr/platformsh-templates/drupal10.svg?style=for-the-badge&labelColor=f4f2f3&color=ffd9d9&label=Pull%20requests" alt="Open PRs" />
</a>&nbsp&nbsp
<a href="https://github.com/platformsh-templates/drupal10/blob/master/LICENSE">
<img src="https://img.shields.io/static/v1?label=License&message=MIT&style=for-the-badge&labelColor=f4f2f3&color=ffd9d9" alt="License" />
</a>&nbsp&nbsp
<br /><br />
<a href="https://console.platform.sh/projects/create-project/?template=https://raw.githubusercontent.com/platformsh/template-builder/master/templates/drupal10/.platform.template.yaml&utm_campaign=deploy_on_platform?utm_medium=button&utm_source=affiliate_links&utm_content=https://raw.githubusercontent.com/platformsh-templates/drupal10/updates/.platform.template.yaml" target="_blank" title="Deploy with Platform.sh"><img src="https://platform.sh/images/deploy/deploy-button-lg-blue.svg" width="175px"></a>
</p>
</p>

<hr>

<p align="center">
<strong>Contents</strong>
<br /><br />
<a href="#about"><strong>About</strong></a>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
<a href="#getting-started"><strong>Getting started</strong></a>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
<a href="#migrate"><strong>Migrate</strong></a>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
<a href="#learn"><strong>Learn</strong></a>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
<a href="#contribute"><strong>Contribute</strong></a>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
<br />
</p>
<hr>

## About

This template builds Drupal 10 using the "Drupal Recommended" Composer project. It is pre-configured to use MariaDB and Redis for caching. The Drupal installer will skip asking for database credentials as they are already provided.

Drupal is a flexible and extensible PHP-based CMS framework.

### Features

- PHP 8.2
- MariaDB 10.11
- Redis 7.2
- Drush included
- Automatic TLS certificates
- Composer-based build


## Getting started

### Deploy

#### Quickstart


The quickest way to deploy this template on Platform.sh is by clicking the button below.
This will automatically create a new project and initialize the repository for you.

<p align="center">
    <a href="https://console.platform.sh/projects/create-project/?template=https://raw.githubusercontent.com/platformsh/template-builder/master/templates/drupal10/.platform.template.yaml">
        <img src="https://platform.sh/images/deploy/lg-blue.svg" alt="Deploy on Platform.sh" width="170px" />
    </a>
</p>
<br/>



You can also quickly recreate this project locally with the following command:

```bash
composer create-project platformsh/drupal10 -s dev
```


> **Note:**
>
> Platform.sh templates prioritize upstream release versions over our own. Despite this, we update template dependencies on a scheduled basis independent of those upstreams. Because of this, template repos do not contain releases. This may change in the future, but until then the `-s dev` flag is necessary to use `composer create-project`.



#### Other deployment options

For all of the other options below, clone this repository first:

```bash
git clone https://github.com/platformsh-templates/drupal10
```

If you're trying to deploy from GitHub, you can generate a copy of this repository first in your own namespace by clicking the [Use this template](https://github.com/platformsh-templates/drupal10/generate) button at the top of this page.

Then you can clone a copy of it locally with `git clone git@github.com:YOUR_NAMESPACE/drupal10.git`.


<details>
<summary>Deploy directly to Platform.sh from the command line</summary>
<!-- <blockquote>
<br/> -->

1. Create a free trial:

   [Register for a 30 day free trial with Platform.sh](https://auth.api.platform.sh/register). When you have completed signup, select the **Create from scratch** project option. Give you project a name, and select a region where you would like it to be deployed. As for the *Production environment* option, make sure to match it to this repository's settings, or to what you have updated the default branch to locally.

1. Install the Platform.sh CLI

   #### Linux/OSX

   ```bash
   curl -sS https://platform.sh/cli/installer | php
   ```

   #### Windows

   ```bash
   curl -f https://platform.sh/cli/installer -o cli-installer.php
   php cli-installer.php
   ```

   You can verify the installation by logging in (`platformsh login`) and listing your projects (`platform project:list`).

1. Set the project remote

   Find your `PROJECT_ID` by running the command `platform project:list`

   ```bash
   +---------------+------------------------------------+------------------+---------------------------------+
   | ID            | Title                              | Region           | Organization                    |
   +---------------+------------------------------------+------------------+---------------------------------+
   | PROJECT_ID    | Your Project Name                  | xx-5.platform.sh | your-username                   |
   +---------------+------------------------------------+------------------+---------------------------------+
   ```

   Then from within your local copy, run the command `platform project:set-remote PROJECT_ID`.

1. Push

   ```bash
   git push platform DEFAULT_BRANCH
   ```

<!-- <br/>
</blockquote> -->
</details>

<details>
<summary>Integrate with a GitHub repo and deploy pull requests</summary>
<!-- <blockquote>
<br/> -->

1. Create a free trial:

   [Register for a 30 day free trial with Platform.sh](https://auth.api.platform.sh/register). When you have completed signup, select the **Create from scratch** project option. Give you project a name, and select a region where you would like it to be deployed. As for the *Production environment* option, make sure to match it to whatever you have set at `https://YOUR_NAMESPACE/nextjs-drupal`.

1. Install the Platform.sh CLI

   #### Linux/OSX

   ```bash
   curl -sS https://platform.sh/cli/installer | php
   ```

   #### Windows

   ```bash
   curl -f https://platform.sh/cli/installer -o cli-installer.php
   php cli-installer.php
   ```

   You can verify the installation by logging in (`platformsh login`) and listing your projects (`platform project:list`).

1. Setup the integration:

   Consult the [GitHub integration documentation](https://docs.platform.sh/integrations/source/github.html#setup) to finish connecting your repository to a project on Platform.sh. You will need to create an Access token on GitHub to do so.

<!-- <br/>
</blockquote> -->
</details>

<details>
<summary>Integrate with a GitLab repo and deploy merge requests</summary>
<!-- <blockquote>
<br/> -->

1. Create a free trial:

   [Register for a 30 day free trial with Platform.sh](https://auth.api.platform.sh/register). When you have completed signup, select the **Create from scratch** project option. Give you project a name, and select a region where you would like it to be deployed. As for the *Production environment* option, make sure to match it to this repository's settings, or to what you have updated the default branch to locally.

1. Install the Platform.sh CLI

   #### Linux/OSX

   ```bash
   curl -sS https://platform.sh/cli/installer | php
   ```

   #### Windows

   ```bash
   curl -f https://platform.sh/cli/installer -o cli-installer.php
   php cli-installer.php
   ```

   You can verify the installation by logging in (`platformsh login`) and listing your projects (`platform project:list`).

1. Create the repository

   Create a new repository on GitLab, set it as a new remote for your local copy, and push to the default branch.

1. Setup the integration:

   Consult the [GitLab integration documentation](https://docs.platform.sh/integrations/source/gitlab.html#setup) to finish connecting a repository to a project on Platform.sh. You will need to create an Access token on GitLab to do so.

<!-- <br/>
</blockquote> -->
</details>

<details>
<summary>Integrate with a Bitbucket repo and deploy pull requests</summary>
<!-- <blockquote>
<br/> -->

1. Create a free trial:

   [Register for a 30 day free trial with Platform.sh](https://auth.api.platform.sh/register). When you have completed signup, select the **Create from scratch** project option. Give you project a name, and select a region where you would like it to be deployed. As for the *Production environment* option, make sure to match it to this repository's settings, or to what you have updated the default branch to locally.

1. Install the Platform.sh CLI

   #### Linux/OSX

   ```bash
   curl -sS https://platform.sh/cli/installer | php
   ```

   #### Windows

   ```bash
   curl -f https://platform.sh/cli/installer -o cli-installer.php
   php cli-installer.php
   ```

   You can verify the installation by logging in (`platformsh login`) and listing your projects (`platform project:list`).

1. Create the repository

   Create a new repository on Bitbucket, set it as a new remote for your local copy, and push to the default branch.

1. Setup the integration:

   Consult the [Bitbucket integration documentation](https://docs.platform.sh/integrations/source/bitbucket.html#setup) to finish connecting a repository to a project on Platform.sh. You will need to create an Access token on Bitbucket to do so.

<!-- <br/>
</blockquote> -->
</details>



### Post-install

Run through the Drupal installer as normal.  You will not be asked for database credentials as those are already provided.

### Local development

This section provides instructions for running the `drupal10` template locally, connected to a live database instance on an active Platform.sh environment.

In all cases for developing with Platform.sh, it's important to develop on an isolated environment - do not connect to data on your production environment when developing locally.
Each of the options below assume that you have already deployed this template to Platform.sh, as well as the following starting commands:

```bash
$ platform get PROJECT_ID
$ cd project-name
$ platform environment:branch updates
```

<details>
<summary>Drupal: using ddev</summary><br />

ddev provides an integration with Platform.sh that makes it simple to develop Drupal locally. Check the [providers documentation](https://ddev.readthedocs.io/en/latest/users/providers/platform/) for the most up-to-date information.

In general, the steps are as follows:

1. [Install ddev](https://ddev.readthedocs.io/en/stable/#installation).
1. A configuration file has already been provided at `.ddev/providers/platform.yaml`, so you should not need to run `ddev config`.
1. [Retrieve an API token](https://docs.platform.sh/development/cli/api-tokens.html#get-a-token) for your organization via the management console.
1. Update your dedev global configuration file to use the token you've just retrieved:
    ```yaml
    web_environment:
    - PLATFORMSH_CLI_TOKEN=abcdeyourtoken`
    ```
1. Run `ddev restart`.
1. Get your project ID with `platform project:info`. If you have not already connected your local repo with the project (as is the case with a source integration, by default), you can run `platform project:list` to locate the project ID, and `platform project:set-remote PROJECT_ID` to configure Platform.sh locally.
1. Update the `.ddev/providers/platform.yaml` file for your current setup:
    ```yaml
    environment_variables:
    project_id: PROJECT_ID
    environment: CURRENT_ENVIRONMENT
    application: drupal
    ```
1. Get the current environment's data with `ddev pull platform`.
1. When you have finished with your work, run `ddev stop` and `ddev poweroff`.

</details>
<details>
<summary>Drupal: using Lando</summary><br />

Lando supports PHP applications [configured to run on Platform.sh](https://docs.platform.sh/development/local/lando.html), and pulls from the same container registry Platform.sh uses on your remote environments during your local builds through its own [recipe and plugin](https://docs.lando.dev/platformsh/).

1. [Install Lando](https://docs.lando.dev/getting-started/installation.html).
1. Make sure Docker is already running - Lando will attempt to start Docker for you, but it's best to have it running in the background before beginning.
1. Start your apps and services with the command `lando start`.
1. To get up-to-date data from your Platform.sh environment ([services *and* mounts](https://docs.lando.dev/platformsh/sync.html#pulling)), run the command `lando pull`.
1. If at any time you have updated your Platform.sh configuration files, run the command `lando rebuild`.
1. When you have finished with your work, run `lando stop` and `lando poweroff`.

</details>



> **Note:**
>
> For many of the steps above, you may need to include the CLI flags `-p PROJECT_ID` and `-e ENVIRONMENT_ID` if you are not in the project directory or if the environment is associated with an existing pull request.


## Migrate

The steps below outline the important steps for migrating your application to Platform.sh - adding the required configuration files and dependencies, for example.
Not every step will be applicable to each person's migration.
These steps actually assume the earliest starting point possible - that there is no code at all locally, and that this template repository will be rebuilt completely from scratch.

- [Getting started](#getting-started-1)
- [Adding and updating files](#adding-and-updating-files)
- [Dependencies](#dependencies)
- [Deploying to Platform.sh](#deploying-to-platformsh)
- [Migrating your data](#migrating-your-data)
- [Next steps](#next-steps)

If you already have code you'd like to migrate, feel free to focus on the steps most relevant to your application and skip the first section.

### Getting started

Assuming that your starting point is no local code, the steps below will setup a starting repository we can begin to make changes to to rebuild this template and migrate to Platform.sh.
If you already have a codebase you are trying to migrate, move onto the next step - [Adding and updating files](#adding-and-updating-files) - and substitute any reference to the default branch `main` with some other branch name.



```bash
$ mkdir drupal10 && cd drupal10
$ git init
$ git remote add upstream https://github.com/drupal/recommended-project.git
$ git branch -m main
$ git fetch --all --depth=2
$ git fetch --all --tags
$ git merge --allow-unrelated-histories -X theirs 10.0.0-rc1

```



### Adding and updating files

A small number of files need to be added to or modified in your repository at this point.
Some of them explicitly configure how the application is built and deployed on Platform.sh, while others simply modify files you may already have locally, in which case you will need to replicate those changes.

Open the dropdown below to view all of the **Added** and **Updated** files you'll need to reproduce in your migration.

<details>
<summary><strong>View files</strong></summary><br/>



|  File | Purpose    |
|:-----------|:--------|
| [`config/sync/.gitkeep`](config/sync/.gitkeep) | **Added** |
| [`web/sites/default/settings.php`](web/sites/default/settings.php) | **Updated:**<br><br> The Drupal settings file has been updated to import and use `web/sites/default/settings.platformsh.php`. |
| [`web/sites/default/settings.platformsh.php`](web/sites/default/settings.platformsh.php) | **Added:**<br><br> Contains Platform.sh-specific configuration, namely setting up the database connection to the MariaDB service and caching via Redis. |
| [`.environment`](.environment) | **Added:**<br><br> The `.environment` file is a convenient place to [set environment variables](https://docs.platform.sh/development/variables/set-variables.html#set-variables-via-script) relevant to your applications that may be dependent on the current environment. It is sourced before the start command is run, as the first step in the `deploy` and `post_deploy` hooks, and at the beginning of each session when you SSH into an application container. It is written in dash, so be aware of the differences to bash.<br><br>It can be used to set any environment variable, including ones that depend on Platform.sh-provided variables like `PLATFORM_RELATIONSHIPS` and `PLATFORM_ROUTES`, or to modify `PATH`. This file should not [produce output](https://docs.platform.sh/development/variables/set-variables.html#testing-environment-scripts).<br><br> Here, the Composer config and `PATH` are updated to allow executable app dependencies from Composer to be run from the path (i.e. `drush`). |
| [`.gitignore`](.gitignore) | **Added:**<br><br> A `.gitignore` file is not included in the upstream, so one has been added. |
| [`.platform.app.yaml`](.platform.app.yaml) | **Added:**<br><br> This file is required to define the build and deploy process for all application containers on Platform.sh. Within this file, the runtime version, relationships to service containers, and writable mounts are configured. It's also in this file that it is defined what dependencies are installed, when they are installed, and that package manager will be used to do so.<br><br>Take a look at the [Application](https://docs.platform.sh/configuration/app.html) documentation for more details about configuration. For more information about the sequence of events that lead from a build to deployment, see the [Build and deploy timeline documentation](https://docs.platform.sh/overview/build-deploy.html).<br><br> This template uses Composer 2 to install dependencies using the default `composer` [build flavor](https://docs.platform.sh/languages/php.html#build-flavor) prior to the `build` hook. Drush tasks are run during the `deploy` hook, and referenced again during the defined `cron` job. |
| [`drush/platformsh_generate_drush_yml.php`](drush/platformsh_generate_drush_yml.php) | **Added:**<br><br> This file has been included to generate the drush yaml configuration on every deployment. |
| [`.platform/services.yaml`](.platform/services.yaml) | **Added:**<br><br> Platform.sh provides a number of on-demand managed services that can easily be added to your projects. It's within this file that each service's version, name, resources, and additional configuration are set. See the [Services documentation](https://docs.platform.sh/configuration/services.html) for more details on configuration, version and service availability.<br><br> In this template, MariaDB and Redis have been configured. |
| [`.platform/routes.yaml`](.platform/routes.yaml) | **Added:**<br><br> This file is require to deploy on Platform.sh, as it defines how requests should be handled on the platform. It's within this file that redirects and basic caching can be configured. See the [Routes documentation](https://docs.platform.sh/configuration/routes.html) for more configuration details.<br><br> |
| [`php.ini`](php.ini) | **Added:**<br><br> An initial `php.ini` file has also beed added. The settings are a result of performance testing and best practice recommendations coming from [Blackfire.io](https://blackfire.io). They will initialize Drupal with a number of good baseline performance settings for production applications, and complement many of the tests specified in [`.blackfire.yml`](.blackfire.yml). |
| [`.blackfire.yml`](.blackfire.yml) | **Added:**<br><br> This file has been added to help you get started using [Blackfire.io](https://blackfire.io) on your project. See [the Blackfire section below](#blackfireio-creating-a-continuous-observability-strategy) for more information on how to get started. |
| [`.lando.upstream.yml`](.lando.upstream.yml) | **Added:**<br><br> This file configures [Lando](https://docs.platform.sh/development/local/lando.html) as a local development option for this template. See the [Platform.sh Lando plugin documentation](https://docs.lando.dev/platformsh/) for more information about configuration and the [Local development](#local-development) section of this README for how to get started. |
| [`.ddev/providers/platform.yaml`](.ddev/providers/platform.yaml) | **Added:**<br><br> This file configures [ddev](https://ddev.readthedocs.io/en/latest/users/providers/platform/) as a local development option for this template. See the [Platform.sh ddev integration documentation](https://ddev.readthedocs.io/en/latest/users/providers/platform/) for more information about configuration and the [Local development](#local-development) section of this README for how to get started. Be sure to follow the instructions provided through the ddev CLI and in the comments section of that file to correctly configure ddev for your project. |



</details>

### Dependencies and configuration

Sometimes it is necessary to install additional dependencies to and modify the configuration of an upstream project to deploy on Platform.sh.
When it is, we do our best to keep these modifications to the minimum necessary.
Run the commands below to reproduce the dependencies in this template.



```bash
$ composer require platformsh/config-reader drush/drush drupal/redis
$ composer config allow-plugins.composer/installers true --no-plugins
$ composer config allow-plugins.drupal/core-composer-scaffold true --no-plugins
$ composer config allow-plugins.drupal/core-project-message true --no-plugins
$ composer config allow-plugins.cweagans/composer-patches true --no-plugins

```



### Deploying to Platform.sh

Your repository now has all of the code it needs in order to deploy to Platform.sh.


<details>
<summary>Deploy directly to Platform.sh from the command line</summary>
<!-- <blockquote>
<br/> -->

1. Create a free trial:

   [Register for a 30 day free trial with Platform.sh](https://auth.api.platform.sh/register). When you have completed signup, select the **Create from scratch** project option. Give you project a name, and select a region where you would like it to be deployed. As for the *Production environment* option, make sure to match it to this repository's settings, or to what you have updated the default branch to locally.

1. Install the Platform.sh CLI

   #### Linux/OSX

   ```bash
   curl -sS https://platform.sh/cli/installer | php
   ```

   #### Windows

   ```bash
   curl -f https://platform.sh/cli/installer -o cli-installer.php
   php cli-installer.php
   ```

   You can verify the installation by logging in (`platformsh login`) and listing your projects (`platform project:list`).

1. Set the project remote

   Find your `PROJECT_ID` by running the command `platform project:list`

   ```bash
   +---------------+------------------------------------+------------------+---------------------------------+
   | ID            | Title                              | Region           | Organization                    |
   +---------------+------------------------------------+------------------+---------------------------------+
   | PROJECT_ID    | Your Project Name                  | xx-5.platform.sh | your-username                   |
   +---------------+------------------------------------+------------------+---------------------------------+
   ```

   Then from within your local copy, run the command `platform project:set-remote PROJECT_ID`.

1. Push

   ```bash
   git push platform DEFAULT_BRANCH
   ```

<!-- <br/>
</blockquote> -->
</details>

<details>
<summary>Integrate with a GitHub repo and deploy pull requests</summary>
<!-- <blockquote>
<br/> -->

1. Create a free trial:

   [Register for a 30 day free trial with Platform.sh](https://auth.api.platform.sh/register). When you have completed signup, select the **Create from scratch** project option. Give you project a name, and select a region where you would like it to be deployed. As for the *Production environment* option, make sure to match it to whatever you have set at `https://YOUR_NAMESPACE/nextjs-drupal`.

1. Install the Platform.sh CLI

   #### Linux/OSX

   ```bash
   curl -sS https://platform.sh/cli/installer | php
   ```

   #### Windows

   ```bash
   curl -f https://platform.sh/cli/installer -o cli-installer.php
   php cli-installer.php
   ```

   You can verify the installation by logging in (`platformsh login`) and listing your projects (`platform project:list`).

1. Setup the integration:

   Consult the [GitHub integration documentation](https://docs.platform.sh/integrations/source/github.html#setup) to finish connecting your repository to a project on Platform.sh. You will need to create an Access token on GitHub to do so.

<!-- <br/>
</blockquote> -->
</details>

<details>
<summary>Integrate with a GitLab repo and deploy merge requests</summary>
<!-- <blockquote>
<br/> -->

1. Create a free trial:

   [Register for a 30 day free trial with Platform.sh](https://auth.api.platform.sh/register). When you have completed signup, select the **Create from scratch** project option. Give you project a name, and select a region where you would like it to be deployed. As for the *Production environment* option, make sure to match it to this repository's settings, or to what you have updated the default branch to locally.

1. Install the Platform.sh CLI

   #### Linux/OSX

   ```bash
   curl -sS https://platform.sh/cli/installer | php
   ```

   #### Windows

   ```bash
   curl -f https://platform.sh/cli/installer -o cli-installer.php
   php cli-installer.php
   ```

   You can verify the installation by logging in (`platformsh login`) and listing your projects (`platform project:list`).

1. Create the repository

   Create a new repository on GitLab, set it as a new remote for your local copy, and push to the default branch.

1. Setup the integration:

   Consult the [GitLab integration documentation](https://docs.platform.sh/integrations/source/gitlab.html#setup) to finish connecting a repository to a project on Platform.sh. You will need to create an Access token on GitLab to do so.

<!-- <br/>
</blockquote> -->
</details>

<details>
<summary>Integrate with a Bitbucket repo and deploy pull requests</summary>
<!-- <blockquote>
<br/> -->

1. Create a free trial:

   [Register for a 30 day free trial with Platform.sh](https://auth.api.platform.sh/register). When you have completed signup, select the **Create from scratch** project option. Give you project a name, and select a region where you would like it to be deployed. As for the *Production environment* option, make sure to match it to this repository's settings, or to what you have updated the default branch to locally.

1. Install the Platform.sh CLI

   #### Linux/OSX

   ```bash
   curl -sS https://platform.sh/cli/installer | php
   ```

   #### Windows

   ```bash
   curl -f https://platform.sh/cli/installer -o cli-installer.php
   php cli-installer.php
   ```

   You can verify the installation by logging in (`platformsh login`) and listing your projects (`platform project:list`).

1. Create the repository

   Create a new repository on Bitbucket, set it as a new remote for your local copy, and push to the default branch.

1. Setup the integration:

   Consult the [Bitbucket integration documentation](https://docs.platform.sh/integrations/source/bitbucket.html#setup) to finish connecting a repository to a project on Platform.sh. You will need to create an Access token on Bitbucket to do so.

<!-- <br/>
</blockquote> -->
</details>



### Migrating your data


If you are moving an existing site to Platform.sh, then in addition to code you also need to migrate your data. That means your database and your files.

<details>
<summary>Importing the database</summary><br/>

First, obtain a database dump from your current site and save your dump file as `database.sql`. Then, import the database into your Platform.sh site using the CLI:

```bash
platform sql -e main < database.sql
```

</details>
<details>
<summary>Importing files</summary><br/>

You first need to download your files from your current hosting environment.
The easiest way is likely with rsync, but consult your old host's documentation.

The `platform mount:upload` command provides a straightforward way to upload an entire directory to your site at once to a `mount` defined in a `.platform.app.yaml` file.
Under the hood, it uses an SSH tunnel and rsync, so it is as efficient as possible.
(There is also a `platform mount:download` command you can use to download files later.)
Run the following from your local Git repository root (modifying the `--source` path if needed and setting `BRANCH_NAME` to the branch you are using).

A few examples are listed below, but repeat for all directories that contain data you would like to migrate.

```bash
$ platform mount:upload -e main --mount web/sites/default/files --source ./web/sites/default/files
$ platform mount:upload -e main --mount private --source ./private
```

Note that `rsync` is picky about its trailing slashes, so be sure to include those.

</details>



### Next steps

With your application now deployed on Platform.sh, things get more interesting.
Run the command `platform environment:branch new-feature` for your project, or open a trivial pull request off of your current branch.

The resulting environment is an *exact* copy of production.
It contains identical infrastructure to what's been defined in your configuration files, and even includes data copied from your production environment in its services.
On this isolated environment, you're free to make any changes to your application you need to, and really test how they will behave on production.

After that, here are a collection of additional resources you might find interesting as you continue with your migration to Platform.sh:

- [Local development](#local-development)
- [Troubleshooting](#troubleshooting)
- [Adding a domain and going live](https://docs.platform.sh/domains/steps.html)
- [(CDN) Content Delivery Networks](https://docs.platform.sh/domains/cdn.html)
- [Performance and observability with Blackfire.io](https://docs.platform.sh/integrations/observability/blackfire.html)
- [Pricing](https://docs.platform.sh/overview/pricing.html)
- [Security and compliance](https://docs.platform.sh/security.html)


## Learn

### Troubleshooting


<details>
<summary><strong>Accessing logs</strong></summary><br/>

After the environment has finished its deployment, you can investigate issues that occured on startup, `deploy` and `post_deploy` hooks, and generally at runtime using the CLI. Run the command:

```bash
platform ssh
```

If you are running the command outside of a local copy of the project, you will need to include the `-p` (project) and/or `-e` (environment) flags as well.
Once you have connected to the container, [logs](https://docs.platform.sh/development/logs.html#container-logs) are available within `/var/log/` for you to investigate.

</details>


<details>
<summary><strong>Rebuilding cache</strong></summary><br/>

You may run into a database error after installing Drupal on your production environment initially.
To fix, SSH into the application container (`platform ssh`) and rebuild the cache using Drush:

```bash
drush cache-rebuild
```

</details>


<details>
<summary><strong>Default <code>hash_salt</code> behavior</strong></summary><br/>

Drupal's [default settings set](https://github.com/drupal/drupal/blob/10.3.x/core/assets/scaffold/files/default.settings.php#L252) `hash_salt` to an empty string:

```php
$settings['hash_salt'] = '';
```

In the past, Platform.sh templates have overridden this value:

```php
$settings['hash_salt'] = $settings['hash_salt'] ?? $platformsh->projectEntropy;
```

This setting was insufficient to cover some user configurations - such as those cases when an application depends on a `Null` value for `hash_salt`.

Now, the setting looks like this in `settings.platformsh.php`:

```bash
$settings['hash_salt'] = empty($settings['hash_salt']) ? $platformsh->projectEntropy : $settings['hash_salt'];
```

This change sets `hash_salt` to the built-in environment variable `PLATFORM_PROJECT_ENTROPY` value if the project contains the default settings OR `Null`.
If your application code *depends* on an empty value, feel free to comment out that line, or reset again later in that file.

Feel free to visit [`platformsh-templates/drupal9#73`](https://github.com/platformsh-templates/drupal9/pull/73) for more details on this discussion.

</details>




### Blackfire.io: creating a Continuous Observability Strategy

This template includes a starting [`.blackfire.yml`](.blackfire.yml) file that can be used to enable [Application Performance Monitoring](https://blackfire.io/docs/monitoring-cookbooks/index), [Profiling](https://blackfire.io/docs/profiling-cookbooks/index), [Builds](https://blackfire.io/docs/builds-cookbooks/index) and [Performance Testing](https://blackfire.io/docs/testing-cookbooks/index) on your project. Platform.sh comes with Blackfire pre-installed on application containers, and [setting up requires minimal configuration](https://docs.platform.sh/integrations/observability/blackfire.html).

* [What is Blackfire?](https://blackfire.io/docs/introduction)
* [Configuring Blackfire.io on a Platform.sh project](https://docs.platform.sh/integrations/observability/blackfire.html)
* [Blackfire.io Platform.sh documentation](https://blackfire.io/docs/integrations/paas/platformsh)
* [Profiling Cookbooks](https://blackfire.io/docs/profiling-cookbooks/index)
* [Monitoring Cookbooks](https://blackfire.io/docs/monitoring-cookbooks/index)
* [Testing Cookbooks](https://blackfire.io/docs/testing-cookbooks/index)
* [Using Builds](https://blackfire.io/docs/builds-cookbooks/index)
* [Configuring Integrations](https://blackfire.io/docs/integrations/index)


### Resources


- [Drupal](https://www.drupal.org/)
- [Drupal 9 on Platform.sh](https://docs.platform.sh/guides/drupal9/deploy.html)
- [Platform.sh PHP documentation](https://docs.platform.sh/languages/php.html)



### Contact

This template is maintained by the Platform.sh Developer Relations team, and they will be notified of all issues and pull requests you open here.

- **Community:** Share your question with the community, or see if it's already been asked on our [Community site](https://community.platform.sh).
- **Slack:** If you haven't done so already, you can join Platform.sh's [public Slack](https://chat.platform.sh/) channels and ping the `@devrel_team` with any questions.


### About Platform.sh

This template has been specifically designed to deploy on Platform.sh.

<details>
<summary>What is Platform.sh?</summary><br/>

Platform.sh is a unified, secure, enterprise-grade platform for building, running and scaling web applications. We’re the leader in Fleet Ops: Everything you need to manage your fleet of websites and apps is available from the start. Because infrastructure and workflows are handled from the start, apps just work, so teams can focus on what really matters: making faster changes, collaborating confidently, and scaling responsibly. Whether managing a fleet of ten or ten thousand sites and apps, Platform.sh is the Developer- preferred solution that scales right.

Our key features include:

* **GitOps: Git as the source of truth**

    Every branch becomes a development environment, and nothing can change without a commit.

* **Batteries included: Managed infrastructure**

    [Simple abstraction in YAML](https://docs.platform.sh/configuration/yaml.html) for [committing and configuring infrastructure](https://docs.platform.sh/overview/structure.html), fully managed patch updates, and 24 [runtimes](https://docs.platform.sh/languages.html) & [services](https://docs.platform.sh/configuration/services.html) that can be added with a single line of code.

* **Instant cloning: Branch, merge, repeat**

    [Reusable builds](https://docs.platform.sh/overview/build-deploy.html) and automatically inherited production data provide true staging environments - experiment in isolation, test, then destroy or merge.

* **FleetOps: Fleet management platform**

    Leverage our public API along with custom tools like [Source Operations](https://docs.platform.sh/configuration/app/source-operations.html) and [Activity Scripts](https://docs.platform.sh/integrations/activity.html) to [manage thousands of applications](https://youtu.be/MILHG9OqhmE) - their dependency updates, fresh content, and upstream code.


To find out more, check out the demo below and go to our [website](https://platform.sh/product/).

<br/>
<p align="center">
<a href="https://platform.sh/demo/"><img src="https://img.youtube.com/vi/ny2YeD6Qt3M/0.jpg" alt="The Platform.sh demo"></a>
</p>


</details>



## Contribute

<h3 align="center">Help us keep top-notch templates!</h3>

Every one of our templates is open source, and they're important resources for users trying to deploy to Platform.sh for the first time or better understand the platform. They act as getting started guides, but also contain a number of helpful tips and best practices when working with certain languages and frameworks.

See something that's wrong with this template that needs to be fixed? Something in the documentation unclear or missing? Let us know!

<p align="center">
<strong>How to contribute</strong>
<br /><br />
<a href="https://github.com/platformsh-templates/drupal10/issues/new?assignees=&labels=bug&template=bug_report.yml"><strong>Report a bug</strong></a>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
<a href="https://github.com/platformsh-templates/drupal10/issues/new?assignees=&labels=feature+request&template=improvements.yml"><strong>Submit a feature request</strong></a>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
<a href="https://github.com/platformsh-templates/drupal10/pulls"><strong>Open a pull request</strong></a>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
<br />
</p>
<br />
<p align="center">
<strong>Need help?</strong>
<br /><br />
<a href="https://community.platform.sh"><strong>Ask the Platform.sh Community</strong></a>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
<a href="https://chat.platform.sh"><strong>Join us on Slack</strong></a>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
<br />
</p>
<br />
<h3 align="center"><strong>Thanks to all of our amazing contributors!</strong></h3>
<br/>
<p align="center">
<a href="https://github.com/platformsh-templates/drupal10/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=platformsh-templates/drupal10" />
</a>
</p>

<p align="center">
<em>Made with <a href="https://contrib.rocks">contrib.rocks</a><em>
</p>

<br />
