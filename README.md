# React-Select-Nested

Yet another Select control for [React](https://reactjs.com). It allows building nested selects.

![](react-select-nested.gif)


```
npm i react-select --save
```

Then use it in your app:

```js

import React, { Component } from 'react';
import Select from 'react-select-nested';

class App extends Component {
  render() {

      const fruit = [
          {
              val: 0,
              label: 'Apple'
          },
          {
              val: 1,
              label: 'Orange',
              items: [{val: 7, label: 'sub item 1', selected: false}, {val: 8, label: 'sub item 2', selected: false}]
          },
          {
              val: 2,
              label: 'Grape',
              items: [{val: 5, label: 'sub item 3', selected: false}, {val: 6, label: 'sub item 4', selected: false}]
          },
          {
              val: 3,
              label: 'Pomegranate',
              items: [{val: 9, label: 'sub item 5', selected: false}, {val: 10, label: 'sub item 6', selected: false}]
          },
          {
              val: 4,
              label: 'Strawberry',
          }
      ];

      return (
          <div>
              <Select
                  placeholder="Select fruit"
                  list={fruit}
                  onSelectChange={(item)=>console.log('use your custom handler here', item)}
              />
          </div>
      );
  }
}

export default App;

```