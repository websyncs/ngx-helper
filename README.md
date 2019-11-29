# @websyncs/ngx-helper

`@websyncs/ngx-helper` is an Angular helper library for many useful operators. 

## Features

Currently it will have a set of decorators below. Its more similar like stencil

- `@Event` declares a DOM event the component might emit
- `@Listen` listens for DOM events


## Installation

To use ngx-helper in your project install it via [npm](https://www.npmjs.com/package/@websyncs/ngx-helper):

```
npm i @websyncs/ngx-helper --save
```

## Usage
```typescript

/** Import the library anywhere inside an application */
import { Event, Listen, EventEmitter } from '@websyncs/ngx-helper';

/** Then add event emitter as a property of any class 
    User @Event() decorator to name the event
*/
export class ClassA {

  @Event('EVENT_NAME') emitter: EventEmitter;
  
  triggerEvent() {
    this.emitter.emit({message: 'Hello World'});
  }
}
/** Then add event event listener to handle the event  
    User @Listen() decorator to name the event
*/
export class ClassB {

  @Listen('EVENT_NAME')
  handleEvent(payload) {
    console.log(payload)
  }
  
}

```
