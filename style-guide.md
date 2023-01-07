# Front-end Style Guide

## Layout

The designs were created to the following widths:

- Mobile: 375px
- Desktop: 1440px

## Colors

### Primary

- Soft blue: hsl(215, 51%, 70%)
- Cyan: hsl(178, 100%, 50%)

### Neutral

- Very dark blue (main BG): hsl(217, 54%, 11%)
- Very dark blue (card BG): hsl(216, 50%, 16%)
- Very dark blue (line): hsl(215, 32%, 27%)
- White: hsl(0, 0%, 100%)

## Typography

### Body Copy

- Font size (paragraph): 18px

### Font

- Family: [Outfit](https://fonts.google.com/specimen/Outfit)
- Weights: 300, 400, 600



@import url('https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,700&family=Montserrat:wght@500;700&family=Outfit:wght@300;400;600&display=swap');
:root {
    --color-main-bg: hsl(217, 54%, 11%);
    --color-card-shadow: hsl(215, 50%, 10%);
    --color-horizontal-line: hsl(215, 32%, 27%);
    --color-white: hsl(0, 0%, 100%) ;
    --color-soft-blue: hsl(215, 51%, 70%);
    --color-cyan: hsl(178, 100%, 50%) ;
    --color-card-bg: hsl(216, 50%, 16%);
    --radius-border: 10px;
}

* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}


html {
    font-family: 'Outfit', sans-serif;
    
}

/* Global styles */

.m-t {
    margin-top: 1rem;
}

.m-b {
    margin-bottom: 1rem;
}

img {
    max-inline-size: 100%;
    block-size: auto;
}

.card-description h2:hover,
.author:hover span>span {
    cursor:pointer;
    color: var(--color-cyan);
}
/* <------------> */

main {
    background-color: var(--color-main-bg);
    min-height: 100vh;
    display: flex;
    align-items: center;
}


section.container {
    box-shadow: 0 10px 15px 10px var(--color-card-shadow);
    background-color: hsl(216, 50%, 16%);
    max-width: 300px;
    margin: 0 auto;
    padding: 1.5rem 1.5rem;
    border-radius:var(--radius-border);
}

.image-main {
    font-size: 0px;
}

.card-image {
    position: relative;
}


.card-image:hover::after {
    content: "";
    opacity: 0.4;
    position: absolute;
    top: 0; left:0;
    inline-size: 100%;
    block-size: 100%;
    z-index: 1;
    border-radius:var(--radius-border);
    animation: bg-animate ease 200ms forwards;
    cursor: pointer;
}


@keyframes bg-animate {
    0% {
        background-color: transparent;
    }

    100% {
        background-color: var(--color-cyan);
    }
}

.card-image i {
    position: absolute;
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    z-index: 2; color: var(--color-white);
    transition: font-size 50ms ease;
}

.card-image:hover i {
    font-size: initial;
}

.card-image img {
    border-radius:var(--radius-border);
}

.card-description h2 {
    color: var(--color-white);
    transition: color 200ms;
}

.card-description p {
    color: var(--color-soft-blue);
    line-height: 1.4;
    font-size: 1.2rem;
    font-weight: 300;
}

.time-status {
    display: flex;
    justify-content: space-between;
    margin-bottom: 1.5rem;
}

.time-status span:nth-of-type(1) {
    color: var(--color-cyan);
}

.time-status i {margin-right: 0.200rem;}

.time-status span:nth-of-type(2) {
    color: var(--color-soft-blue);
}

.author span {
    color: var(--color-soft-blue);
    line-height: 30px;
    vertical-align: middle;
}

.author span>span {
    color: var(--color-white);
    transition: color 200ms;
}

.hr {
    border: 1px solid var(--color-horizontal-line);
}

.author-image {
    display: inline-block;
    width: 30px;
    height: 30px;
    border-radius:50%;
    border: 1px solid var(--color-white);
    margin-right: 0.675rem;
}


footer {
    background: black;
}

.attribution {
    padding: 2rem;
    text-align: center;
    color: var(--color-white);
}