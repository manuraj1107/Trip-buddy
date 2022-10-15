## Lets build trip-buddy 

### Install the packages ,libraries and modules
First we have to install material-ui, material-ui/core, material-ui/icon

> npm install @material-ui/core @material-ui/icons @material-ui/lab

#### Warning
if you face error like this

```
npm ERR! Could not resolve dependency:
        npm ERR! peer react@"^16.8.0 || ^17.0.0" from @material-ui/core@4.12.4
        npm ERR! node_modules/@material-ui/core
        npm ERR!   @material-ui/core@"^4.12.4" from the root project
```

then use and instal this, this will change your node_modules

```
npm config set legacy-peer-deps true
npm i
```


second we'll install axios, google-maps api

##### Axios

> npm install axios

##### google-maps api

> npm install @react-google-maps/api google-map-react


### Building Folders and its Structure

First create folder <b>components</b>

inside of <b>components</b> folder create four more folder and export it with their components

1. Header > Header.jsx
2. List > List.jsx
3. Map > Map.jsx
4. PlaceDetails > PlaceDetails.jsx


#### building the UI structure of App.jsx

> App.jsx
```
import React, { Fragment } from "react";
import {CssBaseline, Grid} from '@material-ui/core'
import Header from "./components/Header/Header";
import List from "./components/List/List";
import Map from "./components/Map/Map";

function App() {

  return (
    <Fragment>
      <CssBaseline />
      <Header />
      <Grid container spacing={3} style={{width: '100%'}} >
          <Grid item xs={12} md={4}>
             <List />
          </Grid>
          <Grid item xs={12} md={4}>
             <Map />
          </Grid>
      </Grid>
    </Fragment>
  )
}

export default App

```