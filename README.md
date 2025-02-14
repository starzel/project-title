# Project Title 🚀

[![Built with Cookieplone](https://img.shields.io/badge/built%20with-Cookieplone-0083be.svg?logo=cookiecutter)](https://github.com/plone/cookiecutter-plone/)
[![Black code style](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/ambv/black)
[![Backend Tests](https://github.com/starzel/project-title/actions/workflows/backend.yml/badge.svg)](https://github.com/starzel/project-title/actions/workflows/backend.yml)

A new project using Plone 6.

## Quick Start 🏁

### Prerequisites ✅

Ensure you have the following installed:

- Python 3.11 🐍
- Docker 🐳

### Installation 🔧

1. Clone the repository:

```shell
git clone git@github.com:starzel/project-title.git
cd project-title
```

2. Install Backend:

```shell
make install
```

### Fire Up the Servers 🔥

1. Create a new Plone site on your first run:

```shell
make backend-create-site
```

2. Start the Backend at [http://localhost:8080/](http://localhost:8080/):

```shell
make backend-start
```

Voila! Your Plone site should be live and kicking! 🎉

### Local Stack Deployment 📦

Deploy a local `Docker Compose` environment that includes:

- Docker image for Backend 🖼️
- A stack with a Traefik router and a Postgres database 🗃️
- Accessible at [http://project-title.localhost](http://project-title.localhost) 🌐

Execute the following:

```shell
make stack-start
make stack-create-site
```

And... you're all set! Your Plone site is up and running locally! 🚀

## Project Structure 🏗️

This monorepo consists of two distinct sections: `backend` and `devops`.

- **backend**: Houses Plone installation, utilizing pip instead of buildout, and includes a policy package named project.title.
- **devops**: Encompasses Docker Stack, Ansible playbooks, and Cache settings.

### Why This Structure? 🤔

- All necessary codebases to run the site are contained within the repo (excluding existing addons for Plone).
- Specific GitHub Workflows are triggered based on changes in each codebase (refer to .github/workflows).
- Simplifies the creation of Docker images for each codebase.
- Demonstrates Plone installation/setup without buildout.

## Code Quality Assurance 🧐

To automatically format your code and ensure it adheres to quality standards, execute:

```shell
make check
```

Linters can be run within the `backend` folder.

## Internationalization 🌐

Generate translation files for Plone with ease:

```shell
make i18n
```

## Credits and Acknowledgements 🙏

Generated using [Cookieplone (0.8.3)](https://github.com/plone/cookieplone) and [cookiecutter-plone (0013aea)](https://github.com/plone/cookiecutter-plone/commit/0013aea5be919b08d2856b3fb93425d5befdb190) on 2025-02-14 14:34:53.158773. A special thanks to all contributors and supporters!
