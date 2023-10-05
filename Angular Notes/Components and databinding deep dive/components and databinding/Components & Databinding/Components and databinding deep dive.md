#

Event binding when clicked button send data and event happened

$event sends data as well

property event binding can be used on elements, directives, and components.

all properties of componeents are only accessible insde thier component not outside
have to be explicit on what you want to bind to others..
need to add a decorator @input any parent can now have access

if you wanna rename you can sign an alias to what you want it to be called on the outside @Input('srvElement')

what if want to inform parent component? confused
can use @
EventEmitter <> is a generic type
So So confused with component communication

Output can use aliases as well

#$#$
input ability to make properties bindable from outside from the parent compentn using this component

Output
allows parent components using this compoent to listen to events using event ommitter?

#More on View Encapsulation

styles will only be used by the component they belong to ..however
diffrent attribute are applied to their speceifc elements by angular
angualr enforces style ecapulation...same attribute giving to all elements in the component.

can overide encapsulation
encapsulation:ViewEncapsulation. none will end it On the compenent it was applied to. but if you apply rules to the one that was overwrtten then it will apply globally
also native. which uses shadow dom

local refrences....get access to elements to templates and use it in the templates or pass it on to use in typescript code

ngonIt is a lifecylce hook
once a new component is made angular goes through diff phases
ngONChanges -executed at start of a compoenent...
and after a bound input property changes
@ input ...when get new values

ngONint...gets executed once component is intiiazlied
will run after constructor

ngDoCheck called during evry change detecton run
property value from 1 to 2 and is in displayed in template?

ngAFterContent Inti-called after ng content has been projected in view

ngafterContentchecked callled when the projected content has been checked

ngAFterviewinit....after view and child view has been initalied

ngonDestryo...called when compennt about to be destyroed.
