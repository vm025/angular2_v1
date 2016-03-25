


1a) app.component.ts (AppComponent class)

export class AppComponent {
  public title = 'Tour of Heroes';
  public hero = 'Windstorm';
}


1b) template: '<h1>{{title}}</h1><h2>{{hero}} details!</h2>'


2a)  app.component.ts (Hero interface)

interface Hero {
  id: number;
  name: string;
}


2b)  app.component.ts (Hero property)

public hero: Hero = {
  id: 1,
  name: 'Windstorm'
};

2c)  template: '<h1>{{title}}</h1><h2>{{hero.name}} details!</h2>'

2d)  multiline tpl: 
  template:`
  <h1>{{title}}</h1>
  <h2>{{hero.name}} details!</h2>
  <div><label>id: </label>{{hero.id}}</div>
  <div><label>name: </label>{{hero.name}}</div>
  `

  Alt:
  template: '<h1>{{title}}</h1> \
           <h2>{{hero.name}} details....</h2> \
           <div><label>id: \
           </label>{{hero.id}}</div>  \
           <div><label>name: </label>{{hero.name}}</div> \
           <div> \
			    <label>name: </label> \
			    <input value="{{hero.name}}" placeholder="name"> \
		  </div> '

2e)  Two way binding:
<input [(ngModel)]="hero.name" placeholder="name">



