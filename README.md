# PulseJS 
Pure vanilla javascript, no CSS changes needed or to add anything else. 

### work in progress  
- [ ]  currently usable  
- [x] non-functioning  

## Usage
### HTML
Add the 'pulse' class to any HTML element to enable a CSS animation to fire upon user click. 
### Javascript
To set the default animation time in milliseconds: 
```Javascript
pulse.settings.animationTime = 250 //accepts number, not string. don't do: '.25s' or '250ms'.
```
To pulse any element in javascript:
```Javascript
pulse.animateElement(element); //pulse any element no need to add 'pulse' class in HTML.
```
To pulse any element, for a one off custom duration in milliseconds:
```Javascript
pulse.animateElement(element, 2000); //pulse this element for 2s.
```
Pulse any element, and repeat animation:
```Javascript
pulse.animateElement(element, 2000, 3); //pulse this element for 2s, repeat 3 times.
```
Pulse any element with callback:
```Javascript
pulse.animateElement(element, 2000, 1, alert); //pulse this element for 2s, repeat 1 times, then alert.
```
Pulse any element with callback and parameters:
```Javascript
pulse.animateElement(element, 2000, 1, ()=>alert('hi')); //pulse this element for 2s, repeat 1 times, then alert. 
```
Cancel pulse on a currently animated element:
```Javascript
pulse.cancelAnimation(element); //only cancels current animation + callback passed in parameters. does not cancel promise yet..
```
