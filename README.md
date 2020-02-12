# SCSS Mixins

### fontSize($size)
**Description:** Returns a font-size in rem with px fallback

**Example usage**
```scss
@include fontSize(16px);
```

**Result**
```css
font-size: 16px;
font-size: 1rem;
```
---
### font($family, $size, $weight: 400)
**Description:** Returns a complete styling for font. Order of sides doesn't matter.

**Example usage**
```scss
@include font('Arial', 16px, 700);
```

**Result**
```css
font-size: 16px;
font-size: 1rem;
font-family: 'Arial';
font-weight: 700;
```


---
### position($arguments)
**Description:** A shortcut to position elements


**Example usage**
```scss
@include absolute(top 0 right 0 left 0 bottom 0);
@include fixed(right 0 left 0 bottom 0 top 0);
@include relative(top 0 left 0 right 0 bottom 0);
```

**Result**
```scss
// For absolute
position: absolute;
top: 0;
right: 0;
left: 0;
bottom: 0;

// For fixed
position: fixed;
right: 0;
left: 0;
bottom: 0;
top: 0;

// For relative
position: relative;
top: 0;
left: 0;
right: 0;
bottom: 0;
```

---
### sizing($args, $prefix: '')
**Description:** A shortcut for sizing elements


**Example usage**
```scss
@include sizing(100px);
@include sizing(100px 50px);
@include sizing(100px 50px, 'min');
```

**Result**
```scss
width: 100px;
height: 100px;

width: 100px;
height: 50px;

min-width: 100px;
min-height: 50px;
```

---
### circle($args)
**Description:** A shortcut for creating circles


**Example usage**
```scss
@include circle(100px);
```

**Result**
```scss
width: 100px;
height: 100px;
border-radius: 50%;
```

---
### three-sided-border($style, $exclude: 'top')
**Description:** Creates a border around 3 sides of container


**Example usage**
```scss
@include three-sided-border(2px solid #000);
@include three-sided-border(2px solid #000, 'left');
```

**Result**
```scss
border: 2px solid #000;
border-top: none;

border: 2px solid #000;
border-left: none;
```

---
### flex-centered
**Description:** Makes container flex and aligns everything to center


**Example usage**
```scss
@include flex-centered;
```

**Result**
```scss
display: flex;
align-items: center;
justify-content: center;
```

---
### flex-centered-y
**Description:** Makes container flex and aligns y axis to center


**Example usage**
```scss
@include flex-centered-y;
```

**Result**
```scss
display: flex;
align-items: center;
```

---
### flex-centered-x
**Description:** Makes container flex and aligns x axis to center


**Example usage**
```scss
@include flex-centered-x;
```

**Result**
```scss
display: flex;
justify-content: center;
```

---
### rwd($breakpoint)
**Description:** Generates a media query for given breakpoints. For breakpoints, check variables file.


**Example usage**
```scss
@include rwd("large") {
  max-width: 200px;
}
```

**Result**
```scss
@media (min-width: 1200px) {
  max-width: 200px;
}
```