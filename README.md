<h1 align="center">
   Pedro's Choice - ReactJS Snippets
</h1>

This extension contains a selections of the best ReactJS Snippets chosen by Pedro.

## React

| Prefix | Renders                          |
| ------- | -------------------------------- |
| `rfc →`   | Creates a React Function Component                   |
| `rfcall →`  | Creates a React Function Component with useCallback, useEffect and useState     |
| `rfceffect →`  | Creates a React Function Component with useEffect hook     |
| `rfcstate →`  | Creates a React Function Component with useState hook     |
| `itf →`  | Creates a new Interface (TS only)    |
| `uca →`  | useCallback hook       |
| `uef →`  | useEffect hook       |
| `ume →`  | useMemo hook       |
| `ust →`  | useState hook       |

## Styled Components

| Prefix | Renders                          |
| ------- | -------------------------------- |
| `sty →`   | Creates a Styled Components File                  |
| `sdiv →`  | Creates a new Styled Div     |
| `stynative →`   | Creates a Styled Components File (React Native)                 |
| `sview →`  | Creates a new Styled View (React Native)     |

## Redux - Thunk

| Prefix | Renders                          |
| ------- | -------------------------------- |
| `rxtype →`   | Creates a Redux Type File                   |
| `rxreducer →`  | Creates a Redux Reducer File    |
| `rxaction →`  | Creates a Redux Action File   |

## Full Expansions
### React

- `rfc` - Create **R**eact **F**unctional **C**omponent

```javascript

export function |(){
  return (
    <div>
      <h1>Hello - |</h1>
    </div>
  );
};

```

- `rfcall` - Create **R**eact **F**unctional **C**omponent with useCallback, useEffect and useState 

```javascript
import { useCallback, useEffect, useState } from 'react';

export function |(){
  const [myState, setMyState] = useState('');

  useEffect(() => {
    setMyState('');
  }, []);

  const myCallback = useCallback(() => {
    console.log(myState);
  }, [myState]);

  return (
    <div>
      <h1>Hello - |</h1>
    </div>
  );
};

```

- `rfceffect` - Create **R**eact **F**unctional **C**omponent with use**Effect**

```javascript
import { useEffect } from 'react';

export function |(){
  useEffect(() => {
    console.log('myEffect');
  }, []);

  return (
    <div>
      <h1>Hello - |</h1>
    </div>
  );
};

```
- `rfcstate` - Create **R**eact **F**unctional **C**omponent with use**State**

```javascript
import { useState } from 'react';

export function |(){
  const [myState, setMyState] = useState('');

  return (
    <div>
      <h1>Hello - |</h1>
    </div>
  );
};

```

- `itf` - Creates a new **I**n**t**er**f**ace

```javascript
interface | {
  myProps?: boolean;
}
```

- `uca` - **u**se**Ca**llback hook

```javascript
const | = useCallback(() => {

}, []);
```

- `uef` - **u**se**Ef**fect hook

```javascript
useEffect(() => {

}, []);
```

- `ume` - **u**se**Me**mo hook

```javascript
const | = useMemo(() => {

}, []);
```

- `ust` - **u**se**St**ate hook

```javascript
const [|, set|] = useState();
//Press Tab to apply CamelCase. e.g. [state, setState]
```

### Styled Components


- `sty` - Creates a **Sty**led Components File

```javascript
import styled from 'styled-components';

export const div = styled.div``;
```

- `sdiv` - Creates a new **S**tyled **div**

```javascript
export const | = styled.div``;
```
- `stynative` - Creates a **Sty**led Components File for React **Native**

```javascript
import styled from 'styled-components/native';

export const div = styled.View``;
```

- `sview` - Creates a new **S**tyled **View**

```javascript
export const | = styled.View``;
```

### Redux - Thunk

- `rxtype` - Creates a **R**edu**x** **Type** File

```javascript
export const START_FETCH = '@|/START_FETCH';
export const DONE_FETCH = '@|/DONE_FETCH';
export const GET_DATA = '@|/GET_DATA';

interface | {
  myData: string;
}

export interface State {
  readonly loading: {
    getData: boolean;
  };
  readonly data: [] | null;
}

interface StartFetch {
  type: typeof START_FETCH;
  kind: string;
}

interface DoneFetch {
  type: typeof DONE_FETCH;
  kind: string;
}

interface GetData {
  type: typeof GET_DATA;
  data: [];
}

export type ActionTypes = 
   | StartFetch
   | DoneFetch
   | GetData;
```

- `rxreducer` - Creates a **R**edu**x** **Reducer** File

```javascript
import * as Types from './types';

const INITIAL_STATE = {
  data: null,
  loading: {
    getData: false,
  },
};

export default (
  state = INITIAL_STATE,
  action: Types.ActionTypes,
): Types.State => {
  switch (action.type) {
    case Types.START_FETCH:
      return { ...state, loading: { ...state.loading, [action.kind]: true } };
    case Types.DONE_FETCH:
      return { ...state, loading: { ...state.loading, [action.kind]: false } };
    case Types.GET_DATA:
      return { ...state, data: action.data };
    default:
      return state;
  }
};
```

- `rxaction` - Creates a **R**edu**x** **Action** File

```javascript
import { Action } from 'redux';
import { ThunkAction } from 'redux-thunk';
import { StoreState } from 'store';
import * as Types from './types';

export const | = (): ThunkAction<
  void,
  StoreState,
  unknown,
  Action<string>
> => async dispatch => {
  try {
    dispatch({ type: Types.START_FETCH });
    dispatch({ type: Types.DONE_FETCH });
  } catch {
    // error
  }
};
```
<hr>

## Add to your project

There are 2 ways you can add Pedro's Choice - Keymap to your project:

#### By command
Launch VS Code Quick Open (`Ctrl+P`), paste `ext install pedroschoice.pedros-choice-reactjs-snippets`, and press enter.

#### By the Extension Marketplace

Launch VS Code Extension Marketplace (Ctrl+Shift+X), search for `Pedro's Choice`, and look for the best looking bald dude in the store.

## Contributing
### How do I contribute?

If you have a sugestion for a new snippet or found some bug, feel free to help me out.

1. Head over to the [GitHub repository](https://github.com/pedrozocatelli/pedros-choice-vscode-reactjs-snippets). 
2. Open the [`snippets-ts.json` file](https://github.com/pedrozocatelli/pedros-choice-vscode-reactjs-snippets/blob/master/snippets/snippets-ts.json) or the [`snippets.json` file](https://github.com/pedrozocatelli/pedros-choice-vscode-reactjs-snippets/blob/master/snippets/snippets.json).
3. Make the changes and updated the README file.
4. Open a pull request. 

## License
[MIT](LICENSE.md)