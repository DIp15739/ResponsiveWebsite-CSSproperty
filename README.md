# ResponsiveWebsite-CSSproperty
[(◔‿◔)!☞ Live Demo](https://dip15739.github.io/ResponsiveWebsite-CSSproperty/)

<p>
<a href="https://dev.to/dip15739/responsive-website-with-only-1-css-property-3ea9">
<img src="https://user-images.githubusercontent.com/42184833/94998236-fdd59680-05cd-11eb-89df-ad178df7664b.gif" height="300" /> 
</a>
</p>

Create a Responsive Website with a one CSS property. Let’s see how it's done. 🤔

Consider this template for example without apply css property🖥

<p align="center">
<img src="https://user-images.githubusercontent.com/42184833/94997491-13948d00-05c9-11eb-9533-c44d1d0547e5.png" height="350" /> 
</p>

Using The **`clamp()`**  [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) function we can create a responsive website with only one property .

Now add the magic CSS 
```css
clamp(minimum, preferred, maximum);
```
Here is! you are done✌
<p align="center">
<img src="https://user-images.githubusercontent.com/42184833/94998004-8ce1af00-05cc-11eb-9494-541bef573ea1.png" height="400" /> 
</p>

### Explanation
**`clamp()`**  works by "clamping", or restricting, a flexible value between a minimum and a maximum range.

Here's how to use it:

1.  minimum value: E.g.  `16px`
2. flexible value: E.g.  `5vw`
3.  maximum value: E.g.  `34px`

```css
h1 {
  font-size: clamp(16px, 5vw, 34px);
}
```

In this example, the  `h1`  `font-size`  value will be  `5%`  of the viewport width. But only if that value is bigger than  `16px`  and smaller than  `34px`.

For instance, if your viewport width is  `300px`, your  `5vw`  value will be equal to  `15px`. However, you clamped that  `font-size`  value to a minimum of  `16px`, so that is what is going to be.

On the other hand, if your viewport width is  `1400px`, you  `5vw`  will be a whooping  `70px`! But luckily you clamped that maximum value to  `34px`, so it won't grow past that.

<p align="center">
<img src="https://user-images.githubusercontent.com/42184833/94998236-fdd59680-05cd-11eb-89df-ad178df7664b.gif" height="300" /> 
</p>

I can add this code For this template...
```css
img {
  width: clamp(15vw, 800%, 100%);
}
h1 {
  font-size: clamp(20px, 5vw, 35px);
}
p {
  font-size: clamp(10px, 4vw, 20px);
}
```
And literally, any other property that accepts a [length, frequency, angle, time, percentage, number, or integer](https://developer.mozilla.org/en-US/docs/Web/CSS/clamp)

<p align="center">
<img src="https://user-images.githubusercontent.com/42184833/94998406-32961d80-05cf-11eb-9be9-e334a6d6e81c.png" height="330" /> 
</p>
