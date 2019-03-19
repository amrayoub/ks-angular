footer: © [@michahell](https://www.twitter.com/michahell) @ [ZIVVER](https://www.zivver.eu)
slidenumbers: true
build-lists: true
theme: Next, 1

[.text-emphasis: scale(3.0), alignment(center)]

# bad parts

![](landscapes/blurred4.jpg)

---

# bad parts

### - view encapsulation
### - ngFor + list updates
### - custom form components
### - ngIf, ngFor, ngLet?
### - state management

![](landscapes/blurred4.jpg)

---

# [fit] view encapsulation

---

# [fit] ngFor list updates

---

# [fit] custom
# [fit] form
# [fit] components

![right filtered](https://media.giphy.com/media/ipOf23LjeNeeI/giphy.gif)

---

# [fit] custom form components

__the bad__
- underdocumented
- uses multiple interfaces, classes and styles
- ``` formControlName !== formcontrolname ```

^ - documentation: not up to date.
- Form API exists of lots of stuff.
- lots of ids, refererences passed as strings.
- READ: especially the last two are important to read about.

__read about__
- **Reactive forms** (programmatic) *vs* **template-driven** (angularJs style) forms
- **FormControl**, **FormGroup**, **FormArray** and **Validator**s
- **ControlValueAccessor**
- **MatFormFieldControl**

---

# [fit] ngIf
# [fit] ngFor
# [fit] ngLet?
# [fit] .......it be

![left filtered](giphies/let-it-be.gif)

---

# [fit] ngIf, ngFor, ngLet

__the bad__
- asd

---

# [fit] state
# [fit] management
# [fit] [NGRX]
# [fit] + component
# [fit] lifecycle

![right filtered](https://media.giphy.com/media/VsuiH69ecp6XC/giphy.gif)

---

# state management

__the bad__
- dumb components, smart components ✅
- encapsulation vs. everything redux ❓
- @Effects and observables *(do / dont / caveats)*

