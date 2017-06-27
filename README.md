# Angular4 - Telosys 3 Template

This template is used by [Telosys](http://www.telosys.org/) to generate an Angular web app using basic RESTful API services based on the NodeJS server template [here](https://github.com/so-technology-watch/telosys-templates-nodejs).

## Prerequisites

You need to have Angular CLI installed. For further info, refer to the [project GitHub](https://github.com/angular/angular-cli).

The Angular CLI version used in the template is v1.1.2

## Table of Contents

* [Installation](#installation)
* [Template Configuration](#template-configuration)
* [Usage](#usage)
* [Configure API](#configure-api)
* [Dependencies used](#dependencies-used)

## Installation

Refer to [Telosys Online Documentation](https://sites.google.com/site/telosystools/getting-started) to download and configure the template.

## Template Configuration

Let's assume you already have created your own project with Angular CLI and you want to generate the template.

*In case you didn't yet created a project, refer to [Angular CLI documentation](https://github.com/angular/angular-cli#generating-and-serving-an-angular-project-via-a-development-server) to see how to create one*

After generating successfuly the template in your project, you will have few steps to do before being able to use the template.

### Package.json

You will find a file called `package_gen.json` next to your original `package.json`.

#### For starting users

Rename the original `package.json` to `package_old.json` and then change the `package_gen.json` to `package.json`. 

And then run :
```bash
~ npm install
```

This will install all the dependencies used by the templates.

#### For advanced users

You can add the modules manually into the `package.json` file.

```
"dependencies": {
    "@angular/material": "^2.0.0-beta.7",
    "@types/underscore": "^1.8.0",
    "angular2-notifications": "^0.7.3",
    "hammerjs": "^2.0.8",
    "material-design-lite": "^1.3.0"
    "underscore": "^1.8.3"
```

<span style="color:#fe2e2e">**IMPORTANT:** Be careful of angular and angular-cli versions or you might have some compilations errors.</span>

### angular-cli.json

As like the package.json file, you will have `.angular-cli_gen.json` file generated.

* Add the following line to `"styles": []` in .angular-cli.json original file

`"../node_modules/material-design-lite/material.min.css"`

* Add the following line to `"scripts":` [] in .angular-cli.json original file

```
"../node_modules/material-design-lite/material.min.js",
"../node_modules/hammerjs/hammer.min.js"` to `"styles": []
```

### tsconfig.json

Rename the original `tsconfig.json` to `tsconfig_old.json`.

And rename the generated file `tsconfig_gen.json` to `tsconfig.json`.


## Usage

After configuring your template, you can run `~ ng serve` from the terminal in your project folder to test it.

*If you already tried and used the NodeJS template, you will be able to interact with the server through its API from the angular web app generated*

## Configure API

The file `src/app/app.configuration.ts` is used to configure the API url.

```javascript
export class Configuration {
    public server = 'http://localhost:3000/';
    public apiUrl = 'api/';
    public serverWithApiUrl = this.server + this.apiUrl;
}
```

You will be able to change your server url as well as the url suffix (if needed).

## Dependencies used

* [Angular CLI](https://github.com/angular/angular-cli) :
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![version](https://img.shields.io/badge/version-1.1.2-brightgreen.svg)
<br>The Angular CLI makes it easy to create an application that already works, right out of the box
* [Material2](https://material.angular.io/) : &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![version](https://img.shields.io/badge/version-2.0.0.beta.7-brightgreen.svg)
<br> Official Material Design components built for and with Angular.
* [Material Design Lite](https://getmdl.io/) :
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![version](https://img.shields.io/badge/version-1.3.0-brightgreen.svg)
 <br/> Material Design Lite lets you add a Material Design look and feel to your websites. It doesn’t rely on any JavaScript frameworks and aims to optimize for cross-device use, gracefully degrade in older browsers, and offer an experience that is immediately accessible
* [Angular2-Notifications](https://github.com/flauc/angular2-notifications) :
&nbsp;&nbsp;
![version](https://img.shields.io/badge/version-0.7.3-brightgreen.svg)
 <br/> A light and easy to use notifications library for Angular 2. It features both regular page notifications (toasts) and push notifications.
 * [Underscorejs](http://http://underscorejs.org/) :
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![version](https://img.shields.io/badge/version-1.8.3-brightgreen.svg)
 <br/> Underscore is a JavaScript library that provides a whole mess of useful functional programming helpers without extending any built-in objects.