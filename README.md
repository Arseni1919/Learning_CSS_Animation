# Learning CSS Animation

## [style.css](static/style.css)

```css
* {
    margin: 0;
    padding: 0;
}
body {
    background: #333;
    font-family: "Arial Hebrew Scholar";
    color: wheat;
    line-height: 1.6;
    text-align: center;
}
h1 {

    text-align: center;

}

.box {
    background: white;
    width: 200px;
    height: 200px;
    position: relative;
    animation-name: myanimation;
    animation-duration: 4s;
    /*animation-iteration-count: infinite;*/
    animation-iteration-count: 1;
    animation-delay: 1s;
    /*animation-direction: reverse;*/
    animation-direction: alternate;
    /*animation-timing-function: linear;*/
    /*animation-timing-function: ease-in;*/
    /*animation-timing-function: ease-out;*/
    animation-fill-mode: forwards;

}

@keyframes myanimation {
    0% {
        background-color: wheat;
        left: 0px;
        top: 0px;
        border-radius: 0;
    }
    25% {
        background-color: red;
        left: 300px;
        top: 0px;
        border-radius: 50%;
    }
    50% {
        background-color: green;
        left: 300px;
        top: 300px;
        border-radius: 0;
    }
    75% {
        background-color: blue;
        left: 0px;
        top: 300px;
        border-radius: 50%;
    }
    100% {
        background-color: white;
        left: 0px;
        top: 0px;
        border-radius: 50%;
    }
}

.box2 {
    background: white;
    width: 300px;
    height: 300px;
    position: relative;
    margin: auto;
    top: 200px;
    /*transition-property: background, border-radius, transform;*/
    transition-property: all;
    transition-duration: 0.25s;
    /*transition-duration: 0.25s, 3s;*/
    /*transition-delay: 2s, 4s;*/
    /*transition-timing-function: linear;*/
}

.box2:hover {
    background: red;
    border-radius: 50%;
    transform: rotateZ(180deg);
}

.container {
    max-width: 960px;
    margin: auto;
    padding: 0 30px;
}

#showcase {
    height: 300px;
}

#showcase h1 {
    font-size: 50px;
    line-height: 1.3;
    position: relative;
    animation: heading;
    animation-duration: 3s;
    animation-fill-mode: forwards;
}

@keyframes heading {
    0% {top: -50px}
    100% {top: 200px}
}

#content {
    position: relative;
    animation-name: content;
    animation-duration: 3s;
    animation-fill-mode: forwards;
}

@keyframes content {
    0% {left: -1000px}
    100% {left: 0}
}

.btn {
    display: inline-block;
    color: white;
    text-decoration: none;
    padding: 1rem 2rem;
    border: #fff 1px solid;
    margin-top: 40px;
    opacity: 0;
    animation-name: btn;
    animation-duration: 3s;
    animation-delay: 3s;
    animation-fill-mode: forwards;

    transition-property: transform;
    transition-duration: 1s;
}

@keyframes btn {
    0% {opacity: 0}
    100% {opacity: 1}
}

.btn:hover {
    transform: rotateZ(360deg);
}
```
## Credits

- [youtube | CSS3 Animation & Transitions Crash Course](https://www.youtube.com/watch?v=zHUpx90NerM&ab_channel=TraversyMedia)