# horiseon-refactor-accesability

---

## Technology Used 

| Technology Used         | Resource URL           | 
| ------------- |:-------------:| 
| HTML    | [https://developer.mozilla.org/en-US/docs/Web/HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) | 
| CSS     | [https://developer.mozilla.org/en-US/docs/Web/CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)      |   
| Git | [https://git-scm.com/](https://git-scm.com/)     |    

---

## Description

[Visit the Deployed Site](https://youtu.be/BFyeuLhjcPY)

Refactored an existing website to improve accessibility issues, code optimization and SEO. 

-The old code did not use semantic element naming. Division elements replaced with header, footer, article and aside elements.

-there was significant duplication of css code with multiple class names having the same code. This was consolidated by eliminating the classes and using the elements article and aside which each had common css

- Changed a class name to background-image and added aria-label for accessabilty to main image at top

- added alt attributes to multiple images for accessability

---

## Code Refactor Example

The below HTML and CSS examples show how in the original website a division with class "hero" was used to render a large photo of the company's workers in action using a background image. The problem with this is that users with vision problems would get no feedback that this photo even exists:

```HTML
<div class="hero"></div>
```
```CSS
.hero {
    height: 800px;
    width: 100%;
    margin-bottom: 25px;
    background-image: url("../images/digital-marketing-meeting.jpg");
    background-size: cover;
    background-position: center;
}
```
To help this website comply with accesablity standards, I changed the class name to "background-image" added a role attribute with an "img" value and an aria-lable attribute with value of "People working in the office" so that a visually impaired user would know the photo existed and its subject as shown below: 

```HTML
<div class="background-image" role ="img" aria-label="People working at the office"></div>
```

```CSS
.background-image {
    height: 800px;
    width: 100%;
    margin-bottom: 25px;
    background-image: url("../images/digital-marketing-meeting.jpg");
    background-size: cover;
    background-position: center;
}
```
## Usage

The 3 main products of Horiseon Social Solution Services are Search Engine Optimization, Online Reputation Management and Social Media Marketing as explained on the website home page seen on this screenshot

```md
![alt text](assets/images/Horiseon-screenshot.png)
```
---

## Learning Points

During this exercise I learned about accessability standards including:

* the use of semantic elements such as article, aside, header, footer, nav and sections which better explain what an element is being used for which helps both screen readers and for Search Engine Optimization

* using the alt attribute for images and aria-lable and other aria attributes to aid in this endevor for background images and other elements where the alt tag cannot be used to help people with vision oimpairment to understand non text elements

* There was also a great deal of code duplication in the CSS which I was able to refactor to conform to the dry principle (Don't Repeat Yourself) 

---

## Author Info

```md
### Jeffrey Nelson


* Portfolio(coming soon)
* [LinkedIn](https://www.linkedin.com/in/jeffrey-nelson13/)
* [Github](https://github.com/Jeffreydne)
```

---
## Credits

The original website, and the table of technology used  in this README.md were both provided by the excellent staff at UC Berkeley Extension Full Stack Bootcamp