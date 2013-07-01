# SASSY ICONS

The purpose of this small project is to gain a basic understanding of SASS while learning to create shapes with CSS.

## Intro to SASS

**Why SASS?**
- Cleaner and simpler syntax than CSS
- Smaller and more manageable styles files with less scrolling
- Ability to create variables and mixins

**Two Flavors! SASS and SCSS**
- Compare SASS and SCSS on the [SASS homepage] (http://sass-lang.com/)
- SASS, or .sass files, has a stripped down syntax with no curly braces or semicolons which is more human-readable
- SCSS, or .scss files, has a syntax more similar to CSS which allows people to write regular CSS in an SCSS file
	
**Compiling SASS**
- SASS and SCSS files are compiled into a master CSS file by an application such as Terminal (running Ruby) or CodeKit. These applications monitor for edits you make to your SASS files and add those changes with proper syntax to your CSS file.
- SASS allows you to break your styles into separate files called partials, which are compiled into a master SASS file (which is then compiled to the master CSS file). Partials are not necessary for this project, but good to be aware of!
	
**Check out the [SASS Tutorial] (http://sass-lang.com/tutorial.html)** for the basics, particularly:
- Nesting and Parent References
- Variables

## CSS Shapes

**Why CSS shapes?**
- Quick and scalable - resize shapes instantly instead of re-saving Photoshop shapes
- Improve browser performance - somewhat debatable, but at least it reduces HTTP requests
	
**See examples of [CSS Shapes] (http://css-tricks.com/examples/ShapesOfCSS)**
- Circles have identical height and width values with a border-radius of half that value (either px, em, or 50%)
`.circle { height: 100px; width: 100px;	border-radius: 50%; }`
- Triangles are basically made of rectangle borders. The rectangle itself has a height and width of 0, but its borders have values and some of the borders are transparent.
` .triangle { width: 0; height: 0; border-left: 50px solid transparent; border-right: 50px solid transparent; border-bottom: 100px solid red; }`

## Intro to CodePen

- Explore [CodePen] (http://codepen.io) to see what kinds of projects people are making.
- Each "Pen" has a layout with four sections:
  - HTML
  - CSS
  - JS
  - Browser Preview
- CodePen will compile SASS to CSS for us on the fly in the browser, so we do not need to download or install anything. Note that CodePen is very aggressive with correcting SASS errors and will autocheck for errors constantly as you type.

- Two example projects I created for this class:
  - Easier and quicker: [Big Email Button] (http://codepen.io/leshields/pen/JtIAo) 
  - More time-consuming: [Arduino Logo] (http://codepen.io/leshields/pen/hsduo)

## Create Your Own SASSy Icon!

1. Sign up for a free [CodePen] (http://codepen.io) account.
2. Login and create a new Pen.
3. Change the CSS setting (small gear button in upper-right) to "SASS with Compass", or "SCSS with Compass" if you prefer.
4. Add a SASS variable for a color, such as $blue: #50aded, into your CSS Pen.
5. Copy and paste code for a CSS shape into your Pen to get started.
6. Code away until you have a SASSy icon!
