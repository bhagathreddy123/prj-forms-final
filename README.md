# N5CompleteGuide

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 1.5.0.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `-prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).


https://console.firebase.google.com

create project on firebase and create a database inside rules give read write true  then publish for giving full permissions to all. 


resolved the issue Property 'map' does not exist on type 'Observable<Response> by adding 
import 'rxjs/Rx';


generating signup and signin components in cmd prompt

ng g c auth/signup --spec false
ng g c auth/signin --spec false

setting up firebase SDK

first enable Email/password  provider in Authentication section.


then run below command in cmd prompt

npm install --save firebase


for giving access for login we need to set up like below in firebase database console inside project

{
  "rules": {
    ".read": "auth != null",
    ".write": "auth != null"
  }
}