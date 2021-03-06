# Flowra

Build workflow have never been such easy. Just define your worker functions and call it when you need with this library in your current project.

## Installation

```bash
npm install flowra --save
```
## Worker

### Configuration

After installing, you need to setup your worker with the information you can get on [simpleFlow](http://simpleflow.io)
```js
const Flowra = require('flowra').config({
  app_env: 'dev || prod',
  app_id: 'YOUR_APP_ID',
  user_token: 'YOUR_USER_TOKEN',
});
```
### Start a worker

When everything is setup well, you can start your worker with this function
```js
Flowra.worker.start(function(taskName, data, onSuccess, onFail) {
  // Job to be done including these functions
  onSuccess("Everything went well");
  onFail("Oups! error");
});
```


## Workflow

### Configuration

You also need to setup your workflow with your app informations on server-side
```js
const Flowra = require('flowra').config({
  app_env: 'dev || prod',
  app_id: 'YOUR_APP_ID',
  user_token: 'YOUR_USER_TOKEN',
});
```

### Start a workflow

To make it work, you have to include this function in your code when you want to call your workflow 
```js
Flowra.workflow.start({
  type: "YOUR_WORKFLOW_TYPE",
  data: {
    
  }
});
```


### Notes

⛔️  This project is currently in development and not working for public ⛔️  
If you're interested please contact me : [here](mailto:louis@thefamily.co?Subject=Project%20Flowra%20Questions)
