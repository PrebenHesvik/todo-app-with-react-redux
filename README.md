#### Installs
- "@reduxjs/toolkit": "^1.9.3",
- "react-redux": "^8.0.5",
- "redux-logger": "^3.0.6",
- "reselect": "^4.1.7",
-  "redux-persist": "^6.0.0",

#### imports
- index.js
  - import { Provider } from 'react-redux';
  - import { PersistGate } from 'redux-persist/integration/react';

- store.js
  - import { configureStore } from '@reduxjs/toolkit';
  - import { persistStore, persistReducer } from 'redux-persist';
  - import storage from 'redux-persist/lib/storage';
  - import logger from 'redux-logger';

- root-reducer.js
  - import { combineReducers } from '@reduxjs/toolkit';

-  cart.reducer.js
   -  import { createSlice} from '@reduxjs/toolkit';

- cart.selector.js
  - createSelector from 'reselect'

- components where state is needed or state is updated
  - useSelector from 'react-redux' + a selector from cart.selector ==> retrieve state
  - useDispatch from 'react-redux' + a function from cart.action ==> to update state


#### Root reducer
- rootReducer is passed to createStore

#### Components where you need to import state or update state

#### Todo app
- light/dark theme
- Todo (todo_text, id, category, level_of_importance)
- Todo Count