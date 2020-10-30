# Table of Content

1. [Setup](#setup)
2. [Coding Standards / Style Guides](#coding-standards--style-guides)
3. [Connect MySQL to MySQL Workbench](#connect-mysql-to-mysql-workbench)
4. [Environment Variable](#environment-variable)

<br><br>

# Setup

1. Prerequisite
   - Docker must be installed and running
2. Clone this repo or download it as a Zip file
3. Rename `template-wordpress-docker-basic` folder with your project name
4. Remove/delete `.git`
5. Initialize Git

```
git init
```

5. Set MySQL [environment variables](#environment-variable)
6. Run Docker compose

```
docker-compose up -d
```

7. Verify site
   - Open the web browser, type `localhost:8000`, and press `Enter`
   - If everything worked as expected, the default WordPress theme will be displayed.

<br><br>

# Coding Standards / Style Guides

- Accessibility
  - [WordPress](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/accessibility/)
- Angular
  - [Google](https://google.github.io/styleguide/angularjs-google-style.html)
- CSS
  - [Airbnb](https://github.com/airbnb/css)
  - [Drupal](https://www.drupal.org/docs/develop/standards/css/css-formatting-guidelines)
  - [Google](https://google.github.io/styleguide/htmlcssguide.html)
  - [WordPress](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/css/)
- HTML
  - [GitLab](https://docs.gitlab.com/ee/development/fe_guide/style/html.html)
  - [Google](https://google.github.io/styleguide/htmlcssguide.html)
  - [WordPress](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/html/)
- JavaScript
  - [Airbnb](https://github.com/airbnb/javascript)
  - [GitLab](https://docs.gitlab.com/ee/development/fe_guide/style/javascript.html)
  - [Google](https://google.github.io/styleguide/jsguide.html)
  - [WordPress](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/javascript/)
- PHP
  - [WordPress](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/php/)
- React
  - [Airbnb](https://github.com/airbnb/javascript/tree/master/react)
- SCSS
  - [GitLab](https://docs.gitlab.com/ee/development/fe_guide/style/scss.html)
- Vue
  - [GitLab](https://docs.gitlab.com/ee/development/fe_guide/style/vue.html)

<br><br>

# Connect MySQL to MySQL Workbench

1. Prerequisite
   - MySQL Workbench must be installed
     - [Community Download](https://dev.mysql.com/downloads/workbench/)
     - [Donwloads](https://www.mysql.com/downloads/)
2. Open `MyQL Workbench`
3. On `MySQL Connections` window, click on the `plus icon` to create a new connection.
   - A dialog window will be displayed
4. Follow the table below to set the connection information
   |||
   | :---------------: | :-------------------------------------------------: |
   |Connection Name|Enter a unique name. Ex. `Docker-Local` |
   | Connection Method | Standard (TCP/IP) |
   | `Parameters Tab` | |
   | Hostname | 127.0.0.1 |
   | Port | 3306 |
   | Username | This will be the `MYSQL_USER` value from `.env` |
   | Password | This will be the `MYSQL_PASSWORD` value from `.env` |
5. Click on `Test Connection`
   - A successful message will be displayed if the connection has been established
6. Click on `OK`
   - The dialog window will close
7. Click on the `Connection Name` to open the server on a new tab
8. From this point on, you will be able to manage the project MySQL database through MySQL Workbench

<br><br>

# Environment Variable

1. Create a `.env` file in the root of this project
2. Add the information mentioned below to `.env` file

```
MYSQL_ROOT_PASSWORD=long-unique-random-password
MYSQL_USER=unique-username
MYSQL_PASSWORD=long-unique-random-password
```
