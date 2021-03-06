# Sass Handy Tips

### -Sass info
`sass -h`
### - Convert files (.sass & .scss)
`sass-convert fileName.scss fileName.sass`

### - Convert to css files
`sass fileName.scss:fileName.css`

### - Watch files
`sass --watch fileName.scss:fileName.css`

### - Watch entire directory and point to a css/styles directory
`sass --watch Directory:CSS`

### - Specify compiling format 
````sass fileName.scss:fileName.css --style compact````  
````sass fileName.scss:fileName.css --style compressed````   
````sass fileName.scss:fileName.css --style expanded````  

### NO .map 
`sass fileName.scss:fileName.css --style expanded --sourcemap=none`

### Go from diff directories to file + NO .map + No Cache 
`sass scss/nav.scss:css/nav.css --style expanded --sourcemap=none --no-cache`

### Watch it
````sass --watch fileName.scss:fileName.css --style expanded --sourcemap=none````  
````sass --watch Directory:CSS --style expanded --sourcemap=none````  

### Variables naming convention (no spaces or spec characters, numbers are fine)
`$white:#fff;`
`$white2:#fff;`

### Share Properties
#### Set place holder
``%shared {
    font-size: 1px;
}``

#### Share it
``
body {
@extend %shared;
}
``

### Mixins
#### create
`@mixin cssProperties {
color: green;
}`
#### call 
``body {
    @include cssProperties();
}
``
#### pass arguments
`@mixin cssProperties($arg1)`
#### call 
``body {
    @include cssProperties(green);
}
``

#### A few built in functions
`lenght(), nth(), set-nth(), list-separator(), join(), append(), index(), zip()`

#### maps are manipulated by SASS scripts functions
`map_keys(), map_values(), map_has_key(), map_get(), map_merge(), inspect(), map_remove()`

#### SASS math operators
`round(), floor(), ceil(), percentage(), abs(), min(), max(), random()`

#### if else syntax
`@if, @else, @else if`

#### loops
`@for, @each, @while`

#### functions
`@function`

### DRY - Source Maps lets you make changes on the fly (browser) and automatically add to your local project
````On Terminal go to source tab````
````right click on desired file````
````Add folder to workspace````
```Allow Permissions```

### Responsive Design
`check out grid and media queries directory`
 
