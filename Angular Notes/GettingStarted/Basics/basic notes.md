#module introduction

#How an angular app gets loaded and started
reach page at local host 4200,
app component html can be used to change the page if ng serve is running. How does the browser know to render it? this index.html is actually served by the server but it is inlcuiding
a <app-root> <app-root>. All files with component are related to the root component. app.component.ts has a selector with app-root and provides information angular needs to replace the app root
with the content we provided in app.component.html. in the index.html file is injects of script imports to be executed. Main.ts is the first code executed. For example bootstrap:[appComponent]

#components are important!
index.html is served and contains scripts that are executed and starts angular app. Angular app gets information that it needs to know and inforation it can parse and undertand and insert angular.
Components are a key feature and application is buit with componetns. The root component holds entire application and items are nested. Each component has its own template and styling

#creating a new component
start with app component ..root component...module.ts? will e added app component.html. A decorator typescript feature to enhance elements, classes, etc. @Component() name a selector which is an html tag where you can use it later.Then need to create a templateUrl to refrence an external file...alternative will be discussed later.
import{ Component } from "@angular/core"

@Component({
selector: "app-server",
templateUrl: "./server.component.html"
})

export class ServerComponent{

}
created first componoent

#understanding the role of appModule and Component
Modules are used to bundle pieces into packages..such as components
by default angular wont scan all modules...have to tell it its there
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';

import { AppComponent } from './app.component';
import { ServerComponent } from './server/server.component';

@NgModule({
declarations: [
AppComponent,
ServerComponent
]

added server component in typescript app.module file
<app-server></app-server> was added to app component .html

#Creating components with cli
can create another component with ng generate component servers
or ng g c servers
servers is name of folder i think
they can be nested and replicate by using the selector multiple times

#working with templates and styles component styles
must have a template or template url.
can also use backtics to write html code
styles:[`
h3{
color:dodgerblue
}`]
})
#component basics
can use inline ...but not both. better use external if more.
can select by atritube by putting in square brackets

<div app-servers></div>

selector: '.app-servers',
or can select by class

<div class="app-servers"></div>
selecting by id wont work...pseudo selectors dont work

#assignment basics problem and solution...tried multipe tiems to download and run ng serve after following all steps but started code would not work on ng serve.
deperacation and callback eroor called.

import { Component } from '@angular/core';

@Component(
{ selector: "app-warning-alert",
template:`
    <p>This is a warning, you are in danger!</p>`
}
)

export class WarningAlertComponent{

}

import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';

import { AppComponent } from './app.component';
import { SuccessAlertComponent } from './success-alert/success-alert.component';
import { WarningAlertComponent } from './warning-alert/warning-alert.component';

@NgModule({
declarations: [
AppComponent,
WarningAlertComponent,
SuccessAlertComponent
],
imports: [
BrowserModule
],
providers: [],
bootstrap: [AppComponent]
})
export class AppModule { }
#what is databidning

Communicaton between typescript and the template html
string interpolation or property binding can be used to outputdata
({{ data }})
([ prperty ])="data

or can event binding...click and an event happens

#string interpolation
