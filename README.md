# Burner
Basic agency style rails app

## Installation

### Install yarn 

1. curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
2. echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
3. sudo apt update && sudo apt install yarn

### Install JQuery

1. yarn add jquery

2. add the following to config/webpack/environment.js

```
	const webpack = require('webpack')
	environment.plugins.prepend('Provide',
  		new webpack.ProvidePlugin({
    	$: 'jquery/src/jquery',
    	jQuery: 'jquery/src/jquery'
  	})
	)
```
3. Require jquery in application.js

```
require('jquery')
```

### Install Bootstrap

1. add bootstrap to Gemfile

2. Run bundle install

3. Add bootstrap to assets/stylesheets/application.css

```
 @import "bootstrap";

```

4. Add bootstrap to application.js

```
//= require jquery3
//= require jquery_ujs
//= require popper
//= bootstrap-sprockets
//= require tree .

```