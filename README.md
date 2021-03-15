# SCSS-bootstrap-override

Steps:

1. npm install

    this installs:
        "bootstrap": "^4.6.0",
        "node-sass": "^5.0.0",
        "scss-compile": "^0.1.7"

    I don't know if you need all of them. 

2. npm run watch

    this runs the third line: 
        "test": "npm run scss-compile",
        "scss-compile": "node-sass -rw ./assets/scss/index.scss -o ./assets/css",
        "watch": "npm run scss-compile"

3. write your scss in assets/scss/index.scss

    if you want to divvy up your scss, write other .scss files and @import them into your index.scss
    see the secondFile.scss example

4. make sure @import "node_modules/bootstrap/scss/bootstrap";

    is after your overrides ( $variable: newValue; )

5. your html pages will reference the assets/css/index.css file. So be sure to link to that in your pages

    <link rel="stylesheet" type="text/css" media="screen" href="/assets/css/index.css" />