# &lt;wdpr-wc-polymer-textbox-custom&gt;

>Custom Input box built from scratch by wrapping Native HTML &lt;input type="text"&gt; element using [Polymer v1.0](https://www.polymer-project.org/) 

## Prerequisites

In order to run it locally you'll need to fetch some dependencies and a basic server setup.

1. Node.js v4.4.7+

2. npm v2

3. Install bower and bower-cli as global module

 	 	npm install -g bower
		npm install -g bower-cli

4. Install [polyserve](https://npmjs.com/polyserve):

 	 	npm install -g polyserve

Note : polyserve works only with Node.js v4.x.x +	



## Install

Install the component using [Bower](http://bower.io/):

```
bower install wdpr-wc-polymer-textbox-custom --save
```

Or [download as ZIP](https://github.com/disney/wdpr-wc-polymer-textbox-custom/archive/master.zip).

## Usage

1. Import polyfill:

    ```html
    <script src="bower_components/webcomponentsjs/webcomponents.min.js"></script>
    ```

2. Import custom element:

    ```html
    <link rel="import" href="bower_components/wdpr-wc-polymer-textbox-custom/wdpr-wc-polymer-textbox-custom.html">
    ```

3. Start using it!

    ```html
    <wdpr-wc-polymer-textbox-custom placeholder=" First Name*" >
    ```


## Development


1. Install local dependencies:

    ```
    bower install
    ```

2. Start development server and open `http://localhost:8080/components/wdpr-wc-polymer-textbox-custom/`.

    ```
    $ polyserve
    ```

2.  Test in IE11+ , latest google chrome and firefox browser


## Known Issues
1. Overriding shadow DOM styling using  **/deep/** (zero-or-more shadow boundary crossing) and **::shadow **(one level shadow boundary crossing) are depreciated from Web Components Spec v1.
Currently Chrome browser supports v0 but throws warning message stating "Shadow piercing combinators are depreciated". There is no alternative in Spec v1. For more details refer [here](http://hayato.io/2016/shadowdomv1/#shadow-piercing-combinators).

2. Since custom element is created without extending Native HTML elements (Input &lt;input type="text"&gt;), custom elements will not inherit any attributes, properties and methods of  Native HTML elements. We have to explicitly add those default behaviors.  