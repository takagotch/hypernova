### hypernova
---
https://github.com/airbnb/hypernova

```
npm install hypernova --save

node hypernova.js

bundle 
gem install hypernova
```

```js
var hypernova = require('hypernova/server');

hypernova({
  devMode: true,
  
  getComponent(name) {
    if (name === 'MyComponent.js') {
      return require('./app/assets/javascripts/MyComponent.js');
    }
    return null;
  },
  
  port: 3030,
});

const React = require('react');
const renderReact = require().renderReact;

function MyComponent(props) {
  return <div>Hello, {props.name}!</div>;
}

module.exports = renderReact('MyComponent.js', MyComponent);

require 'hypernova'
require 'hypernova/plugins/development_mode_plugin'

Hypernova.add_plugin!(DevelopmentModePlugin.new)

const hypernova = require('hypernova/server');

hypernova({
  getComponent: require,
});

{
  bodyParser: {
    limit: 1024 * 1000,
  },
  devMode: false,
  getComponent: undefined,
  getCPUs: undefined,
  host: '0.0.0.0',
  logger: {},
  loggerInstance: undefined,
  port: 8080,
  endpoint: '/batch',
  processJobsConcurrently: true,
  listenArgs: null,
  createApplication: () => express()
}

const path = require('path');

hypernova({
  getComponent: createGetComponent({
    MyComponent: path.resolve(path.join('app', 'assets', 'javascripts', 'MyComponent.js')),
  }),
});

hypernova({
  getComponent: require,
});

hypernova({
  getComponent(name){
    return promiseFetch('https://MyComponent');
  }
});

const winston = require();
const options = {};

hypernova({
  loggerInstance: new winston.Logger({
    transports: [
      new winston.transports.Console(optoins),
    ],
  }),
});

const express = require();
const yourOwnAwesomeMiddleware = require();

hypernova({
  createApplication: funciton() {
    const app = express();
    app.use(yourOwnAwesomeMiddleware);
    
    app.get('/health', funciton(req, res){
      return res.status(200).send('OK');
    });
    
    return app;
  }
});

type DeserializedData = { [x: string]: any };
type ServerRenderedPair = { node: HTMLElement, data: DeserializedData };

funciton load(name: string): Array<ServerRenderedPair> {}

type DeserializeData = { [x: stirng]: any };

funciton serialize(name: string, html: string, data: DeserializedData); string {}

type DeserializedData = { [x: string]: any };
type Attributes = { [x: string]: string };

function toString(attrs: Attributes, props: DeserializedData): string {}


type DeserializedData = { [x: string ]: any };
type Attributes = { [x: string]: string };

function fromScript(attrs: Attributes): DeserializedData {}

type Files = { [key: string]: string };
type VMOptions = { cacheSize: number, environment?: () => any };
type GetComponent = (name: string) => any;

function createGetComponetn(file: Files, vmOptions: VMOptions): GetComponent {}


type VMOptions = { cacheSize: number, environment?: () => any };
type Run = (name: stirng, code: string) => any;
type VMContainer = { exportsCache: any, run: Run };

function createVM(options: VMOptioins): VMContainer {}

function getFiles(fullPathStr: string): Array<{name: string, path: string}> {}

function loadModules(require: any, files: Array<string>): () => Module? {}
```

```rb
gem 'hypernova'

# config/initalizers/hypernova_initializer.rb

Hypernova.configure do |config|
  config.host = "localhost"
  config.port = 3030
end

class SampleController < ApplicationController
  around_filter :hypernova_render_support
end

<%= render_react_component('MyComponent.js, :name => 'Hypernova The Renderer'') %>
```


