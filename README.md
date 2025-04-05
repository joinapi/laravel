# JOINAPI - Laravel ( Larament based )

## Table of Contents

- [Features](#features)
  - [Security and Testing](#security-and-testing)
  - [Quality of Life](#quality-of-life)
  - [Design](#design)
- [Default User](#default-user)
- [Included Packages](#included-packages)
- [Installation](#installation)
  - [CLI Installation](#cli-installation)

---

## Features

### Security and Testing

- **PESTPHP**: Preconfigured with test cases for streamlined testing. ([Learn more](https://pestphp.com/docs/installation))
- **Strict mode enabled** via [Should Be Strict](https://laravel-news.com/shouldbestrict):
  - Prevents lazy loading (N+1 queries).
  - Guards against discarding or accessing missing attributes.
- **Production safeguards**: Prevents destructive commands in production. ([Learn more](https://laravel-news.com/prevent-destructive-commands-from-running-in-laravel-11))
- **Architectural testing** with Archtest.
- **Static analysis** using PHPStan.
- **Debugging** with Laravel Debugbar.

### Quality of Life

- Custom login page autofills email and password with seeded data for quicker testing.
- Built-in password generator action on the user profile and user resource pages.
- Enhanced global search includes email addresses for better discoverability.
- Auto-translatable component labels.
- `composer review`: A single command to run Pint, PHPStan, and PEST.
- Helper functions available through a dedicated helper file.
- Custom `php artisan make:filament-action` command for generating Filament actions.

### Design

- Filament Panel's primary color is preset to blue.
- Single Page Application (SPA) mode enabled by default.
- Global search keybinding set to `CTRL + K` or `CMD + K`.
- A ready-to-use FilamentPHP custom theme, including a sidebar separator.
- Enhanced profile page with a built-in password generator.

---

## Default User

A default user is seeded with the following credentials, pre-filled on the login page for quick access:

```dotenv
DEFAULT_USER_NAME="John Doe"
DEFAULT_USER_EMAIL="admin@example.com"
DEFAULT_USER_PASSWORD="password"
```

## Installation
### Using the Template
- Create a repository using the Larament template.
- Clone your repository to your local machine.
 Navigate to the project directory and run the following commands:
```bash
composer install
npm install && npm run build
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan db:seed
```

### CLI Installation
Alternatively, you can use the following command to create a new project with Larament:

```bash
composer create-project --prefer-dist joinapi/laravel example-app
```

### Create a Terminal Alias
For easier usage in future projects, create an alias in your terminal:

```bash
alias joinapp="composer create-project --prefer-dist joinapi/laravel"
```

Now, you can create a new project with a simple command:

```bash
joinapp my-cool-app
```
