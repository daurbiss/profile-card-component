# Frontend Mentor - Profile card component solution

This is a solution to the [Profile card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/profile-card-component-cfArpWshJ). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Links

- Live Site URL: [Click here](https://daurbiss.github.io/profile-card-component)

## What I learned

### Styling the background

I have learnt the background property - a shortcut for using multiple attributes like url(), position and no-repeat.
Main challenge was to position the 2 background images so that they adjust in both size and position when display width changes. I found using a "55vw" background size allowed me to position the circles relative to its size, hence why I used vw units.
I have also learnt that I can use right/bottom and -10vw -21vw together.

I used media query to fix the size of the 2 circles and their position when the screen size gets smaller than 766px.

```css
body {
  background:
    url("../images/bg-pattern-top.svg")
    -10vw -21vw
    no-repeat,
    url("../images/bg-pattern-bottom.svg")
    right -10vw bottom -21vw
    no-repeat;
  background-size: 55vw;
  background-color: hsl(185, 75%, 39%);
  font-family: "Kumbh Sans", sans-serif;
}

@media only screen and (max-width: 765px) {
  body {
    background:
      url("../images/bg-pattern-top.svg")
      -80px -159px
      no-repeat,
      url("../images/bg-pattern-bottom.svg")
      right -80px bottom -159px
      no-repeat;
    background-size: 420.75px;
    background-color: hsl(185, 75%, 39%);
  }
}
```

### hr line

I learnt to style the horizontal line in a way that it looks "professional", i.e. really thin and greyish colour.

```css
hr {
  border: 0;
  height: 0;
  border-top: 1px solid rgba(0, 0, 0, 0.1);
  border-bottom: 1px solid rgba(255, 255, 255, 0.3);
}
```

### Profile picture position

I learnt positioning the image using position: relative. I had to limit the height of the top div (which includes the pattern and profile pic) to allow the name and age to follow straight after the profile pic. 

```css
.profile-pic {
  border-style: solid;
  border-radius: 5em;
  border-color: white;
  border-width: thick;
  position: relative;
  bottom: 3.5em;
}
```
