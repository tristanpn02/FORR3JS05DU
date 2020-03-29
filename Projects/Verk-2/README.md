# FORR3JS-Verk2
---
1. Afhverju er `getElementById()` fljótleglegasta aðferðin?
* Vegna þess að það er bein kall á JavaScript og leitar bara eftir ID í staðin fyrir attributes, class ofl.
2. Hver er munurinn á static og live NodeList?
* Munurin er sá að Live Nodelist uppfærir safnið sjálfkrafa eftir breytingum á DOM
3. Hver er munurinn á true og false í AddEventListener?
```javascript
   elem.addEventListener("click", handlerFunction, true);
   elem.addEventListener("click", handlerFunction, false);
```
* Event handlerin er annaðhvort keyrður ef skilyrðið er satt eða ekki
4. this vísar í Event listener á html element en ekki á object. Þú getur notað `bind()` til að breyta því.
Leystu eftirfarandi kóðadæmi með notkun á `bind()` til að birta í console “My name is Sam“ en ekki undefined.
```javascript
let Person = {   
  name: 'Sam',   
  sayName: function(){     
     console.log('My name is '+ this.name);   
  }
 };
buttonEl.addEventListener('click', Person.sayName);
```
vvv
```javascript
let Person = {   
  name: 'Sam',   
 };

function sayName() {     
     console.log('My name is '+ this.name);   
}

let sayPerson = sayName.bind(Person);

buttonEl.addEventListener('click', sayPerson());
```
