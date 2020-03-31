# COVID Self report

![CI](https://github.com/ch-covid-19/self-report-frontend/workflows/CI/badge.svg)

This repository hosts the frontend code of the covid-self-report project.

This project is based on [Vue.js](https://github.com/vuejs/) and vue-cli, using [Argon design template from Creative Tim](https://www.creative-tim.com/product/argon-design-system).

## Getting started

For front-end developers, please check the [develop section](#develop) section.

### Pre-requisite

The following things are needed:

- A domain name (e.g. covid-self-report.ch)
- A hosting server (we are using firebase, but it's not mandatory)
- An instance of [self-report-backend](https://github.com/ch-covid-19/self-report-backend) running (or develop your own backend)
- A reCAPTCHA API configuration
- A reports data source
- A geocoding data source
- URLs of the social platforms that have to be linked (share buttons)
- A development environment to build the front-end

#### Settings up reCAPTCHA

1. Go to https://www.google.com/recaptcha/admin/create
2. Fill th form :
    - Use reCAPTCHA version 3
    - Add your domain name (also add 'localhost' if used for development), if you're hosting the frontend on Firebase, you'll need to know its domain name too
    - Send
3. Copy the site key, it will be useful for the frontend configuration

#### Report data source

The reports data source is an online CSV file containing a summary of the reports by location, summed by status.

You can check the format [here](https://github.com/ch-covid-19/datasets).

A second file containing the last update time of the data source has also to be provided (last_update.txt). It's an ASCII text file containing the date in ISO format.

The report data source is generated by consolidation scripts in the [backend](https://github.com/ch-covid-19/self-report-backend).

This file must available online with a very high uptime and huge load capacity. It is used for the visualization and will be downloaded by each user.

#### Geocoding data source

The geocoding data source is an online CSV file containing, for each location, the name of the location and the geographical coordinates.

You can check the format [here](https://github.com/ch-covid-19/geo-locations).

The geocoding data source has to be set up for each country.

This file must available online with a very high uptime and huge load capacity. It is used for the visualization and will be downloaded by each user.

#### Local development environment

The frontend uses vue-cli. Please refer to the [official documentation](https://cli.vuejs.org/) for setup instructions.

### Setup

Please be sure to use 'yarn' instead of 'npm' as package manager.

  1. Clone this repository
  2. Create a `.env` file based on the `.env.example` file and fill it with your configuration. See below to learn more about the configuration.
  4. Run `yarn serve` to test locally and `yarn build` to build application

#### Configuration

1. Choose you location selector (default: postal-code) (only postal code available for now)
1. Setup the data source and geocoding data URLs
2. Set the map default position and zoom level
3. Set the recaptcha key (not the secret) with the value from the reCAPTCHA console.
4. List the languages you need
5. Set the github repository of your fork for the issues reporting
6. Set the social links for the desired platforms
7. Configure the URL for the backend endpoint to your backend instance.

### Notes on settng up NPM on Ubuntu ###
0. Download latest https://nodejs.org/en/download/ and set it to your path (e.g., ~/.bashrc) in ubuntu.
   - `NODEPATH=/home/pksec/software/node-v12.16.1-linux-x64/bin`
   - `PATH="$NODEPATH:$PATH:"`
1. `sudo apt-get install npm`
2. `npm install -g @vue/cli` # might need sudo rights
3. `npm install`
4. `npm run serve`

If you have installed with old node version. Frontend v1.0.1 will not compile in your machine. Update your node as described above and run:
`npm rebuild`

#### Fix 
https://stackoverflow.com/questions/49008498/npm-run-serve-error

``echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p``

## Develop


If you want to develop on the front-end, you can set-up the configuration with existing data sources from an already running instance.

For example, to point to the Swiss data source, put this in your .env file:
```
VUE_APP_VISU_DATA_SOURCE_URL=https://raw.githubusercontent.com/ch-covid-19/datasets/master
VUE_APP_VISU_GEOCODE_URL=https://raw.githubusercontent.com/ch-covid-19/datasets/master/geocoding.csv
VUE_APP_VISU_LAST_UPDATE_URL=https://raw.githubusercontent.com/ch-covid-19/datasets/master/last_update.txt

```

## Translations

Translations are done with the online [POEditor](https://poeditor.com/projects/view?id=327349) service.

The process for translators is the following :

- New keys are added in the frontend by the developers
- New keys are imported in POEditor (done automatically, but with manual trigger, responsibility to be defined)
- Translators are informed of the new keys by notifications
- Translators translates the new keys in POEditor
- Translations are exported in the frontend (done automatically, but with manual trigger, responsibility to be defined)
- The next release includes the new translations

## Contribute

Contributions are welcome through merge requests.

This section will be updated soon...
