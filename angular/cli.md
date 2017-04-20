# Angular cli Hacks

## commands
### General Commands
Install
```
npm install -g @angular/cli
```
Version
```
ng version
```
Help
```
ng help
```
Help specific command
```
ng help <command>
```
### create a project
Generate a new app in /my-app
```
ng new my-app
```
Generate a new app in /my-app
```
ng new my-app --routing          // Add routing
              --prefix <prefix>  // Set your prefix
              --style scss       // Define your styles
              --dry-run          // Verify it is generating my expectations
              --skip-install     // Without running npm install
```
### Server
Run server
```
ng serve
```
run server and ope in a browser
```
ng serve -o // -open
```
### generate components
Generate component
```
ng g c my-component // Or ng generate component my-component
```
Generate class
```
ng g cl myClass // Or ng generate class myClass
```
Generate Service
```
ng g s data // Or ng generate service data
```
Generate Service and add to module
```
ng g s data -m app.module
```
Service with dry-run
```
ng g s data -m app.module -d
```
