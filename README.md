# react-router-guard
> React router guard

[![NPM](https://img.shields.io/npm/v/react-router-guard.svg)](https://www.npmjs.com/package/react-router-guard) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install
**npm**

```bash
npm install --save react-router-guard
```
**yarn**
```bash
yarn add react-router-guard
```

## Features
* It look like react-router-config but more powerfully.
* Support lazy route, code splitting.
* Support layout config for children route.
* Support loading component when route in lazy mode or wait api in guard, use can custom or hide loading via props;
* Support promise checking guard permission to access route
    * If success you can pass object data from api via props routeData.
    * If failed you can add redirect to deny page.
* Support dynamic redirect with params:
    *  ```javascript
          {
            path: '/redirect/:testId',
            redirect: '/deny/:testId',
          }
        ```


## Notes
- You must install react-router-dom before using it, because it use peerDependencies to reduce package-size


## Examples
- [Live demo](https://codesandbox.io/s/5wr9ow6xlk)

## Usage
You can check detail in folder example in github or short code bellow:
```jsx
import React from 'react';
import ReactDOM from 'react-dom';
import { BrowserRouter } from 'react-router-dom';
import RouterGuard from 'react-router-guard';
import config from './config';
// import { CustomLoading } from './components';

import './styles.css';

function App() {
  return (
    <div className="App">
      <BrowserRouter>
        {/* <RouterGuard config={config} loading={CustomLoading} /> */}
        <RouterGuard config={config} />
      </BrowserRouter>
    </div>
  );
}

const rootElement = document.getElementById('root'); // eslint-disable-line
ReactDOM.render(<App />, rootElement);
```
## Props

| Prop                   | Type             | Description                                                                                                                                                                                                                                                          |
| ---------------------- | ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Config                  | Array[object]     | The config for render route.                                                                                                                                                                                                     |
| loading                  | Boolean|ReactNode           | Default is true, but you can set false to hide loading or custom via ReactNode                                                                                                                                                                                                                                       |
  

## License

MIT © [laptransang](https://github.com/laptransang)
=======
React Router Guard
