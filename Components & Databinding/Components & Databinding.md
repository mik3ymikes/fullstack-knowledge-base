#Adding Navigation with Event biding and ngif
@Output() makes it listenable from outside from the compnent from the parent component
<app-recipes *ngIf="loadedFeature==='recipe'"></app-recipes>
<app-shopping-list *ngIf="loadedFeature!=='recipe'"></app-shopping-list>

     #Passing Recipe Data with property binding

@Input() allows us to bind a component property from the outside.

#Pasing Data with event and propety binding Combined

#allow the user to add ingredients
