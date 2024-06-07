* There are two main color models: the additive RGB (red, green, blue) model used in electronic devices, and the subtractive CMYK (cyan, magenta, yellow, black) model used in print.
In this project, you'll work with the RGB model. This means that colors begin as black, and change as different levels of red, green, and blue are introduced. An easy way to see this is with the CSS rgb function.

* While the red and blue markers look the same, the green one is much lighter than it was before. This is because the green color keyword is actually a darker shade, and is about halfway between black and the maximum value for green.

* A color wheel is a circle where similar colors, or hues, are near each other, and different ones are further apart. For example, pure red is between the hues rose and orange.
Two colors that are opposite from each other on the color wheel are called complementary colors. If two complementary colors are combined, they produce gray. But when they are placed side-by-side, these colors produce strong visual contrast and appear brighter.

In the rgb function for the .one CSS rule, set the red value to the max of 255 to produce pure red. In the rgb function for .two CSS rule, set the values for green and blue to the max of 255 to produce cyan.
In the .two CSS rule, set the green value in the rgb function to 127 to lower its intensity.

* The HSL color model, or hue, saturation, and lightness, is another way to represent colors.
The CSS hsl function accepts 3 values: a number from 0 to 360 for hue, a percentage from 0 to 100 for saturation, and a percentage from 0 to 100 for lightness.
If you imagine a color wheel, the hue red is at 0 degrees, green is at 120 degrees, and blue is at 240 degrees.
Saturation is the intensity of a color from 0%, or gray, to 100% for pure color. You must add the percent sign % to the saturation and lightness values.
Lightness is how bright a color appears, from 0%, or complete black, to 100%, complete white, with 50% being neutral.

==> In the .blue CSS rule, use the hsl function to change the background-color property to pure blue. Set the hue to 240, the saturation to 100%, and the lightness to 50%. <"background-color: hsl(240, 100%, 50%);">

* You've learned a few ways to set flat colors in CSS, but you can also use a color transition, or gradient, on an element.
A gradient is when one color transitions into another. The CSS linear-gradient function lets you control the direction of the transition along a line, and which colors are used.
One thing to remember is that the linear-gradient function actually creates an image element, and is usually paired with the background property which can accept an image as a value.

* The linear-gradient function is very flexible -- here is the basic syntax you'll use in this tutorial:
linear-gradient(gradientDirection, color1, color2, ...);
gradientDirection is the direction of the line used for the transition. color1 and color2 are color arguments, which are the colors that will be used in the transition itself. These can be any type of color, including color keywords, hex, rgb, or hsl.

==>   background: linear-gradient(90deg, rgb(255, 0, 0), rgb(0, 255, 255));

Color-stops allow you to fine-tune where colors are placed along the gradient line. They are a length unit like px or percentages that follow a color in the linear-gradient function.

==> linear-gradient(90deg, red 90%, black);

* Even without the color-stops, you might have noticed that the colors for the green marker transition at the same points as the red marker. The first color is at the start (0%), the second is in the middle (50%), and the last is at the end (100%) of the gradient line.
The linear-gradient function automatically calculates these values for you, and places colors evenly along the gradient line by default.

* If no gradientDirection argument is provided to the linear-gradient function, it arranges colors from top to bottom, or along a 180 degree line, by default.

* Another way to set the opacity for an element is with the alpha channel. Similar to the opacity property, the alpha channel controls how transparent or opaque a color is.
You've already set sleeve's opacity with a named color and the opacity property, but you can add an alpha channel to the other CSS color properties.

* (!!) It looks like your sleeve disappeared, but don't worry -- it's still there. What happened is that your new cap div is taking up the entire width of the marker, and is pushing the sleeve down to the next line.
This is because the default display property for div elements is block. So when two block elements are next to each other, they stack like actual blocks. For example, your marker elements are all stacked on top of each other.

* The last thing you'll do is add a slight shadow to each marker to make them look even more realistic.
The box-shadow property lets you apply one or more shadows around an element. Here is basic syntax:
box-shadow: offsetX offsetY color;
Here's how the offsetX and offsetY values work:
both offsetX and offsetY accept number values in px and other CSS units
a positive offsetX value moves the shadow right and a negative value moves it left
a positive offsetY value moves the shadow down and a negative value moves it up
if you want a value of zero (0) for any or both offsetX and offsetY, you don't need to add a unit. Every browser understands that zero means no change.
The height and width of the shadow is determined by the height and width of the element it's applied to. You can also use an optional --"spreadRadius"-- value to spread out the reach of the shadow. More on that later.

* an optional blurRadius value for the box-shadow property:
box-shadow: offsetX offsetY blurRadius color;
If a blurRadius value isn't included, it defaults to 0 and produces sharp edges. The higher the value of blurRadius, the greater the blurring effect is.

* The vh unit stands for viewport height, and is equal to 1% of the height of the viewport. This makes it relative to the viewport height.

* (!!)Now, get rid of the horizontal scroll-bar, by setting the body default margin added by some browsers to 0.

* (!!) That is better. Now, make the background easy on the eyes, by changing the body background-color to #1b1b32. Then, to see the text, change the color to #f5f6f7.

* The rem unit stands for root em, and is relative to the font size of the html element.

* Nest an input element within each label. Be sure to add each input after the label text, and include a space after the colon.

==>   <fieldset>
        <label>Enter Your First Name:<input></label>
        <label>Enter Your Last Name:<input></label>
        <label>Enter Your Email:<input></label>
        <label>Create a New Password:<input></label>
      </fieldset>