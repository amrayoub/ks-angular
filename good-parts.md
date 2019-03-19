footer: © [@michahell](https://www.twitter.com/michahell) @ [ZIVVER](https://www.zivver.eu)
slidenumbers: true
build-lists: true
theme: Next, 1

[.text-emphasis: scale(3.0), alignment(center)]

# good parts

![](landscapes/blurred1.jpg)

---

# good parts

### - **TypeScript**
### - **app component tree**
### - **AOT**
### - **change strategy**
### - **animations**

#### - **decorators**


---

# good parts

### - reactive forms
### - view encapsulation
### - guards, interceptors

### - unit testing
### - observables (RXJS)

#### - state management (NGRX)
#### - marble testing

---

# reactive forms

![](bokeh/pexels3.jpeg)

---

[.code: Fira Code, line-height(1.2)]

# reactive forms

- opposed to *template-driven forms*
- still requires template bindings

- does **Angular** or do **you** create and manage **form** and **form controls** ?

<!-- - **[⚡ stackBlitz](https://stackblitz.com/edit/rxjs-uni-multicast)** -->

reactive

```html
<input type="text" [formControl]="name">
```

template-driven

```html
<input type="text" [(ngModel)]="model.name">
```

---

[.code: Fira Code, line-height(1.2)]

# reactive forms


```TS
new FormControl(
  { value: 'defaultValue', disabled: false },
  [
  	Validators.required,
    Validators.pattern(/[a-z]/)
  ]
)

// setting validators at a later time, sync:
formControl.setValidators(syncValidator)

// async:
formControl.setAsyncValidators(asyncValidator)
```

---

# [fit] view encapsulation

![](bokeh/pexels2.jpeg)

---

# [fit] view encapsulation

- VE in Angular ([pascal precht](https://blog.thoughtram.io/angular/2015/06/29/shadow-dom-strategies-in-angular2.html))
- ViewEncapsulation.**None**
- ViewEncapsulation.**Emulated** (default)
- ViewEncapsulation.**Native**
- **/deep/, >>>, and ::ng-deep** [(deprecated)](https://angular.io/guide/component-styles#deprecated-deep--and-ng-deep)
- Angular Material about [styling other components](https://material.angular.io/guide/customizing-component-styles)

---

# [fit] view encapsulation

[.code: Fira Code, line-height(1.2)]

```TS
new FormControl(
  { value: 'defaultValue', disabled: false },
  [
  	Validators.required,
    Validators.pattern(/[a-z]/)
  ]
)

// setting validators at a later time, sync:
formControl.setValidators(syncValidator)

// async:
formControl.setAsyncValidators(asyncValidator)
```

---

# unit testing

![](bokeh/pexels4.jpeg)

---

# unit testing

- clear way of setting up tests
- mock all dependencies with useClass / useValue
- easier to not mock the **Store**
- **.override()** deps you need
- don't use global methods -> Services
- shallow testing with **NO-ERROR-SCHEMA**
- mock data / models
- recommend looking at **[Spectator](https://engineering.datorama.com/spectator-for-angular-or-how-i-learned-to-stop-worrying-and-love-the-spec-2aa8521c8488)**

---

# unit testing

mocking dependencies

- **useValue**
- **useClass**
- use real thing, but only **.spyOn()**

---

# observables

### - observable or promise?
### - .pipe() or subscribe()?
### - observable life + switchMap
### - subscription management
### - hot vs cold, unicast vs multicast
### - operators

![](bokeh/pexels1.jpeg)

---

# [fit] observable or promise?

- **promise**: one-off, eager, not cancelable
- **observable**: multiple emits, lazy, **cancelable**
- handler functions: [promise -> async, Obs -> sync.](https://itnext.io/javascript-promises-vs-rxjs-observables-de5309583ca2)
- promise -> observable : **from(promise);**
- observable -> promise : **observable.toPromise();**

---

# [fit] .pipe() or subscribe()?

- I struggle with this 👶
- prefer **.pipe()** because I feel it reads easier
- use **tap()** operator for side effects

---

# [fit] observable life + switchMap

-  *| async* (Angular manages sub)
- *subscribe()* (You manage sub)
- keep alive or resubscribe
- *switchMap*

---

# [fit] subscription management

- [don't .unsubscribe()](https://medium.com/@benlesh/rxjs-dont-unsubscribe-6753ed4fda87)
- **takUntil(), takeWhile()**

---

# [fit] 🔥 hot vs. cold 🌧
# [fit] observables

- **cold**: data source does not exist. is instantiated upon **.subscribe()**
- **hot**: data source **exists** and is instantiated only *once*.
- relates to **unicast / multicast ([multicast operators](https://www.learnrxjs.io/operators/multicasting/))**
- [⚡ stackBlitz](https://stackblitz.com/edit/rxjs-uni-multicast)

![right](giphies/dribbble-iceberg.gif)

---

# observables

## to read
### - [learning observable by building observable](https://medium.com/@benlesh/learning-observable-by-building-observable-d5da57405d87)

---

# [fit] state management (NGRX)

![](bokeh/pexels5.jpeg)

---

# [fit] state management (NGRX)

- [don't fear the boilerplate](https://codeburst.io/state-management-in-angular-ee2ccb81c283) (super interesting read!)

---

# marble testing

### - [RxViz](https://rxviz.com/examples/pause-and-resume)

---

# decorators

### - [Create and Test Decorators in JavaScript – Netanel Basal](https://netbasal.com/create-and-test-decorators-in-javascript-85e8d5cf879c)
