#planning App
Should look at features you will need and what components
root component...the app comoneent.
a header in its own component
a shopping list component with a list and edit component nested in the list
a recipe book compnent ....with a list, items, and details
each component focus on one main topic.
Determine which data to use. data should be in classes.
#Creating compnents can create with ng g c and then the name
example ng g c recipes
Could also nest folders ng g c recipes/recipe-list
could nest even deeper ng g c recipes/recipe-list/recipe-item
by default a folder will nest in the app component foler
#using components
call the compoenents in the main app compnent html...you can then call other compenets in the compenets that were callled the the main app. This will put the things in oreder.

# adding a nav bar

Bootstrap can be used to add navbars quickly

<nav class="navbar navbar-default">
  <div class="contianer-fluid">
    <div class="navbar-header">
      <a href="#" class="navbar-brand">Recipe Book</a>
    </div>
    <div class="collapse navbar-collapse">
    <ul class="nav navbar-nav">
      <li><a href="#">Recipes</a></li>
      <li><a href="#">Shopping List</a></li>
    </ul>
    <ul class="nav navbar-nav navbar-right">
      <li class="dropdown">
        <a href="#" class="dropdown-toggle">Manage <span class="caret"></span></a>
        <ul class="dropdown-meun">
          <li> <a href="#">Save Data</a></li>
          <li> <a href="#">Fetch Data</a></li>
        </ul>

#creating a recipe model
Created a recipe.model.ts file to hold the information required for a certain class
export class Recipe{
public name:string;
public description:string;
public imagePath:string;

constructor(name:string, desc:string, imagePath:string){
this.name=name;
this.description=desc;
this.imagePath=imagePath
}

}
#adding content to recipe components
must inport Recipe from other file
import {Recipe} from "../recipes.model" have to move up one folder so extra period
recipes:Recipe[]=[] ...its going to expect an array
export class RecipeListComponent {
recipes:Recipe[]=[
new Recipe("A test recipe", "simply a test","https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTcPBKGZDo0rHbKJ6JBGCWeKgLBV3BJsZy_WA&usqp=CAU" )
]

#OUttputting a list of reipes with ngFor
class="list-group-item clearfix"
\*ngFor="let recipe of recipes">
then use string interpolation

<h4 class="list-group-item-heading">{{recipe.name}}</h4>
        <p class="list-group-item-text">{{recipe.description}}</p>
      </div>
      <span class="pull-right">
        <img src="{{recipe.imagePath}}"
        or could use property binding[src]="recipe.imagePath
#display recipe details
dont know how to do cross component communnication yet

#creating ingredient model

export class Ingredient{
public name:string;
public amount:number

constructor(name:string, amount:number){
this.name=name,
this.amount=amount
}
}

could do this but there is shortcut
export class Ingredient{
constructor(public name: string, public amount: number ){}
}

more examples of looping
\*ngFor="let ingredient of ingredients" > {{ingredient.name}} ({{ingredient.amount}})</a>

</ul>
</div>

  </div>
# add a shoping list

added buttons and layout
