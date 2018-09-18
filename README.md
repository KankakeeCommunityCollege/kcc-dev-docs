# KCC Web Development - Site Template Documentation
#### Jekyll + Gulp + Sass + Browsersync + Travis CI + . . .

## [View This README](https://kankakeecommunitycollege.github.io/kcc-dev-docs/) as a styled page.

- Jekyll static site generator
- Gulp.js with Modular gulp-tasks
- YAML Gulp config file
- Modular Sass
- Browsersync for live previewing
- Travis CI for continuous integration

Documentation for the Jekyll/Gulp template used to build KCC's new websites.  Visual styling of the sites are based off of design mockups.

## Contents:

1. [Requirements](https://github.com/wdzajicek/kcc-dev-docs#requirements)
  - [Mac](https://github.com/wdzajicek/kcc-dev-docs#mac):
    - [RVM](https://github.com/wdzajicek/kcc-dev-docs#1-rvm-using-ruby-250----httpsrvmiorvminstall):
      - [Installation](https://github.com/wdzajicek/kcc-dev-docs#1-rvm-using-ruby-250----httpsrvmiorvminstall)
      - [Install ruby-2.5.0](https://github.com/wdzajicek/kcc-dev-docs#1-rvm-using-ruby-250----httpsrvmiorvminstall)
      - [Set ruby-2.5.0 as default](https://github.com/wdzajicek/kcc-dev-docs#1-rvm-using-ruby-250----httpsrvmiorvminstall)
    - [NVM](https://github.com/wdzajicek/kcc-dev-docs#2-nvm-using-node-version-961---httpsgithubcomcreationixnvm):
      - [Installation](https://github.com/wdzajicek/kcc-dev-docs#2-nvm-using-node-version-961---httpsgithubcomcreationixnvm)
      - [Install Node Version 9.6.1](https://github.com/wdzajicek/kcc-dev-docs#2-nvm-using-node-version-961---httpsgithubcomcreationixnvm)
    - [NPM 6.1.0](https://github.com/wdzajicek/kcc-dev-docs#3-npm-version-610)
    - [Jekyll](https://github.com/wdzajicek/kcc-dev-docs#4-jekyll-and-bundler---httpsjekyllrbcomdocsinstallation)
    - [Gulp](https://github.com/wdzajicek/kcc-dev-docs#6-gulp---httpsgulpjscom)
  - [Windows PC](https://github.com/wdzajicek/kcc-dev-docs#windows-pc):
    - [Enable "Windows Subsystem for Linux"](https://github.com/wdzajicek/kcc-dev-docs#1-install-the-windows-subsystem-for-linux---run-in-powershell-as-administrator)
    - [Install Ubuntu in the Microsoft Store](https://github.com/wdzajicek/kcc-dev-docs#2-install-ubuntu-in-the-microsoft-store)
    - [Git SCM](https://github.com/wdzajicek/kcc-dev-docs#3-git-scm---httpsgit-scmcom)
    - [RVM](https://github.com/wdzajicek/kcc-dev-docs#4-rvm-using-ruby-250----httpsrvmiorvminstall):
      - [Installation](https://github.com/wdzajicek/kcc-dev-docs#4-rvm-using-ruby-250----httpsrvmiorvminstall)
      - [Install ruby-2.5.0](https://github.com/wdzajicek/kcc-dev-docs#4-rvm-using-ruby-250----httpsrvmiorvminstall)
      - [Set ruby-2.5.0 as default](https://github.com/wdzajicek/kcc-dev-docs#4-rvm-using-ruby-250----httpsrvmiorvminstall)
    - [NVM](https://github.com/wdzajicek/kcc-dev-docs#5-nvm-using-node-version-961---httpsgithubcomcreationixnvm):
      - [Installation](https://github.com/wdzajicek/kcc-dev-docs#5-nvm-using-node-version-961---httpsgithubcomcreationixnvm)
      - [Install Node Version 9.6.1](https://github.com/wdzajicek/kcc-dev-docs#5-nvm-using-node-version-961---httpsgithubcomcreationixnvm)
    - [NPM 6.1.0](https://github.com/wdzajicek/kcc-dev-docs#6-npm-version-610)
    - [Jekyll](https://github.com/wdzajicek/kcc-dev-docs#7-jekyll-and-bundler---httpsjekyllrbcomdocsinstallation)
    - [Travis-CLI](https://github.com/wdzajicek/kcc-dev-docs#8-travis-cli---httpsdocstravis-cicomuserencryption-keysstqstp0)
    - [Gulp](https://github.com/wdzajicek/kcc-dev-docs#9-gulp---httpsgulpjscom)
2. [Local Installation](https://github.com/wdzajicek/kcc-dev-docs#local-installation)
	- [install.sh](https://github.com/wdzajicek/kcc-dev-docs#local-installation)
		- [Gemfile](https://github.com/wdzajicek/kcc-dev-docs#local-installation)
		- [Bundle install](https://github.com/wdzajicek/kcc-dev-docs#local-installation)
		- [npm install](https://github.com/wdzajicek/kcc-dev-docs#local-installation)
3. [Development](https://github.com/wdzajicek/kcc-dev-docs#development)
    - [The build](https://github.com/wdzajicek/kcc-dev-docs#development)
    - [Browsersync](https://github.com/wdzajicek/kcc-dev-docs#development)
    - [watch](https://github.com/wdzajicek/kcc-dev-docs#watch)
3. [Travis CI](https://github.com/wdzajicek/kcc-dev-docs#travis-ci)
  - [Travis Configuration File](https://github.com/wdzajicek/kcc-dev-docs#travis-configuration-file-travisyml):
    - [before_install](https://github.com/wdzajicek/kcc-dev-docs#before_install)
    - [install](https://github.com/wdzajicek/kcc-dev-docs#install)
    - [Branches](https://github.com/wdzajicek/kcc-dev-docs#branches)
    - [Notifications](https://github.com/wdzajicek/kcc-dev-docs#notification-settings-with-encrypted-emails)
    - [before_script](https://github.com/wdzajicek/kcc-dev-docs#before_script)
    - [script](https://github.com/wdzajicek/kcc-dev-docs#script)
    - [after_success](https://github.com/wdzajicek/kcc-dev-docs#after_succes)
    - [Global Environment Variables](https://github.com/wdzajicek/kcc-dev-docs#global-environment-variables)
  - [Encrypting Using Travis CLI](https://github.com/wdzajicek/kcc-dev-docs#encrypting-using-travis-cli)
  - [Encrypting Notification emails](https://github.com/wdzajicek/kcc-dev-docs#encrypting-notification-emails)
  - [Encrypting and Calling Environment Variables](https://github.com/wdzajicek/kcc-dev-docs#encrypting-and-calling-environment-variables)

## Requirements

<span style="float: right; position: relative; top: -4rem;"><a href="https://github.com/wdzajicek/kcc-dev-docs#contents">Contents</a></span>

Prerequisites to run site builds on a local machine.

### Mac

Prerequisites: Latest Xcode for your OS<br>
Install in the following order:

##### 1. RVM using ruby-2.5.0  - <https://rvm.io/rvm/install>

		# Install public key
		$ gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB

		# Install RVM stable with ruby
		$ \curl -sSL https://get.rvm.io | bash -s stable --ruby

		# Install ruby-2.5.0
		$ rvm install 2.5.0

		# Set ruby-2.5.0 as Default Ruby Version
		$ rvm --default use 2.5.0

##### 2. NVM using Node version 9.6.1 - <https://github.com/creationix/nvm>

		# Use the install script
		$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash

		# Close all terminal windows and test nvm
		$ command -v nvm
		# Should return 'nvm'

		# Install Node version 9.6.1 and set it as default
		$ nvm install 9.6.1
		$ nvm alias default 9.6.1

##### 3. NPM Version 6.1.0

		$ npm i -g npm@6.1.0

##### 4. Jekyll and Bundler - <https://jekyllrb.com/docs/installation/>

		$ gem install jekyll
		$ gem install bundler

##### 5. Travis CLI - https://docs.travis-ci.com/user/encryption-keys/#stq=&stp=0

		$ gem install travis

##### 6. Gulp - https://gulpjs.com/

		$ npm install gulp-cli -g

<br>
<hr>
<br>

### Windows PC

<span style="float: right; position: relative; top: -4rem;"><a href="https://github.com/wdzajicek/kcc-dev-docs#contents">Contents</a></span>

Prerequisites: Windows 10 PC running newest Windows Build Version<br>
Install in the following order:

##### 1. Install the Windows Subsystem for Linux - Run in PowerShell as Administrator:

		Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

		# Restart when prompted

##### 2. Install Ubuntu in the Microsoft Store

	- Open Microsoft Store App
	- Search "ubuntu"
	- Click "Get" button on Ubuntu page
	- Run Ubuntu from Start menu after install
	- Follow prompts and create Unix User/Password
	- After first run test by opening and cmd.exe program as admin and running `$ bash`
	- You should be able to call a `$ bash` shell session from any command line

##### 3. Git SCM - <https://git-scm.com/>

	- Use installer at <https://git-scm.com/>
	- Install using default settings (however, I set default text editor to nano)

##### 4. RVM using ruby-2.5.0  - <https://rvm.io/rvm/install>

		# Install public key
		$ gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB

		# Install RVM stable with ruby
		$ \curl -sSL https://get.rvm.io | bash -s stable --ruby

		# Install ruby-2.5.0
		$ rvm install 2.5.0

		# Set ruby-2.5.0 as Default Ruby Version
		$ rvm --default use 2.5.0

##### 5. NVM using Node version 9.6.1 - <https://github.com/creationix/nvm>

		# Use the install script
		$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash

		# Close all terminal windows and test nvm
		$ command -v nvm
		# Should return 'nvm'

		# Install Node version 9.6.1 and set it as default
		$ nvm install 9.6.1
		$ nvm alias default 9.6.1

##### 6. NPM Version 6.1.0

		$ npm i -g npm@6.1.0

##### 7. Jekyll and Bundler - <https://jekyllrb.com/docs/installation/>

		$ gem install jekyll
		$ gem install bundler

##### 8. Travis CLI - https://docs.travis-ci.com/user/encryption-keys/#stq=&stp=0

			$ gem install travis

##### 9. Gulp - https://gulpjs.com/

		$ npm install gulp-cli -g

<br>
<hr>
<br>

## Local Installation

<a href="https://github.com/wdzajicek/kcc-dev-docs#contents" style="float: right; position: relative; top: -4.5rem;">Contents</a>

To install the project on your local machine:

1. Clone the Repository:

		$ git clone https://github.com/KankakeeCommunityCollege/kcc-startup-template.git <project name>

2. Run the "install.sh" shell script within the cloned repository:

		$ cd <project name>
		$ sh install.sh

> ***What does the install.sh script do?***
> 1. Create a Gemfile from Gemfile.txt
> 2. NPM install
> 3. Bundle install
> 4. Remove remote "origin" to prevent overwriting of the template in Github
>
> 	**Running the following commands will produce the same results as running install.sh:**
>		 $ cp Gemfile.txt gemfile
>		 $ npm install
>		 $ bundle install
>		 $ git remote remove origin

<br>
<hr>
<br>

## Development

<a href="https://github.com/wdzajicek/kcc-dev-docs#contents" style="float: right; position: relative; top: -4.5rem;">Contents</a>

For development of sites run the default gulp task:

	$ gulp

> The default gulp task consists of 3 main parts:
>
> 1. The build
> 2. Browsersync
> 3. watch

**1. The Build:**

The "build" gulp task cleans the _site/ dir, runs the Jekyll site build, creates the sitemap, compiles the Sass and JavaScript and copies static assets like images.

	gulp.task('build', function(done) {
		sequence( 'clean', 'jekyll-build', 'sitemap', ['sass', 'contentSass', 'javascript'], 'copy', done);
	});

**2. Browsersync**

Starts Browsersync for injecting changes into browser during development (live preview)

**3. watch**

Watch the project files for changes to be injected into the browser via Browsersync

<br>
<hr>
<br>

## Production

<a href="https://github.com/wdzajicek/kcc-dev-docs#contents" style="float: right; position: relative; top: -4.5rem;">Contents</a>

> Production build minifies CSS and JavaScript and compresses image files.
>
> A gulp production build should be run before committing and pushing any CSS, JS, or new images to the Github repository.
>
>Trying to push non-minified CSS and JS may result in merge conflicts.  If you have a merge conflict, especially on main.css or all.min.js, try running `$ gulp --production` before trying to push again

	$ gulp --production

## The gulpfile.js and gulpconfig.yml

See the comments within gulpfile.js and gulpconfig.yml for detailed explanation of what happens on running `$ gulp` or `$ gulp --production`

<br>
<hr>
<br>

## Travis CI

<a href="https://github.com/wdzajicek/kcc-dev-docs#contents" style="float: right; position: relative; top: -4.5rem;">Contents</a>

### Travis Configuration File (.travis.yml)

Same ruby version as local dev environment

    language: ruby
    rvm:
    - 2.5.0
    sudo: false
    addons:
    apt:
      packages:
      - ncftp

#### before_install:

gemfile.sh Creates the Gemfile for travis to use. Install npm v6.1.0:

    before_install:
    - chmod +x _scripts/gemfile.sh
    - _scripts/gemfile.sh
    - npm i -g npm@6.1.0

#### install:

npm install, bundle install, jekyll gem installs:

    install:
    - npm install
    - bundle install
    - gem install jekyll
    - gem install jekyll-feed
    - gem install jekyll-sitemap

#### Defining Branches

With CloudCannon's publishing workflow, the publish branch is the only one  that gets built.

    branches:
    only:
    - publish

#### Notification settings with encrypted emails

##### See [Encrypting Notification Emails](https://github.com/wdzajicek/kcc-dev-docs#encrypting-and-calling-environment-variables)

    notifications:
    email:
      recipients:
      - secure: gK8tke5tvf+kn0QCQz8mBdEKDcxgtOKHSkS55k6GGSyGOSBh0wlWVYP0S3pgmJ9zGu6y6y0gBkwhA12t3SbhMXEPeKUnAdBJrss+MJdHk6Z3mhb9BhO/kyKxhkS+oTYrTBXndINEVa0JKrpwVcE3s9b+PWn7B59jKWrcXiZ4a7BMgfyXM+pKi+sJwRnRGBDsa2kbBz1S7slkb1P7t8xN+/JTM+vArHn0Pb0cXmfeW4/9llqTMMHkuscULDrcnkhgQuHWXi4SX9kk42dj9+ga2tI1vkfSuUg0m3BKc3N+wNkPt9NJoXXEJbkfbrOkKKJ8tbKHooi1bNbcwlI9Axmu5QTWQkwCAEtvbbroXch2zzEIg3gOuaFxbCwRjEUEkHP5jWLgIA4gH70ZRgRLEL31AkoRXXgZMjKvHV/IhonGzAz25jdRPf6uReMGnjwjyDDLTSSacI0yAwSI8No4MDMs3VuXRP9+6pbg01bwOc1DijTbpfu0zKHuOm2jSTErZdhNPDA2m673lbyt4AbqGqXWigWFAPLnB5SBNS63O7IluYu8SwS0rh6oQppsJF6RNB7EQ4VSuvYYJ2a0NZbT7QZ47hJrbkNFfBsa+vBXKYtZZ2gaBqGGkGNA7VGhob2Hd8Y0GKl0gEBRH7UgpxRhpw3IMwE/1Csn8mYxKhlEXm5wi/c=
      - secure: ThPSgqgVNLGilY8sUdKvEQmGuQocuoVuoRYdjaH6pojpsREXlNb5Yv8MlWLWRTY+JvhZcFAmE+B4e5lUT6PCgKoeidM94tzhuRj+wI3c88Y+HHe6P1p+hnQH5aVGNQTchxLF3Bdio412d2KLqhvO1+fWGLIsw12EuoMezGsuCfOCkR3fR2G7dn7IKiJEtwluee4eY59bPI90ucYRTJdZAHYg13JsBWo+D40hpuPYnqJNAk8uM9XQVGoYU4VWclFm1gfok3hzhIgncgxdIyuDy73f6WZ9hnvv73eo0FJUrn9CPAve+fNhOElpqtBCZlSU7Axe8NyDZZDcXAvakLqCPWmlwgu+UuwoVPaYQNyrzSIePT18tocSa4UYBtXu46kryT4g0oD6CQmZ5tcXcqGQi3K+2OmJjYvy9TeCde3YERRVX8JEudTBkNLccJaSpxr6grIP/+LIyBsnAbKFeq2yrXYCnRmA1iyD603vaed8y37uufH3WGAjZgRVN5dAo0P5feJ1EH9GuTH1YXw44yKcymYtBNX+sgm0MBZTZMCw2metm+JB6Jc3ji4qGxd3Fpe2CtcOLasPZzU0ifvUTpiqaA9/LqeHRev2i/cXxaxvXdbpRWpVzkVKfFkSFDjqQqJUZ2Z52ATD0/qJ/k20+dC2X318HPtI60AKyfUs61ydaho=
      - secure: IOJLMgek9M6Irp3WsTyuDTGzia29Vs0zWzqNg6kGS2oqQAwwdiVATND+2OwYt+zXieS6/0qJm5gq8gQbFohlmqDQ6utLuugvKi6B22DT5yQGzkeMCr5wNlrag11jFS1uULPhRApwCz5ThnYY33Oiaac4csCBNZ5YMpb4pIQugSBkyFob2oMMZlegL/2yXOtjhLkYJxQvJ5D2zpl+3oQFgmHo7n6XY0c0lJY2bFs9ehY2aXGiTw1WheLDiMMoraCSXxSrYskPOzp7c6ywg1CsdnZAy3IxJaCWEDCBEGmgh2Ljnlh0lTeWYIgow4L8TWOYYrQeU8IolfHRlx1hgCTKmildsyVrTmtLbuKVaUYzvYnuZmlHWF4d+OEkW1RCTmx3gb7iQUEZu28QsCHOgFRZPpI8Um+1ApXM3JcJI4r7zF+qduyLkRR6mdYHTDplhs/nttZYlsWGOkQnqIiJWmPQUeYgSuQgz+3sSnVmA8kNEcPlolH7U+299aL7yAw9z/khNLhErsAYqUI/35E3kecIZeLVFfCKFF1pTQedNCxhxu3lgHNROLu0Q7nXxgrpC2OGBoaR9dwvkdS9MW2Lnh8rK9lGeMvcRjhJsXfkhyJaPgJWa99O9vNUbLK9FHU/qlrM1cvhxd+Ch8QRat3PF3wv+sPZFEYjhb32pVCXukl7I0w=
      on_success: never
      on_failure: always

#### before_script:

###### install Gulp.js

    before_script:
    - npm install -g gulp-cli

#### script:

###### The build script: `$ gulp travis`

the "travis" gulp task creates a production build of the site (production uses asset minification i.e. images, JS, & CSS minified/uglified/compressed.

    script:
    - chmod +x _scripts/build.sh
    - _scripts/build.sh

#### after_succes:


###### Deploy!

deploy.sh runs two gulp tasks: cleanFTP and newerFTP. cleanFTP deletes everything from the server folder and newerFTP copies the new passing site build to the server.

deploy.sh also issues a 15 second delay via `$ sleep 15` between the cleanFTP and newerFTP tasks.

    after_success:
    - chmod +x _scripts/deploy.sh
    - _scripts/deploy.sh

#### Global Environment Variables

##### See [Encrypting and Calling Environment Variables](https://github.com/wdzajicek/kcc-dev-docs#encrypting-and-calling-environment-variables).

    env:
    global:
    - secure: UXS4WAMKaUFb/WIv0bam2q7T36hNXKTgUVeWSSISyxkU+Rvd5rDpkLNNC21N7NqNBF1DHUPhBMpwoYKjvTVbUfgsF7bBPLOTPAvz9Fyl7kJjkVTzk+usqFOxm5vYiJrogBro1BH7ZJKMmEqrzYIJtw+2KIvE826E6kxMAVyOHMeRiPXHH8fz2mNoE6D9hYgAL2pOOPFZ6VKQOHWqWSimXGEPH0M2vMp8MO5NFlu3rLJs/30LdeUM7evOOzl1iftLYqNgt9H56jlY0ztjYWOsSr6tIYfpWyKcSgSA5ZnAnP3MVDS3/ym5xOfSe7vNfDuGfbBKYBx9NKlwL6MVAFMsqJyBIz14wjvBT1cl6YHh8o+2su3gUvsn6uDIDk7m2T3WPXylN9/+jNvvzN2Cvi2QeSi/m/jZKBfrH6bL+4KAklpgRl69oek891Zfwln1Yu87bWXsHuT7nXcw+gGHg4xifbQu95RRlMYyhTnMZKC0UwTBwUK7uLsH3/GnwLh9Mzi8Hg4NLMMZIZ5kn2eIeb691Y84she/ZwNuvuHM6ThFWm+L9vT7CBkZP5oKJRRVOvgunv0uh1UpybSsdcyLnyx1mbEW/8X0q3zTvSa2euUsFHkBlfNefr4Q26b+93pS5di6ufpGRBuVrBQKHZdsjJD6FVPZg2oOI1vCgyZsWZO0DM4=
    - secure: J5PE3reG8l3IOyFKxqmRpVdiGwa5Uc8uo5ksJptBDB/8Bju/Y+mlbZy6ELIE+nQcFMo0WqBx59qY5h8PPG2NeLBlpkgPWiKecxiOBIHR4WwPV2EFcBvcFwM++k4YcQpB/bghZP5OzzNO1psOnoNM/V3DNgsy1V8BmsnmqpkF1Y3aQZfsIKwpITFaUFhX/9k29l5dQqS4cWJKktUjei3HNhYB6zst2K5cWxqagTbB2PjPWTIw1uQzQR4PR1XZ0gPq5R8KpI2Rey4HAucDnesgBxSSgoo3DppHGId8NdXGVh4CxIHowv6PGZtZ5sF/Q7WZcwbSMDstf+ZZ3A4jcJyReadZUsRnE+H+YPrXIS8GwJZ6c0E9s8hN+1lkEog0gzT0sskD4Psv4Yk2NuP+zrNsfxwf9hrNWlOIM2eTF+5LFr5TlwHHKvkByGxfpkePTQBYc1g02EDxzSQnx/nEqL+c0e2lMskT0adTU/lbUkqtsTD4taxAEyZbAseJ0dkIwl4oPSaLwwpMlMcSy7H4SiJzWpI+sU+XNCyg25oDKn3KjcQIzZC5jce1EtgnKY/Ww1FTPI4tPM2r0mq7TnYOI44cH91TiHlMOg/jOBRSmtlhMHcr6Scsy4LegOfAVlj67x+mEvT/GOzbheLS+QtqmU2XFELWS9KHA+N/C6XGkrqXCzE=
    - secure: ldvzd3QRFAcq/dGFwJHG+EUbmTM88HV3Ou7GHkS5rINCCZz1GXGMHJ2Il9SvpMIorEyy//p7qieaFG+3r+L1DpthLQBKEY5GEPlAgKjeduDQ1wjbWjXJ1llc0B39tZmMXu9xNRoLMjLqtvAl/IgUhCCnl4vvCrMJFtXzzA73HNz9XzFRhhaUF+UXPmGGrj+ABX9C4/ODUsZdFLox0kMiR/wjqkf4TDhLPszQuP49H9OQBqdfc9/7QCnLPYt77gPcpo6FLphdnyufCzdNrectGnU2HM7lStVGtP81EjkR04XjKF+XvBbWuk689kTBPNC1f3R1FcRFds7xXnKlAoTxrFO7Zd47K9GxiAUtG2xInbugHYcY/KN9lA0F35FFdbaksVPiMEYPlHMSKqPSJrviG58jGBhZiQXsAKU1psahLZKAayKeAkDAdWS2P42tNzG5817NSFT9DdWnUrGKgimuescXsuJ5E5J0Y9Dqg5tCi3CgKlU9E0pQEWqaILM0ZS5Vx1rvuZiYnTUWqefdVRrWZ3Z0c9itdu8hJOuBzLBVzzzk9eCkhdS+vVo+dMIpt1ecxX2qpRVUWJvxJ19CDgJPQL7pUb3T09MXx5r3atePwMrKcK18WGFV+PuPVYPPmxsjUXIpg4+/M2cRaRypwU+beENvXycO42+7I+nFzlxF6zA=

<br>
<hr>
<br>

## Encrypting Using Travis CLI

<a href="https://github.com/wdzajicek/kcc-dev-docs#contents" style="float: right; position: relative; top: -4.5rem;">Contents</a>

to encrypt travis variables use the travis gem and login using Github credentials (travis logins will timeout):

    $ gem install travis
    $ travis login            // this will prompt for Github user/password

> **Certain characters within a string to be encyrpted must be escaped:**<br>
> Any character that ***bash cannot parse*** without escaping must be escaped (e.g. braces, parentheses,  backslashes, and pipe symbols.)
>
> **To escape special characters in a string precede them with two backslashes ( \\\ ).**<br>
> You are essentially escaping the escape for any special characters.

To encrypt the string `4!4(2&^2\` you must escape `!`, `(`, `&`, `^`, and `\`

    $ travis encrypt "4\\!4\\(2\\&\\^2\\\\"

> That way, when you enter the command `$ travis encrypt "4\\!4\\(2\\&\\^2\\\\"` travis is actually encrypting the string `4\!4\(2\&\^2\\`.
>
>  **This is needed so that, when travis decrypts this string and uses it, all the special characters within the string have already been escaped.**

For example, to encrypt `www.url.com|ftp_user` you would have to escape the pipe ( | ) symbol

    $ travis encrypt "www.url.com\\|ftp_user"

<br>
<hr>
<br>

## Encrypting Notification emails

<a href="https://github.com/wdzajicek/kcc-dev-docs#contents" style="float: right; position: relative; top: -4.5rem;">Contents</a>

#### Default notification email example in .travis.yml.

This is how standard email notifications are set in .travis.yml without encryption:

    notifications:
    email:
      recipients:
        - <recipient-1>@gmail.com
        - <recipient-2>@gmail.com

#### To encrypt an email.

You must be in a local git repository that travis-ci.org has access to.

    $ travis encrypt "<recipient-1>@gmail.com"

Travis will return something like this:

    Please add the following to your .travis.yml file:

      secure: "XDD3KrR1M5Xmg+wlea4y1o14uhIhV78yAUA96SaQT4KKBRXqixQbo+Mme4ghIRlWyuZ35BReL6h/MO2Gr3xJ1TEsmo/7d+aP+OazwJ4weGX7YEQYuE7RGKQt4LIENQVhbJmUspzoZl/bocas+2PaiS8LT4cKJ58l35kFW4fIONPir4M/4xUqJX5kxvUqww7K+ijipJYAcO2ySeFeMbPL5sMxezBaXNg1sG44s/4RmHJ9tpLlnLJc1X1n0OdxrNPI2KpEQWIyTdve7vtUZb7FJ0UefL1ll9C4fojhIp8Fb3IzS5W3hLiBTys56OvhEcgp0SejCrTD9guxrwJxrZPy5i2T4Ahjg2H7ej7QsvBqh3kIfxKzKFLVvp9jKfiE0zI+lTHWhKcGXHRZTP5qLtAgEaVyKiEVd1wgwrbnv+JPLRT7Gr4CIb9BtTZjPyqAErC1uVcvapvzR19EoIAC+/Z5cyQlkZkXeLx+5c1675WoHae92MzE8xr2lf5t9b9CVk1Hdd47qaoRz172ikddcWOO242v6orxh0QT0ar65L9DqMQ+7IZP+95wn/fd97Et7zMLpkVrzaj8kSUDAi2QvhhSunBCwToe8czAUwZQ160BTicCIZ8LZpjeqZXTvEBGdqgT3Df7dNrsbODY/XiVLmpIHRaUPlcJWiwIjD2WCuGqMAg="

#### Copy and paste into .travis.yml

Replace `- <recipient-1>@gmail.com` with `- secure: <long encrypted string>`:

    notifications:
    email:
      recipients:
        - secure: "XDD3KrR1M5Xmg+wlea4y1o14uhIhV78yAUA96SaQT4KKBRXqixQbo+Mme4ghIRlWyuZ35BReL6h/MO2Gr3xJ1TEsmo/7d+aP+OazwJ4weGX7YEQYuE7RGKQt4LIENQVhbJmUspzoZl/bocas+2PaiS8LT4cKJ58l35kFW4fIONPir4M/4xUqJX5kxvUqww7K+ijipJYAcO2ySeFeMbPL5sMxezBaXNg1sG44s/4RmHJ9tpLlnLJc1X1n0OdxrNPI2KpEQWIyTdve7vtUZb7FJ0UefL1ll9C4fojhIp8Fb3IzS5W3hLiBTys56OvhEcgp0SejCrTD9guxrwJxrZPy5i2T4Ahjg2H7ej7QsvBqh3kIfxKzKFLVvp9jKfiE0zI+lTHWhKcGXHRZTP5qLtAgEaVyKiEVd1wgwrbnv+JPLRT7Gr4CIb9BtTZjPyqAErC1uVcvapvzR19EoIAC+/Z5cyQlkZkXeLx+5c1675WoHae92MzE8xr2lf5t9b9CVk1Hdd47qaoRz172ikddcWOO242v6orxh0QT0ar65L9DqMQ+7IZP+95wn/fd97Et7zMLpkVrzaj8kSUDAi2QvhhSunBCwToe8czAUwZQ160BTicCIZ8LZpjeqZXTvEBGdqgT3Df7dNrsbODY/XiVLmpIHRaUPlcJWiwIjD2WCuGqMAg="
        - <recipient-2>@gmail.com

##### Travis can now decrypt your email and send you notifications without making your email publicly available.

<br>
<hr>
<br>

## Encrypting and Calling Environment Variables

<a href="https://github.com/wdzajicek/kcc-dev-docs#contents" style="float: right; position: relative; top: -4.5rem;">Contents</a>

to encrypt travis variables use the travis gem and login using Github credentials. You must be in a local git repository that travis-ci.org has access to.

    $ gem install travis
    $ travis login            // this will prompt for Github user/password

##### Encrypting Environment Variables and writing to .travis.yml at the same time:

If I wanted to put an FTP username and password in my .travis.yml as an encrypted environment variable. The `--add` flag writes the encrypted string to your .travis.yml file:

    $ travis encrypt FTP_USER="<example user>" --add
    $ travis encrypt FTP_PASSWORD="<example password>" --add

Travis now has access to those encrypted variables. For example you could call the FTP user and password in your deploy script use the dollar-sign followed by the variables name (e.g. `$FTP_USER`)

Example in a deploy.sh file used by travis:


    $ gulp deploy --user $FTP_USER --password $FTP_PASSWORD

<br>
<hr>
<br>

<span style="float: right;"><a href="https://github.com/wdzajicek/kcc-dev-docs#contents">Contents</a></span>
