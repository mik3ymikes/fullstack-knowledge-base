# #module introduction


# #How an angular app gets loaded and started
# reach page at local host 4200, 
# app component html can be used to change the page if ng serve is running. How does the browser know to render it? this index.html is actually served by the server  but it is inlcuiding 
# a <app-root> <app-root>. All files with component are related to the root component. app.component.ts has a selector with app-root and provides information angular needs to replace the app root
# with the content we provided in app.component.html. in the index.html file is injects of script imports to be executed. Main.ts is the first code executed. For example bootstrap:[appComponent]

# #components are important!
# index.html is served and contains scripts that are executed and starts angular app. Angular app gets information that it needs to know and inforation it can parse and undertand and insert angular.
# Components are a key feature and application is buit with componetns. The root component holds entire application and items are nested. Each component has its own template and styling
